<template>
  <apexchart
    type="donut"
    height="350"
    :options="chartOptions"
    :series="series"
  />
</template>

<script lang="ts">
import {defineComponent, reactive, toRefs} from 'vue'

export default defineComponent({
  setup () {
    const data = reactive({
      chartOptions: {
        chart: {
          type: 'donut',
        },
        responsive: [
          {
            breakpoint : 480,
            options    : {
              chart: {
                width: 200
              },
              legend: {
                position: 'bottom'
              }
            }
          }
        ]
      },
      series: [
        44, 55, 41, 17, 15
      ],
    })

    return {
      ...toRefs(data),
    }
  },
})

</script>
