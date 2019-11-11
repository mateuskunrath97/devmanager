<template>
    <v-card class="mx-auto" height="100vh" width="256">
        <v-navigation-drawer class="deep-purple accent-4" dark permanent>
            <v-list>
                <v-list-item v-for="item in items" :key="item.title" link>
                    <v-list-item-icon>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                        <v-list-item-title class="text-menu-padding-left">{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>

            <template v-slot:append>
                <div class="pa-2">
                    <v-btn block>Logout</v-btn>
                </div>
            </template>
        </v-navigation-drawer>
    </v-card>
</template>

<script>
	export default {
		name: "Menu",
		data () {
            return {
                user: {
                    name: 'Mateus Kunrath',
                    email: 'mateus.kunrath@devmind.com',
                    theme: 'dark'
                },
                drawer: true,
                items: [
                    { title: 'Dashboard', icon: 'mdi-view-dashboard' },
                    { title: 'Projetos', icon: 'mdi-folder' },
                    { title: 'Equipe', icon: 'mdi-account-group-outline' },
                ],
                mini: true,
            }
        },
	};
</script>

<style scoped>
    * {
        font-family: 'Roboto', Tahoma, Geneva, Verdana, sans-serif;
    }

    .text-menu-padding-left {
        padding-left: 20px;
    }

    .page-height {
        height: 100vh;
    }

    .menu-padding {
        padding: 10px;
    }

    .menu-padding-2 {
        padding: 20px;
    }
</style>