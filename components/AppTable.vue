<template>
    <DataTable :value="data" sortMode="multiple" tableStyle="min-width: 50rem; border: 1px solid black">
        <Column field="code" header="Code" sortable style="width: 50px"></Column>
        <Column field="name" header="Name" sortable style="width: 25%"></Column>
        <Column field="description" header="Description" sortable style="width: 25%"></Column>
        <Column field="type" header="Type" sortable style="width: 100px"></Column>
        <Column field="created" header="Created" sortable style="width: 25%"></Column>
        <Column field="lastUpdated" header="Last Updated" sortable style="width: 25%"></Column>
        <Column field="status" header="Status" sortable style="width: 25%"></Column>
    </DataTable>
</template>

<script setup>
import { ref } from 'vue';
import DataTable from 'primevue/datatable';
import Column from 'primevue/column';

const data = ref([
  {
    "code": "DRE",
    "name": "Alice Green",
    "description": "Complete Diabetic Retinal Examination",
    "type": "Assessment",
    "created": "7/1/2024 by Emily Clark",
    "lastUpdated": "7/5/2024 by Michael Stone",
    "status": "Active"
  },
  {
    "code": "A1C",
    "name": "Liam White",
    "description": "Blood Sugar Level Test (A1C)",
    "type": "Assessment",
    "created": "7/2/2024 by Emily Clark",
    "lastUpdated": "7/6/2024 by Sarah King",
    "status": "Active"
  },
  {
    "code": "HRA",
    "name": "Olivia Adams",
    "description": "Health Risk Assessment Call",
    "type": "Outreach",
    "created": "7/3/2024 by Emily Clark",
    "lastUpdated": "7/7/2024 by Michael Stone",
    "status": "Active"
  },
  {
    "code": "WEL",
    "name": "Daniel Harris",
    "description": "Welcome Phone Call",
    "type": "Outreach",
    "created": "7/4/2024 by Emily Clark",
    "lastUpdated": "7/8/2024 by Sarah King",
    "status": "Active"
  },
  {
    "code": "BKR",
    "name": "Megan Taylor",
    "description": "Gentle Back Rub Therapy",
    "type": "Service Only",
    "created": "7/5/2024 by Emily Clark",
    "lastUpdated": "7/9/2024 by Michael Stone",
    "status": "Inactive"
  },
  {
    "code": "HAE",
    "name": "Sophia Lee",
    "description": "Comprehensive Health Assessment Evaluation",
    "type": "Assessment",
    "created": "7/6/2024 by Emily Clark",
    "lastUpdated": "7/10/2024 by Sarah King",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Lucas Perez",
    "description": "Lorem ipsum dolor sit amet",
    "type": "Service Only",
    "created": "Lorem ipsum dolor",
    "lastUpdated": "Lorem ipsum dolor",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Charlotte Thomas",
    "description": "Lorem ipsum dolor sit amet",
    "type": "Service Only",
    "created": "Lorem ipsum dolor",
    "lastUpdated": "Lorem ipsum dolor",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Ethan Roberts",
    "description": "Lorem ipsum dolor sit amet",
    "type": "Service Only",
    "created": "Lorem ipsum dolor",
    "lastUpdated": "Lorem ipsum dolor",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Isabella Jackson",
    "description": "Lorem ipsum dolor sit amet",
    "type": "Service Only",
    "created": "Lorem ipsum dolor",
    "lastUpdated": "Lorem ipsum dolor",
    "status": "Active"
  }
]);

</script>
