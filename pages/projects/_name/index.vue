<template>
  <div class="row">
    <!-- <h1>Project with id {{ name }}</h1> -->
    <!-- Stats Cards -->
    <div class="col-lg-3 col-md-6" v-for="card in statsCards" :key="card.title">
      <stats-card
        :title="card.title"
        :sub-title="card.subTitle"
        :type="card.type"
        :icon="card.icon"
      >
        <div slot="footer" v-html="card.footer"></div>
      </stats-card>
    </div>

    <!-- Small charts -->
    <!-- <div class="col-lg-4" :class="{ 'text-right': isRTL }">
      <card type="chart">
        <template slot="header">
          <h5 class="card-category">Total Shipments</h5>
          <h3 class="card-title">
            <i class="tim-icons icon-bell-55 text-primary "></i> 763,215
          </h3>
        </template>
        <div class="chart-area">
          <line-chart
            style="height: 100%"
            :chart-data="purpleLineChart.chartData"
            :gradient-colors="purpleLineChart.gradientColors"
            :gradient-stops="purpleLineChart.gradientStops"
            :extra-options="purpleLineChart.extraOptions"
          >
          </line-chart>
        </div>
      </card>
    </div>
    <div class="col-lg-4" :class="{ 'text-right': isRTL }">
      <card type="chart">
        <template slot="header">
          <h5 class="card-category">Daily Sales</h5>
          <h3 class="card-title">
            <i class="tim-icons icon-delivery-fast text-info "></i> 3,500€
          </h3>
        </template>
        <div class="chart-area">
          <bar-chart
            style="height: 100%"
            :chart-data="blueBarChart.chartData"
            :gradient-stops="blueBarChart.gradientStops"
            :extra-options="blueBarChart.extraOptions"
          >
          </bar-chart>
        </div>
      </card>
    </div>
    <div class="col-lg-4" :class="{ 'text-right': isRTL }">
      <card type="chart">
        <template slot="header">
          <h5 class="card-category">Completed tasks</h5>
          <h3 class="card-title">
            <i class="tim-icons icon-send text-success "></i> 12,100K
          </h3>
        </template>
        <div class="chart-area">
          <line-chart
            style="height: 100%"
            :chart-data="greenLineChart.chartData"
            :gradient-stops="greenLineChart.gradientStops"
            :extra-options="greenLineChart.extraOptions"
          >
          </line-chart>
        </div>
      </card>
    </div> -->
    <div class="col-lg-5">
      <card type="tasks" :header-classes="{ 'text-right': isRTL }">
        <template slot="header">
          <h6 class="title d-inline">Tasks (5)</h6>
          <p class="card-category d-inline">Today</p>
          <base-dropdown
            menu-on-right=""
            tag="div"
            title-classes="btn btn-link btn-icon"
            :class="{ 'float-left': isRTL }"
          >
            <i slot="title" class="tim-icons icon-settings-gear-63"></i>
            <a class="dropdown-item" href="#pablo"> Action </a>
            <a class="dropdown-item" href="#pablo"> Another action </a>
            <a class="dropdown-item" href="#pablo"> Something else </a>
          </base-dropdown>
        </template>
        <div class="table-full-width table-responsive">
          <task-list></task-list>
        </div>
      </card>
    </div>
    <div class="col-lg-7">
      <card class="card" :header-classes="{ 'text-right': isRTL }">
        <h5 slot="header" class="card-title">Team</h5>
        <div class="table-responsive">
          <user-table></user-table>
        </div>
      </card>
    </div>
    <!-- <div class="col-lg-12"><country-map-card></country-map-card></!-->
  </div>
</template>

<script>
import StatsCard from '@/components/Cards/StatsCard';
import TaskList from '@/components/Dashboard/TaskList';
import CountryMapCard from '@/components/Dashboard/CountryMapCard';
import UserTable from '@/components/Dashboard/UserTable';

export default {
  components: {
    TaskList,
    StatsCard,
    CountryMapCard,
    UserTable
  },
  validate ({ params }) {
    return true
  },
  computed: {
    isRTL () {
      return this.$rtl.isRTL;
    }
  },
  data() {
    return {
      name: this.$route.params.name,
      statsCards: [
        {
          title: '93',
          subTitle: 'Companies',
          type: 'warning',
          icon: 'tim-icons icon-chat-33',
          footer: '<a href="/projects/eLegacy/companies"><i class="tim-icons icon-bank"></i> Mostra</a>'
        },
        {
          title: '12',
          subTitle: 'Nuove email',
          type: 'primary',
          icon: 'tim-icons icon-email-85',
          footer: '<a href="/projects/eLegacy/mails"><i class="tim-icons icon-sound-wave"></i></i> Mostra</a>'
        },
        {
          title: '2',
          subTitle: 'Appuntamenti',
          type: 'info',
          icon: 'tim-icons icon-calendar-60',
          footer: '<i class="tim-icons icon-trophy"></i> Mostra'
        },
        {
          title: '4',
          subTitle: 'Team',
          type: 'danger',
          icon: 'tim-icons icon-molecule-40',
          footer: '<i class="tim-icons icon-watch-time"></i> In the last hours'
        }
      ]
    }
  }
}
</script>