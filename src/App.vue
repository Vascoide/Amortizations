<!-- src/App.vue -->

<template>
  <AmortizationList :amortizations="amortizations" />
</template>

<script>
import AmortizationList from "@/components/AmortizationList.vue";

export default {
  components: {
    AmortizationList,
  },
  data() {
    return {
      amortizations: [
        {'schedule_date': '2023-06-21 07:24:35', 'state': 'pending', 'amount': 1388, 'project_id': 9},
        {'schedule_date': '2023-05-01 09:26:19', 'state': 'paid', 'amount': 2659, 'project_id': 10},
        {'schedule_date': '2023-06-21 02:23:31', 'state': 'pending', 'amount': 1814, 'project_id': 9},
        {'schedule_date': '2023-05-05 07:23:18', 'state': 'paid', 'amount': 2522, 'project_id': 9},
        {'schedule_date': '2023-06-27 08:52:13', 'state': 'pending', 'amount': 3616, 'project_id': 5},
        {'schedule_date': '2023-06-05 18:08:05', 'state': 'pending', 'amount': 3571, 'project_id': 5},
        {'schedule_date': '2023-06-28 00:02:39', 'state': 'pending', 'amount': 2566, 'project_id': 10},
        {'schedule_date': '2023-06-07 03:31:51', 'state': 'pending', 'amount': 2372, 'project_id': 8},
        {'schedule_date': '2023-06-27 21:36:35', 'state': 'pending', 'amount': 3136, 'project_id': 9},
        {'schedule_date': '2023-06-06 09:25:13', 'state': 'pending', 'amount': 4790, 'project_id': 10},
        {'schedule_date': '2023-05-13 12:43:25', 'state': 'paid', 'amount': 1325, 'project_id': 6},~
        {'schedule_date': '2023-06-03 11:17:03', 'state': 'pending', 'amount': 4968, 'project_id': 6},
        {'schedule_date': '2023-06-14 18:14:42', 'state': 'pending', 'amount': 1146, 'project_id': 6},
        {'schedule_date': '2023-06-16 19:01:21', 'state': 'pending', 'amount': 2867, 'project_id': 5},
        {'schedule_date': '2023-05-18 10:25:36', 'state': 'paid', 'amount': 3202, 'project_id': 2},
        {'schedule_date': '2023-06-06 08:18:19', 'state': 'pending', 'amount': 3178, 'project_id': 9},
        {'schedule_date': '2023-06-27 12:15:20', 'state': 'pending', 'amount': 2833, 'project_id': 4},
        {'schedule_date': '2023-05-22 00:11:20', 'state': 'paid', 'amount': 3898, 'project_id': 10},
        {'schedule_date': '2023-06-23 10:05:15', 'state': 'pending', 'amount': 3331, 'project_id': 9},
        {'schedule_date': '2023-05-11 18:34:16', 'state': 'paid', 'amount': 4470, 'project_id': 9},
        {'schedule_date': '2023-06-13 17:01:57', 'state': 'pending', 'amount': 4120, 'project_id': 6},
        {'schedule_date': '2023-06-06 04:21:13', 'state': 'pending', 'amount': 3139, 'project_id': 4},
        {'schedule_date': '2023-06-29 08:43:53', 'state': 'pending', 'amount': 2702, 'project_id': 1},
        {'schedule_date': '2023-06-16 20:34:50', 'state': 'pending', 'amount': 2765, 'project_id': 2},
        {'schedule_date': '2023-05-21 18:34:02', 'state': 'paid', 'amount': 3978, 'project_id': 5},
        {'schedule_date': '2023-06-04 04:24:47', 'state': 'pending', 'amount': 3244, 'project_id': 1},
        {'schedule_date': '2023-04-30 22:13:01', 'state': 'paid', 'amount': 2876, 'project_id': 1},
        {'schedule_date': '2023-05-21 15:29:16', 'state': 'paid', 'amount': 2755, 'project_id': 5},
        {'schedule_date': '2023-06-26 08:52:11', 'state': 'pending', 'amount': 3259, 'project_id': 1},
        {'schedule_date': '2023-05-08 12:06:40', 'state': 'paid', 'amount': 2539, 'project_id': 6},
        {'schedule_date': '2023-06-28 02:18:23', 'state': 'pending', 'amount': 1927, 'project_id': 3},
        {'schedule_date': '2023-05-08 11:54:48', 'state': 'paid', 'amount': 4245, 'project_id': 8},
        {'schedule_date': '2023-05-16 09:34:52', 'state': 'paid', 'amount': 4131, 'project_id': 2},
        {'schedule_date': '2023-05-28 16:00:06', 'state': 'paid', 'amount': 2450, 'project_id': 1},
        {'schedule_date': '2023-06-30 11:32:38', 'state': 'pending', 'amount': 2859, 'project_id': 9},
        {'schedule_date': '2023-06-01 08:53:31', 'state': 'pending', 'amount': 3076, 'project_id': 9},
        {'schedule_date': '2023-06-13 20:56:26', 'state': 'pending', 'amount': 2700, 'project_id': 2},
        {'schedule_date': '2023-06-25 02:53:20', 'state': 'pending', 'amount': 3676, 'project_id': 1},
        {'schedule_date': '2023-05-13 00:50:20', 'state': 'paid', 'amount': 3132, 'project_id': 3},
        {'schedule_date': '2023-06-02 11:12:04', 'state': 'pending', 'amount': 2476, 'project_id': 8},
        {'schedule_date': '2023-05-13 15:33:27', 'state': 'paid', 'amount': 2117, 'project_id': 7},
        {'schedule_date': '2023-05-08 23:14:42', 'state': 'paid', 'amount': 4362, 'project_id': 1},
        {'schedule_date': '2023-05-05 11:52:10', 'state': 'paid', 'amount': 4937, 'project_id': 7},
        {'schedule_date': '2023-05-24 02:00:43', 'state': 'paid', 'amount': 4694, 'project_id': 10},
        {'schedule_date': '2023-06-11 21:30:46', 'state': 'pending', 'amount': 4014, 'project_id': 1},
        {'schedule_date': '2023-06-05 18:29:08', 'state': 'pending', 'amount': 1785, 'project_id': 5},
        {'schedule_date': '2023-05-01 00:24:09', 'state': 'paid', 'amount': 1841, 'project_id': 4},
        {'schedule_date': '2023-06-13 11:13:08', 'state': 'pending', 'amount': 1927, 'project_id': 6},
        {'schedule_date': '2023-05-28 07:17:47', 'state': 'paid', 'amount': 3920, 'project_id': 2},
        {'schedule_date': '2023-06-14 19:33:14', 'state': 'pending', 'amount': 2593, 'project_id': 5},
        {'schedule_date': '2023-05-07 17:24:58', 'state': 'paid', 'amount': 3106, 'project_id': 1},
        {'schedule_date': '2023-05-19 02:31:09', 'state': 'paid', 'amount': 3617, 'project_id': 5},
        {'schedule_date': '2023-06-28 00:50:26', 'state': 'pending', 'amount': 1950, 'project_id': 2},
        {'schedule_date': '2023-05-04 12:43:17', 'state': 'paid', 'amount': 4333, 'project_id': 2},
        {'schedule_date': '2023-06-17 23:12:53', 'state': 'pending', 'amount': 1878, 'project_id': 1}
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 4rem;
}

h1 {
  font-size: 3em;
  margin-bottom: 20px;
}
</style>
