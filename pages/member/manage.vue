<template>
  <div class="page-container">
      <div class="header">
          <h3>Members Management</h3>
          <div class="actions">
              <IconField>
                  <InputIcon class="pi pi-search" />
                  <InputText size="small" placeholder="Search" />
              </IconField>
              <Button size='small' icon="pi pi-plus" iconPos="right" label="Create Member" />
          </div>
      </div>
      <div class="body">
          <AppTable />
      </div>
  </div>
</template>

<script setup lang="ts">
import Button from 'primevue/button';
import InputText from 'primevue/inputtext';
import IconField from 'primevue/iconfield';
import InputIcon from 'primevue/inputicon';
import AppTable from '@/components/AppTable.vue';
definePageMeta({
  layout: 'base'
})
</script>

<style scoped lang="scss">
.page-container {
  display: flex;
  flex: 1;
  flex-direction: column;
  .header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 5px 10px;
      .actions {
          display: flex;
          align-items: center;
          justify-content: center;
          gap: 10px;
      } 
  }
  .body {
      max-height: 100%;
      overflow: auto;
  }
}
</style>