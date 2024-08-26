<template>
    <GuestLayout>
      <div class="event-list">
        <h1 class="title">Upcoming Events</h1>
        <ul class="events">
          <li v-for="event in events" :key="event.id" class="event">
            <div class="event-div">
              <span class="date">{{ event.date }}</span>
              <span class="name">{{ event.name }}</span>
            </div>
          </li>
        </ul>
      </div>
    </GuestLayout>
  </template>
  
  <script>
  import GuestLayout from '@/Layouts/GuestLayout.vue';
  
  export default {
    components: {
      GuestLayout,
    },
    data() {
      return {
        events: [
          { id: 1, name: 'Ice Cream Party', date: '2024-09-01' },
          { id: 2, name: 'Pajama Day', date: '2024-09-05' },
          { id: 3, name: 'Kite Festival', date: '2024-09-10' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .event-list {
    background-color: #e0f7fa;
    padding: 20px;
    border-radius: 15px;
    margin: 40px auto;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .title {
    font-family: 'Comic Sans MS', cursive, sans-serif;
    color: #007bb5;
    text-align: center;
    margin-bottom: 20px;
  }
  
  .events {
    list-style: none;
    padding: 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
  
  .event {
    background-color: #b3e5fc;
    margin: 10px;
    padding: 10px;
    border-radius: 10px;
    font-family: 'Comic Sans MS', cursive, sans-serif;
    color: #01579b;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    flex-basis: calc(33.333% - 20px);
  }
  
  .event-div {
    height: 100px;
    width: 100%;
    text-align: center;
  }
  
  .event .date {
    font-weight: bold;
    color: #0288d1;
    display: block;
  }
  
  .event .name {
    color: #01579b;
    display: block;
    margin-top: 5px;
  }
  </style>
  