<template>
  <div class="page">
    <Header />
    <Navigation />
    <div class="page__wrap">
      <div class="page__wrap__inner">
        <div class="title__wrap dashboard">
          <h2 class="f-midium page__title">Dashboards</h2>
          <dl>
            <dt class="f-midium">Auto Refresh</dt>
            <dd>
              <button class="toggle__btn"><span></span></button>
            </dd>
          </dl>
        </div>
        <p class="today__date">
          {{ todayTxt }}
        </p>
        <Statebar />
        <RealtimeSales />
        <DailySales />
        <WeeklySales />
        <MonthlySales />
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api';
import Header from '@/pages/layout/header.vue';
import Navigation from '@/pages/layout/nav.vue';
import Statebar from '@/components/dashboards/statebar.vue';
import RealtimeSales from '@/components/dashboards/realtime-sales.vue';
import DailySales from '@/components/dashboards/daily-sales.vue';
import WeeklySales from '@/components/dashboards/weekly-sales.vue';
import MonthlySales from '@/components/dashboards/monthly-sales.vue';
import { Chart, registerables } from 'chart.js';

Chart.register(...registerables);

export default defineComponent({
  components: {
    Header,
    Navigation,
    Statebar,
    RealtimeSales,
    DailySales,
    WeeklySales,
    MonthlySales,
  },
  setup() {
    const dayArr = [
      'Sunday',
      'Monday',
      'Tuesday',
      'Wednesday',
      'Thursday',
      'Friday',
      'Saturday',
    ];

    const month = new Date().getMonth() + 1;
    const date = new Date().getDate();
    const year = new Date().getFullYear();
    const day = new Date().getDay();

    const todayTxt = `Today is ${dayArr[day]}, ${date} ${month} ${year}`;

    return {
      todayTxt,
    };
  },
});
</script>
