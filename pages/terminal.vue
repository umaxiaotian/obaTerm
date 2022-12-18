<template>
    <div id="pageDashboard">
      <v-card>
    <v-tabs
      v-model="tab"
      background-color="primary"
      dark
    >
      <v-tab
        v-for="item in items"
        :key="item.tab"
      >
        {{ item.tab }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item in items"
        :key="item.tab"
      >
        <v-card flat>
          <v-card-text>{{ item.content }}</v-card-text>
          <console />
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
 
    </div>
  </template>
  
  <script>
    import API from '@/api';
    import console from '@/components/console';
    export default {
      layout: 'dashboard',
      components: {
        console
      },
      data () {
      return {
        tab: null,
        items: [
                { tab: 'server1', content: 'server1 Content' },
                { tab: 'server2', content: 'Tab 2 Content' },
                { tab: 'server3', content: 'Tab 3 Content' },
                { tab: 'server4', content: 'Tab 4 Content' },
                { tab: 'server5', content: 'Tab 5 Content' },
                { tab: 'server6', content: 'Tab 6 Content' },
                { tab: 'server7', content: 'Tab 7 Content' },
                { tab: 'server8', content: 'Tab 8 Content' },
                { tab: 'server9', content: 'Tab 9 Content' },
                { tab: 'server10', content: 'Tab 10 Content' },
            ],
      }
    },
    };
  </script>
  