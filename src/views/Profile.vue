<template>
  <v-container class="main-container" fill-height>
    <v-toolbar class="toolbar">
      <v-toolbar-title class="toolbar-title">
        Noteshare
        <v-toolbar-subtitle class="toolbar-caption">
          Sharing Knowledge worldwide
        </v-toolbar-subtitle>
      </v-toolbar-title>
    </v-toolbar>
    <v-row align="center" justify="center" class="fill-height">
      <v-col cols="12" md="8" lg="6">
        <v-card class="center-card">
          <v-card-title>
            <h2>Share Only Verified Materials to avoid Barn</h2>
          </v-card-title>
          <v-card-subtitle>
            By doing this you'll receive 10 points which can be used for Unlimited Downloads and Sharing
          </v-card-subtitle>
          <v-card-text>
            <p>Upload page</p>
          </v-card-text>
          <v-divider></v-divider>
          <v-card-actions>
            <v-chip class="status-chip">Upload</v-chip>
            <v-chip class="status-chip">Details</v-chip>
            <v-chip class="status-chip">Done</v-chip>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
.main-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  padding-top: 90px;
}

.toolbar {
  width: 100%;
  height: 90px;
  background-color: #bec3df;
  position: fixed;
  top: 0;
}

.toolbar-title {
  text-align: left;
}

.toolbar-caption {
  display: block;
  font-size: 14px;
  color: #5f6368;
  margin-top: 4px;
}

.center-card {
  padding: 20px;
  text-align: center;
}

.status-chip {
  margin-right: 8px;
}
</style>
