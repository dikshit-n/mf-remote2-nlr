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
    "name": "John Doe",
    "description": "Diabetic Retinal Exam",
    "type": "Assessment",
    "created": "6/6/2024 by Kurtis Segars",
    "lastUpdated": "6/8/2024 by Stephanie Pham",
    "status": "Active"
  },
  {
    "code": "A1C",
    "name": "Jane Smith",
    "description": "A1C Blood Test",
    "type": "Assessment",
    "created": "6/6/2024 by Kurtis Segars",
    "lastUpdated": "6/7/2024 by Meghan Tooher",
    "status": "Active"
  },
  {
    "code": "HRA",
    "name": "Michael Johnson",
    "description": "HRA Call",
    "type": "Outreach",
    "created": "6/6/2024 by Kurtis Segars",
    "lastUpdated": "6/6/2024 by Kurtis Segars",
    "status": "Active"
  },
  {
    "code": "WEL",
    "name": "Emily Davis",
    "description": "Welcome Call",
    "type": "Outreach",
    "created": "6/6/2024 by Kurtis Segars",
    "lastUpdated": "6/7/2024 by Kurtis Segars",
    "status": "Active"
  },
  {
    "code": "BKR",
    "name": "David Brown",
    "description": "Back Rub",
    "type": "Service Only",
    "created": "6/6/2024 by Kurtis Segars",
    "lastUpdated": "6/6/2024 by Kurtis Segars",
    "status": "Inactive"
  },
  {
    "code": "HAE",
    "name": "Sarah Wilson",
    "description": "Health Assessment Evaluation",
    "type": "Assessment",
    "created": "6/6/2024 by Kurtis Segars",
    "lastUpdated": "6/6/2024 by Kurtis Segars",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "James Miller",
    "description": "Lorem ipsum",
    "type": "Service Only",
    "created": "Lorem ipsum",
    "lastUpdated": "Lorem ipsum",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Patricia Garcia",
    "description": "Lorem ipsum",
    "type": "Service Only",
    "created": "Lorem ipsum",
    "lastUpdated": "Lorem ipsum",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Robert Martinez",
    "description": "Lorem ipsum",
    "type": "Service Only",
    "created": "Lorem ipsum",
    "lastUpdated": "Lorem ipsum",
    "status": "Active"
  },
  {
    "code": "LMP",
    "name": "Linda Hernandez",
    "description": "Lorem ipsum",
    "type": "Service Only",
    "created": "Lorem ipsum",
    "lastUpdated": "Lorem ipsum",
    "status": "Active"
  }
]);

</script>
