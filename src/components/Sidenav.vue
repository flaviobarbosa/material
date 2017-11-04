<template>
  <div>
      <md-toolbar>
    <md-button class="md-icon-button" @click="toggleLeftSidenav">
      <md-icon>menu</md-icon>
    </md-button>

    <h2 class="md-title">My App</h2>
  </md-toolbar>

  <md-sidenav class="md-left" ref="leftSidenav" @open="open('Left')" @close="close('Left')">
    <md-toolbar>
      <div class="md-toolbar-container">
        <h3 class="md-title" >Menu</h3>
        <md-layout md-align="end" md-gutter="16">
          <md-button class="md-icon-button " @click="closeLeftSidenav">
            <md-icon>clear</md-icon>
          </md-button>  
        </md-layout>
      </div>
    </md-toolbar>

    <md-list>
      <md-list-item>
        <md-button class="md-primary " @click="closeLeftSidenav">
            <md-icon>face</md-icon>
            <span>Perfil</span>
        </md-button>
      </md-list-item>

      <md-list-item>
        <md-icon>send</md-icon> <span>Sent Mail</span>
      </md-list-item>
    </md-list>
  </md-sidenav>

  <md-sidenav class="md-right" ref="rightSidenav" @open="open('Right')" @close="close('Right')">
    <md-toolbar>
      <div class="md-toolbar-container">
        <h3 class="md-title">Sidenav content</h3>
      </div>
    </md-toolbar>

    
  </md-sidenav>
  </div>
</template>

<script>
export default {
  name: "Sidenav",
  methods: {
    toggleLeftSidenav() {
      this.$refs.leftSidenav.toggle();
    },
    toggleRightSidenav() {
      this.$refs.rightSidenav.toggle();
    },
    closeLeftSidenav() {
      this.$refs.leftSidenav.close();
    },
    open(ref) {
      console.log("Opened: " + ref);
    },
    close(ref) {
      console.log("Closed: " + ref);
    }
  }
};
</script>
