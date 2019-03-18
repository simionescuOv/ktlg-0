<template>
    <nav>
        <v-toolbar app
            class="blue lighten-4"
        >
            <v-toolbar-side-icon class="red--text"
                        @click='sertar = !sertar'
            ></v-toolbar-side-icon>
            <v-toolbar-title class="purple--text">
                ceamaiaplicatieever
            </v-toolbar-title>
        </v-toolbar>

        <v-navigation-drawer app 
                v-model="sertar"
                class="red lighten-4"
        >
            <v-list>
                <v-list-tile v-for='linc in lincuriMeniu' 
                              :key='linc.textu'
                              router
                              :to='linc.cararea'
                >
                    <v-list-tile-action>
                        <v-icon class="white black--text  "

                        >{{linc.iconu}}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title 
                            class="white green--text"

                        >{{linc.textu}}</v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>  
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>
<script>
export default {
    data (){
        return {
            sertar: false,
            lincuriMeniu: [
                {iconu:'assignment', textu:'Catalog', cararea:'ktlog'},
                {iconu:'home', textu:'Acasica unde-i cald si e papica', cararea:'/'},
                {iconu:'polymer', textu:'Despre', cararea:'/about'}
            ]
        }
    }
}
</script>

