<template>
  <q-layout view="lHh Lpr lFf">
    <q-header style="background: #2a9d8f" elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
        <q-toolbar-title style="font-family: 'Lora', serif">
          FIMEBOT
        </q-toolbar-title>
        <q-btn
          flat
          dense
          icon="smart_toy"
          @click="rightDrawerOpen = !rightDrawerOpen"
        />
        
      </q-toolbar>

    </q-header>
  <q-drawer       side="right"
 v-model="rightDrawerOpen" >
  <!-- <iframe  class="chatbot" src='https://webchat.botframework.com/embed/chatBotFime2?s=LrMIZIMOuXA.Qy1TpPFb5Q7XUUFPIE8oQwQAFMlEcoQWuG_SHPtqUAk' ></iframe> -->
<iframe   class="chatbot" src='https://webchat.botframework.com/embed/fimeBot?s=0D_EHcq1wSk.9biUO75vk6NgUrWoCIjjvqWsfBfk9s7kxvdh7EU9tzY'></iframe>  </q-drawer>
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      side="left"
      content-class="navs-color"
      :width="220"
      style="font-family: 'Lora', serif"
    >

      <q-list bordered separator >
        <q-item-label header style="color: white"> Menu </q-item-label>

        <!-- <q-list bordered separator> -->
        <q-item class="text-grey-2" exact clickable v-ripple to="/">
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>Inicio</q-item-section>
        </q-item>
        <q-item class="text-grey-2" exact clickable v-ripple to="/chatbot">
          <q-item-section avatar>
            <q-icon name="smart_toy" />
          </q-item-section>
          <q-item-section>Chat bot</q-item-section>
        </q-item>
        <q-item class="text-grey-2" exact clickable v-ripple to="/aboutus">
          <q-item-section avatar>
            <q-icon name="contact_support" />
          </q-item-section>
          <q-item-section>About us</q-item-section>
        </q-item>
        <!-- <q-item
          class="text-grey-2"
          exact
          clickable
          v-ripple
          to="/credits"
        >
          <q-item-section avatar>
            <q-icon name="connect_without_contact " />
          </q-item-section>
          <q-item-section>Agradecimineto</q-item-section>
        </q-item> -->
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: "MainLayout",
  data() {
    return {
      leftDrawerOpen: false,
      rightDrawerOpen:false,
    };
  },
};
</script>


<style >
.navs-color {
  background-color: #2a9d8f;
}
.text-grey-2 {
  color: white !important;
}

.chatbot{
  width: 100%;
  height: 100%;
   min-height: 40em;
}
.chatWindows{
  width: 100%;
  height: 100%;
  margin-left: 3rem;
}
</style>