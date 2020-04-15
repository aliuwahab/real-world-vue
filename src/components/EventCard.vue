<template>
    <div class="event-card -shadow">
    <span> @{{ event.time }} on {{event.date}}</span>
    <h4 class="title"> {{ event.title}}</h4>
    <span>{{ event.attendees.length}}</span>
    </div>
</template>

<script>
export default {
    data() {
        return {
      event: {
                id: 1,
                title: 'Sample Event Title ',
                date: 'Wednesday April, 2020',
                time: '6:00',
                attendees:[
                    {id: '12345', name: 'Gbeila Aliu Wahab'},
                    {id: '12344', name: 'Nyusung Faiq Aliu'},
                ]
            }
        }
    },

}
</script>

<style scoped>
    .event-card {
      padding: 20px;
      margin-bottom: 24px;
      transition: all 0.2s linear;
      cursor: pointer;
    }
    .event-card:hover {
      transform: scale(1.01);
      box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
    }
    .event-card > .title {
      margin: 0;
    }
    
    .event-link {
      color: black;
      text-decoration: none;
      font-weight: 100;
    }
</style>
