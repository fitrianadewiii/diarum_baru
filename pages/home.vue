<template>
  <section>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="section">
      <div class="columns">

        <main class="column">
          <div class="level">
            <div class="level-left">
              <div class="level-item">
                <div class="title">Dashboard</div>
              </div>
            </div>
            <div class="level-right">
              <div class="level-item">
                <button type="button" class="button is-small">
                  March 8, 2017 - April 6, 2017
                </button>
              </div>
            </div>
          </div>

          <div class="columns is-multiline">
            <div class="column">
              <div class="box">
                <div class="heading"><b>Total Checkin Today</b></div>
                <div class="title">
                  560
                </div>
              </div>
            </div>
            <div class="column">
              <div class="box">
                <div class="heading"><b>Total List Activity Today</b></div>
                <div class="title">560</div>
              </div>
            </div>
            <div class="column">
              <div class="box">
                <div class="heading"><b>Total News</b></div>
                <div class="title">560</div>
              </div>
            </div>
            <div class="column">
              <div class="box">
                <div class="heading"><b>Total Member</b></div>
                <div class="title">560</div>
              </div>
            </div>
          </div>

          <div class="columns is-multiline">
            <div class="column is-6">
              <div class="panel">
                <p class="panel-heading">
                  <b>Total Checkin Today</b>
                </p>
                <div class="panel-block">

                  <div class="center-chart" id="chartdiv">
                  </div>

                </div>
              </div>
            </div>
            <div class="column is-6">
              <div class="panel">
                <p class="panel-heading">
                  <b>Total List Activity Today</b>
                </p>
                <div class="panel-block">
                  <div class="center-chart" id="chartdiv1">
                  </div>
                </div>
              </div>
            </div>
            <div class="column is-6">
              <div class="panel">
                <p class="panel-heading">
                  <b>Total News</b>
                </p>
                <div class="panel-block">
                  <div class="center-chart" id="chartdiv2">
                  </div>
                </div>
              </div>
            </div>
            <div class="column is-6">
              <div class="panel">
                <p class="panel-heading">
                  <b>Total Member</b>
                </p>
                <div class="panel-block">
                  <div class="center-chart" id="chartdiv3">
                  </div>
                </div>
              </div>
            </div>
          </div>
        </main>
      </div>
    </div>
  </section>
</template>



