<template>
  <q-page padding>
    <q-card>
      <q-card-section>
        <div class="text-h5">Popis svih knjiga</div>
      </q-card-section>
      <q-card-section>
        <q-table
          :rows="allBooks"
          :columns="columns"
          row-key="id"
          flat
        />
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script>
export default {
  setup() {
    const allBooks = [
    { id: 1, title: 'Čudnovate zgode šegrta Hlapića', author: 'Ivana Brlić-Mažuranić' },
    { id: 1, title: 'Kiklop', author: 'Ranko Marinković' },
    { id: 2, title: 'Glembajevi', author: 'Miroslav Krleža' }, 
    { id: 3, title: 'Mali princ', author: 'Antoine de Saint-Exupéry' },
    { id: 4, title: 'U registraturi', author: 'Ante Kovačić' },
    { id: 5, title: 'Metastaze', author: 'Alen Bović' }
    ];

    const columns = [
      { name: 'id', label: 'ID', field: 'id', align: 'left' },
      { name: 'title', label: 'Naslov', field: 'title', align: 'left' },
      { name: 'author', label: 'Autor', field: 'author', align: 'left' },
    ];

    return {
      allBooks,
      columns,
    };
  },
};
</script>