<template>
  <div class="dashboard">
    <v-subheader class="d-flex justify-space-between align-center">
        <h3>Dashboard</h3>
        <v-btn color="success">
            View Orders
        </v-btn>
    </v-subheader>
    <v-row>
        <v-col lg="7" cols="12">
            <v-alert
                dense
                text
                type="success"
            >
                <strong>Login Successfully</strong>
                Good Morning
            </v-alert>

            <v-row>
                <v-col lg="6" cols="12" v-for="(item, i) in activities" :key="i">
                    <v-card
                        elevation="2"
                        class="rounded-lg"
                    >
                        <v-card-text class="d-flex justify-space-between align-center">
                            <div>
                                <strong>{{item.title}}</strong> <br>
                                <small>Last 2 weeks</small>
                            </div>
                            <v-avatar :color="item.color" size="60">
                                <span class="white--text">{{item.amount}}</span>
                            </v-avatar>
                        </v-card-text>
                    </v-card>
                </v-col>
            </v-row>
        </v-col>

        <v-col lg="5" cols="12">
            <v-card>
                <v-card-title>
                    Activities
                </v-card-title>
                <v-timeline
                    align-top
                    dense
                >
                    <v-timeline-item
                    color="pink"
                    small
                    >
                    <v-row class="pt-1">
                        <v-col>
                        <strong>10 minutes ago</strong>
                        <div class="text-caption">
                            Dot Numpang
                        </div>
                        </v-col>
                    </v-row>
                    </v-timeline-item>

                    <v-timeline-item
                    color="teal lighten-3"
                    small
                    >
                    <v-row class="pt-1">
                        <v-col>
                        <strong>50 minutes ago</strong>
                        <div class="text-caption mb-2">
                            Play game
                        </div>
                        </v-col>
                    </v-row>
                    </v-timeline-item>

                    <v-timeline-item
                    color="blue"
                    small
                    >
                    <v-row class="pt-1">
                        <v-col>
                        <strong>3 hours ago</strong>
                        <div class="text-caption">
                            Eating
                        </div>
                        </v-col>
                    </v-row>
                    </v-timeline-item>

                    <v-timeline-item
                    color="green"
                    small
                    >
                    <v-row class="pt-1">
                        <v-col>
                        <strong>10 hours ago</strong>
                        <div class="text-caption">
                            Watch Football
                        </div>
                        </v-col>
                    </v-row>
                    </v-timeline-item>
                </v-timeline>
            </v-card>
        </v-col>
    </v-row>

    <v-row>
        <v-col cols="12">
            <v-data-table
                caption="Recent Orders"
                :headers="headers"
                :items="desserts"
                :items-per-page="5"
                class="elevation-1"
            >
                <template
                    v-slot:item.action>
                    <v-btn
                        color="success"
                    >
                        View
                    </v-btn>
                </template>
            </v-data-table>
        </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
    data() {
        return {
            activities: [
                { title: "Total Products", color: "red", amount: 4505},
                { title: "Total Categories", color: "blue", amount: 3000},
                { title: "Total Orders", color: "green", amount: 5005},
                { title: "Total Pending Orders", color: "yellow", amount: 105},
                { title: "Total Cancel Orders", color: "cyan", amount: 10},
                { title: "Total Users", color: "orange", amount: 5}
            ],
            headers: [
                {
                    text: 'Dessert (100g serving)',
                    align: 'start',
                    sortable: false,
                    value: 'name',
                },
                { text: 'Calories', value: 'calories' },
                { text: 'Fat (g)', value: 'fat' },
                { text: 'Carbs (g)', value: 'carbs' },
                { text: 'Protein (g)', value: 'protein' },
                { text: 'Action', value: 'action' },
            ],
            desserts: [
                {
                    name: 'Frozen Yogurt',
                    calories: 159,
                    fat: 6.0,
                    carbs: 24,
                    protein: 4.0,
                    iron: '1%',
                },
                {
                    name: 'Ice cream sandwich',
                    calories: 237,
                    fat: 9.0,
                    carbs: 37,
                    protein: 4.3,
                    iron: '1%',
                },
                {
                    name: 'Eclair',
                    calories: 262,
                    fat: 16.0,
                    carbs: 23,
                    protein: 6.0,
                    iron: '7%',
                },
                {
                    name: 'Cupcake',
                    calories: 305,
                    fat: 3.7,
                    carbs: 67,
                    protein: 4.3,
                    iron: '8%',
                },
                {
                    name: 'Gingerbread',
                    calories: 356,
                    fat: 16.0,
                    carbs: 49,
                    protein: 3.9,
                    iron: '16%',
                },
                {
                    name: 'Jelly bean',
                    calories: 375,
                    fat: 0.0,
                    carbs: 94,
                    protein: 0.0,
                    iron: '0%',
                },
                {
                    name: 'Lollipop',
                    calories: 392,
                    fat: 0.2,
                    carbs: 98,
                    protein: 0,
                    iron: '2%',
                },
                {
                    name: 'Honeycomb',
                    calories: 408,
                    fat: 3.2,
                    carbs: 87,
                    protein: 6.5,
                    iron: '45%',
                },
                {
                    name: 'Donut',
                    calories: 452,
                    fat: 25.0,
                    carbs: 51,
                    protein: 4.9,
                    iron: '22%',
                },
                {
                    name: 'KitKat',
                    calories: 518,
                    fat: 26.0,
                    carbs: 65,
                    protein: 7,
                    iron: '6%',
                },
            ],
        }
    }
}
</script>

<style>

</style>