<script>
  import * as am4core from "@amcharts/amcharts4/core";
  import * as am4charts from "@amcharts/amcharts4/charts";
  import am4themes_animated from "@amcharts/amcharts4/themes/animated";
  import Logo from '~/components/Logo.vue'

  am4core.useTheme(am4themes_animated);

  export default {
    components: {
      Logo

    },
    name: 'hello',
    mounted() {

      // Create chart instance
      var chart = am4core.create("chartdiv", am4charts.XYChart3D);

     

      // Add data
      chart.data = [{
        "country": "Senin",
        "visits": 10
      }, {
        "country": "Selasa",
        "visits": 30
      }, {
        "country": "Rabu",
        "visits": 40
      }, {
        "country": "Kamis",
        "visits": 50
      }, {
        "country": "Jumat",
        "visits": 30
      }];

      // Create axes
      let categoryAxis = chart.xAxes.push(new am4charts.CategoryAxis());
      categoryAxis.dataFields.category = "country";
      categoryAxis.renderer.labels.template.rotation = 270;
      categoryAxis.renderer.labels.template.hideOversized = false;
      categoryAxis.renderer.minGridDistance = 20;
      categoryAxis.renderer.labels.template.horizontalCenter = "right";
      categoryAxis.renderer.labels.template.verticalCenter = "middle";
      categoryAxis.tooltip.label.rotation = 270;
      categoryAxis.tooltip.label.horizontalCenter = "right";
      categoryAxis.tooltip.label.verticalCenter = "middle";

      let valueAxis = chart.yAxes.push(new am4charts.ValueAxis());
      valueAxis.title.text = "";
      valueAxis.title.fontWeight = "bold";

      // Create series
      var series = chart.series.push(new am4charts.ColumnSeries3D());
      series.dataFields.valueY = "visits";
      series.dataFields.categoryX = "country";
      series.name = "Visits";
      series.tooltipText = "{categoryX}: [bold]{valueY}[/]";
      series.columns.template.fillOpacity = .8;

      var columnTemplate = series.columns.template;
      columnTemplate.strokeWidth = 2;
      columnTemplate.strokeOpacity = 1;
      columnTemplate.stroke = am4core.color("#FFFFFF");

      columnTemplate.adapter.add("fill", (fill, target) => {
        return chart.colors.getIndex(target.dataItem.index);
      })

      columnTemplate.adapter.add("stroke", (stroke, target) => {
        return chart.colors.getIndex(target.dataItem.index);
      })

      chart.cursor = new am4charts.XYCursor();
      chart.cursor.lineX.strokeOpacity = 0;
      chart.cursor.lineY.strokeOpacity = 0;


      // Chart Baru

      // Create chart instance
      var chart2 = am4core.create("chartdiv2", am4charts.XYChart3D);

      // Add data
      chart2.data = [{
        "country": "Senin",
        "visits": 10
      }, {
        "country": "Selasa",
        "visits": 30
      }, {
        "country": "Rabu",
        "visits": 40
      }, {
        "country": "Kamis",
        "visits": 50
      }, {
        "country": "Jumat",
        "visits": 30
      }];

      // Create axes
      let categoryAxis2 = chart2.xAxes.push(new am4charts.CategoryAxis());
      categoryAxis2.dataFields.category = "country";
      categoryAxis2.renderer.labels.template.rotation = 270;
      categoryAxis2.renderer.labels.template.hideOversized = false;
      categoryAxis2.renderer.minGridDistance = 20;
      categoryAxis2.renderer.labels.template.horizontalCenter = "right";
      categoryAxis2.renderer.labels.template.verticalCenter = "middle";
      categoryAxis2.tooltip.label.rotation = 270;
      categoryAxis2.tooltip.label.horizontalCenter = "right";
      categoryAxis2.tooltip.label.verticalCenter = "middle";

      let valueAxis2 = chart2.yAxes.push(new am4charts.ValueAxis());
      valueAxis2.title.text = "";
      valueAxis2.title.fontWeight = "bold";

      // Create series
      var series = chart2.series.push(new am4charts.ColumnSeries3D());
      series.dataFields.valueY = "visits";
      series.dataFields.categoryX = "country";
      series.name = "Visits";
      series.tooltipText = "{categoryX}: [bold]{valueY}[/]";
      series.columns.template.fillOpacity = .8;

      var columnTemplate2 = series.columns.template;
      columnTemplate2.strokeWidth = 2;
      columnTemplate2.strokeOpacity = 1;
      columnTemplate2.stroke = am4core.color("#FFFFFF");

      columnTemplate2.adapter.add("fill", (fill, target) => {
        return chart2.colors.getIndex(target.dataItem.index);
      })

      columnTemplate2.adapter.add("stroke", (stroke, target) => {
        return chart2.colors.getIndex(target.dataItem.index);
      })

      chart2.cursor = new am4charts.XYCursor();
      chart2.cursor.lineX.strokeOpacity = 0;
      chart2.cursor.lineY.strokeOpacity = 0;


      // chart baru

      // Create chart instance
      var chart3 = am4core.create("chartdiv1", am4charts.XYChart3D);



      // Add data
      chart3.data = [{
        "country": "Senin",
        "visits": 10
      }, {
        "country": "Selasa",
        "visits": 30
      }, {
        "country": "Rabu",
        "visits": 40
      }, {
        "country": "Kamis",
        "visits": 50
      }, {
        "country": "Jumat",
        "visits": 30
      }];

      // Create axes
      let categoryAxis3 = chart3.xAxes.push(new am4charts.CategoryAxis());
      categoryAxis3.dataFields.category = "country";
      categoryAxis3.renderer.labels.template.rotation = 270;
      categoryAxis3.renderer.labels.template.hideOversized = false;
      categoryAxis3.renderer.minGridDistance = 20;
      categoryAxis3.renderer.labels.template.horizontalCenter = "right";
      categoryAxis3.renderer.labels.template.verticalCenter = "middle";
      categoryAxis3.tooltip.label.rotation = 270;
      categoryAxis3.tooltip.label.horizontalCenter = "right";
      categoryAxis3.tooltip.label.verticalCenter = "middle";

      let valueAxis3 = chart3.yAxes.push(new am4charts.ValueAxis());
      valueAxis3.title.text = "";
      valueAxis3.title.fontWeight = "bold";

      // Create series
      var series = chart3.series.push(new am4charts.ColumnSeries3D());
      series.dataFields.valueY = "visits";
      series.dataFields.categoryX = "country";
      series.name = "Visits";
      series.tooltipText = "{categoryX}: [bold]{valueY}[/]";
      series.columns.template.fillOpacity = .8;

      var columnTemplate3 = series.columns.template;
      columnTemplate3.strokeWidth = 2;
      columnTemplate3.strokeOpacity = 1;
      columnTemplate3.stroke = am4core.color("#FFFFFF");

      columnTemplate3.adapter.add("fill", (fill, target) => {
        return chart3.colors.getIndex(target.dataItem.index);
      })

      columnTemplate3.adapter.add("stroke", (stroke, target) => {
        return chart3.colors.getIndex(target.dataItem.index);
      })

      chart3.cursor = new am4charts.XYCursor();
      chart3.cursor.lineX.strokeOpacity = 0;
      chart3.cursor.lineY.strokeOpacity = 0;




      // piechart
      let chart4 = am4core.create("chartdiv3", am4charts.PieChart3D);
      chart.hiddenState.properties.opacity = 0; // this creates initial fade-in

      chart4.data = [{
          country: "Belum Checkin",
          litres: 50
        },
        {
          country: "Checkin",
          litres: 150
        }

      ];

      chart4.innerRadius = am4core.percent(50);
      chart4.depth = 10;
      

      chart4.legend = new am4charts.Legend();

      let series4 = chart4.series.push(new am4charts.PieSeries3D());
      series4.dataFields.value = "litres";
      series4.dataFields.depthValue = "litres";
      series4.dataFields.category = "country";
      series4.slices.template.cornerRadius = 5;
      series4.colors.step = 3;


    },





  }

</script>
<style>
  .center-chart {
    margin-left: auto;
    margin-right: auto
  }

  .panel-block {
    align-items: center;
    color: #363636;
    display: flex;
    height: 300px;
    justify-content: flex-start;
    padding: 0.5em 0.75em;
  }

</style>
