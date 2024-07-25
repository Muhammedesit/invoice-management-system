<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="invoices-page">
    <h2>Faturalar</h2>
    <InvoiceList />
    <InvoiceForm />
  </div>
</template>

<script>
import InvoiceList from '@/components/InvoiceList.vue'
import InvoiceForm from '@/components/InvoiceForm.vue'

export default {
  name: 'InvoicesPage',
  components: {
    InvoiceList,
    InvoiceForm
  }
}
</script>