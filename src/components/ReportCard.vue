<!-- 
Component name: ReportCard
use: to display information on the organization in the report page.
props: dataprop {logo, org_name, description, link}
-->

<template>
   <div color="cyan-lighten-5">
        <div>
            <a-row class="align-center justify-center">
                <a-col xs="12" sm="12" md="5" lg="3">
                    <a-avatar
                    class="ma-4"
                    size="200"
                    rounded="0">
                        <v-img :src="dataprop.logo"></v-img>
                    </a-avatar>
                </a-col>
                <a-col xs="12" sm="12" md="7" lg="9">
                    <div>
                        {{dataprop.org_name}}
                    </div>
                    <div>
                        {{dataprop.description}}
                    </div>
                    <a :href="dataprop.link" target="_blank">
                        <v-btn  class="ms-2" color="success" on-hover>
                            visit site
                        </v-btn>
                    </a> 
                </a-col>
            </a-row>
        </div>
    </div> 
</template>

<script setup>
    const props = defineProps({
        dataprop:{
            type:Object
        }
    })

</script>