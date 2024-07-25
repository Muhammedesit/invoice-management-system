<template>
  <div>
    <h3>Fatura Listesi</h3>
    <table>
      <thead>
        <tr>
          <th>Fatura No</th>
          <th>Müşteri</th>
          <th>Tarih</th>
          <th>Tutar</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="invoice in invoices" :key="invoice.id">
          <td>{{ invoice.invoiceNumber }}</td>
          <td>{{ invoice.customer }}</td>
          <td>{{ invoice.date }}</td>
          <td>{{ invoice.amount }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'InvoiceList',
  data() {
    return {
      invoices: [
        { id: 1, invoiceNumber: 'INV-001', customer: 'Müşteri 1', date: '2023-07-01', amount: 1000 },
        { id: 2, invoiceNumber: 'INV-002', customer: 'Müşteri 2', date: '2023-07-02', amount: 1500 },
        { id: 3, invoiceNumber: 'INV-003', customer: 'Müşteri 3', date: '2023-07-03', amount: 2000 }
      ]
    }
  }
}
</script>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
}

th, td {
  padding: 8px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}
</style>