<template>
  <div>
    <h2>{{ $data.PaymentTitle }}</h2>
    <h4>{{ $data.PaymentBrief }}</h4>
    <div class="p-field">
      <label for="email">Email</label>
      <InputText
        id="email"
        class="p-inputtext-sm"
        type="email"
        aria-describedby="email-help"
      />
    </div>
    <div class="p-field">
      <label for="CardDetails">Card Number</label>
      <InputText
        id="CardDetails"
        class="p-inputtext-sm"
        type="CardDetails"
        aria-describedby="CardDetails-help"
      />
      <label>Expiry Date</label>
      <InputMask placeholder="mm/dd/yyyy" mask="mm/dd/yyyy" />
    </div>
    <div class="p-field">
      <label for="CardHolderName">Card Holder Name</label>
      <InputText
        id="CardHolderName"
        class="p-inputtext-sm"
        type="CardHolderName"
        aria-describedby="CardHolderName-help"
      />
    </div>
    <div class="p-field">
      <Dropdown
        v-model="selectedCity"
        :options="cities"
        optionLabel="name"
        placeholder="Select a City"
      />
      <div>
        <label for="zipocode">Zipcode</label>
        <InputNumber
          id="zipocode"
          class="p-inputtext-sm"
          mode="decimal"
          :useGrouping="false"
        />
        <label for="email">State</label>
        <InputText id="email" type="email" aria-describedby="email-help" />
      </div>
    </div>
    <Button
      label="Pay $43.99"
      class="p-text-center p-button-rounded p-button-help"
    />
  </div>
</template>

<script>
export default {
  data: () => ({
    PaymentTitle: "Payment Details",
    PaymentBrief: "Complete you purchase by providing your payment details.",
    selectedCity: "New York",
    cities: [
      { name: "New York", code: "NY" },
      { name: "Rome", code: "RM" },
      { name: "London", code: "LDN" },
      { name: "Istanbul", code: "IST" },
      { name: "Paris", code: "PRS" },
    ],
  }),
  name: "FormHolder",
};
</script>

<style scoped>
.p-field * {
  display: block;
}
</style>
