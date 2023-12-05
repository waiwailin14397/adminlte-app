<script setup>
//------------------------------------------------
// Import Section
//------------------------------------------------
// import packages
import { ref, shallowReactive } from "vue";

import { defineComponent } from "vue";

import Tab1 from "../components/Tab1.vue";
import Tab2 from "../components/Tab2.vue";
import Tab3 from "../components/Tab3.vue";


const activeTab = ref('m001c');
const tabs = [
  {key: 'tab1', name: ' 1.Tab1 '},
  {key: 'tab2', name: ' 2.Tab2 '},
  {key: 'tab3', name: ' 3.Tab3 '},
]

const currentTabComponent = shallowReactive({
  tab1: Tab1,
  tab2: Tab2,
  tab3: Tab3
})





//------------------------------------------------
// private fanction
//------------------------------------------------
// Tab Click Action
const tabClick = (tab) => {
  activeTab.value = tab;
  currentTabComponent.value = tab;
}


</script>

<template>
  <!-- Content Wrapper. Contains page content -->
  <div class="content-wrapper">
    <!-- Content Header (Page header) -->
    <section class="content-header">
      <div class="container-fluid">
        <div class="row mb-2">
          <div class="col-sm-6">
            <h1><i class="fas fa-edit"></i> My Tab </h1>
          </div>
        </div>
      </div>
      <!-- /.container-fluid -->
    </section>

    <!-- Main content -->
    <section class="content">

      <!-- content list box -->
      <div class="container-fluid">
        <div class="card card-warning card-tabs">
          <!-- card-header -->
          <div class="card-header p-0 pt-1">
            <!-- tabs -->
            <ul class="nav nav-tabs" id="custom-tabs-one-tab" role="tablist">
              <li v-for="tab in tabs"
                  :key="tab.key"
                  :class="[{ 'active': activeTab === tab.key }, 'nav-link']"
                  @click="tabClick(tab.key)">
                  {{tab.name}}
              </li>
            </ul>
          </div>
          <!-- /.card-header -->

          <div class="card-body">
            <!-- 内容部分 -->
            <div class="tab-content">
              <!-- <keep-alive> -->
                <component :is="currentTabComponent[activeTab]" />
              <!-- </keep-alive> -->
            </div>
            <!-- /.tab-content -->
          </div>
          <!-- /.card-body -->

        </div>
        <!-- /.card -->
      </div>
      <!-- /.container-fluid -->

    </section>
    <!-- /.content -->
  </div>
  <!-- /.content-wrapper -->
</template>

<style>
/* */
</style>
