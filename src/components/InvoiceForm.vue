<template>
  <div>
    <h3>Yeni Fatura Oluştur</h3>
    <form @submit.prevent="submitForm">
      <div>
        <label for="invoiceNumber">Fatura No:</label>
        <input type="text" id="invoiceNumber" v-model="invoiceNumber" required>
      </div>
      <div>
        <label for="customer">Müşteri:</label>
        <input type="text" id="customer" v-model="customer" required>
      </div>
      <div>
        <label for="date">Tarih:</label>
        <input type="date" id="date" v-model="date" required>
      </div>
      <div>
        <label for="amount">Tutar:</label>
        <input type="number" id="amount" v-model="amount" required>
      </div>
      <button type="submit">Fatura Oluştur</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'InvoiceForm',
  data() {
    return {
      invoiceNumber: '',
      customer: '',
      date: '',
      amount: 0
    }
  },
  methods: {
    submitForm() {
      // Formdan alınan verileri kullanarak yeni bir fatura oluştur
      const newInvoice = {
        invoiceNumber: this.invoiceNumber,
        customer: this.customer,
        date: this.date,
        amount: this.amount
      }
      
      // Fatura verilerini sunucuya gönder veya başka bir işlem yap
      console.log('Yeni fatura oluşturuldu:', newInvoice)
      
      // Formu sıfırla
      this.resetForm()
    },
    resetForm() {
      this.invoiceNumber = ''
      this.customer = ''
      this.date = ''
      this.amount = 0
    }
  }
}
</script>

<style scoped>
form {
  margin-top: 20px;
}

div {
  margin-bottom: 10px;
}

label {
  display: block;
  font-weight: bold;
}

input[type="text"],
input[type="date"],
input[type="number"] {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button[type="submit"] {
  padding: 8px 16px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>