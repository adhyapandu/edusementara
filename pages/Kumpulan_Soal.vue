<template>
  <b-container fluid>
    <!-- User Interface controls -->
    

    <!-- Main table element -->
    <b-table
      show-empty
      small
      stacked="md"
      :items="items"
      :fields="fields"
      :current-page="currentPage"
      :per-page="perPage"
      :filter="filter"
      :filter-included-fields="filterOn"
      :sort-by.sync="sortBy"
      :sort-desc.sync="sortDesc"
      :sort-direction="sortDirection"
      @filtered="onFiltered"
    >

      <template #cell(actions)="row">
        <b-button size="sm" @click="info(row.item, row.index, $event.target)" class="mr-1">
          Download
        </b-button>
      </template>

      <template #row-details="row">
        <b-card>
          <ul>
            <li v-for="(value, key) in row.item" :key="key">{{ key }}: {{ value }}</li>
          </ul>
        </b-card>
      </template>
    </b-table>
    <b-row>
      

      <b-col sm="5" md="6" class="my-1">
        <b-form-group
          label="Per page"
          label-cols-sm="6"
          label-cols-md="4"
          label-cols-lg="3"
          label-align-sm="right"
          label-size="sm"
          label-for="perPageSelect"
          class="mb-0"
        >
          <b-form-select
            v-model="perPage"
            id="perPageSelect"
            size="sm"
            :options="pageOptions"
          ></b-form-select>
        </b-form-group>
      </b-col>

      <b-col sm="7" md="6" class="my-1">
        <b-pagination
          v-model="currentPage"
          :total-rows="totalRows"
          :per-page="perPage"
          align="fill"
          size="sm"
          class="my-0"
        ></b-pagination>
      </b-col>
    </b-row>

    
  </b-container>
</template>

<script>
  export default {
    data() {
      return {
        items: [
          { No: 1, MataPelajaran: 'Matematika', Deskripsi: 'Lorem ipsum dolor sit amet consectetur.' },
          { No: 2, MataPelajaran: 'Bahasa Indonesia', Deskripsi: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa, nemo?' },
          { No: 3, MataPelajaran: 'IPA', Deskripsi: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa, nemo?' },
          { No: 4, MataPelajaran: 'IPS', Deskripsi: 'Lorem ipsum dolor sit amet consectetur.' },
          { No: 5, MataPelajaran: 'IPS', Deskripsi: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa, nemo?' },
          { No: 6, MataPelajaran: 'Matematika', Deskripsi: 'Lorem ipsum dolor sit amet consectetur.' },
          { No: 7, MataPelajaran: 'PPKN', Deskripsi: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa, nemo?' },
          { No: 8, MataPelajaran: 'Matematika', Deskripsi: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsa, nemo?' },
          { No: 9, MataPelajaran: 'IPA', Deskripsi: 'Lorem ipsum dolor sit amet consectetur.' }
        ],
        fields: [
          { key: 'No', label: 'No', sortable: true },
          { key: 'MataPelajaran', label: 'MataPelajaran', sortable: true, sortDirection: 'desc' },
          { key: 'Deskripsi', label: 'Deskripsi' },
          { key: 'actions', label: 'Actions' }
        ],
        totalRows: 1,
        currentPage: 1,
        perPage: 5,
        pageOptions: [5, 10, 15, { value: 100, text: "Show a lot" }],
        sortBy: '',
        sortDesc: false,
        sortDirection: 'asc',
        filter: null,
        filterOn: [],
        infoModal: {
          id: 'info-modal',
          title: '',
          content: ''
        }
      }
    },
    computed: {
      sortOptions() {
        // Create an options list from our fields
        return this.fields
          .filter(f => f.sortable)
          .map(f => {
            return { text: f.label, value: f.key }
          })
      }
    },
    mounted() {
      // Set the initial number of items
      this.totalRows = this.items.length
    },
    methods: {
      info(item, index, button) {
        this.infoModal.title = `Row index: ${index}`
        this.infoModal.content = JSON.stringify(item, null, 2)
        this.$root.$emit('bv::show::modal', this.infoModal.id, button)
      },
      resetInfoModal() {
        this.infoModal.title = ''
        this.infoModal.content = ''
      },
      onFiltered(filteredItems) {
        // Trigger pagination to update the number of buttons/pages due to filtering
        this.totalRows = filteredItems.length
        this.currentPage = 1
      }
    }
  }
</script>