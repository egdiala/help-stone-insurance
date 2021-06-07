<template>
<div class="mb-50">
  <h1 class="text-center fs-4 fw-bold">PRODUCT AND SERVICES</h1>
  <section>
    <div class="container">
      <div v-for="(service, s) in services" :key="s" :id="s" class="row">
        <div class="col-md-6 mt-3">
          <img :src="require(`@/assets/img/${service.img}`)" class="img-thumbnail" alt="">
        </div>
        <div class="col-md-6 fs-5 mt-3">
          <h1 class="text-center fw-bold fs-2">{{service.title}}</h1>
          {{service.text}}
          <ul v-if="s == 0" class="">
            <li v-for="(care, c) in cares" :key="c" :id="`c${c}`">
              <div class="ms-2 fs-5 me-auto">
                <div class="fs-4 fw-bold">{{care.title}}</div>
                {{care.subtitle}}
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data() {
    return {
      services: [
        {
          img: 'medicare.jpeg',
          title: 'Medicare',
          text: 'Medicare is a federal medical expense insurance program for people age 65 and older even if the individual continues to work. Medicare benefits are also available to anyone, regardless off age, who has been entitled to Social Security disability income benefits for 2 years or has a permanent kidney failure (End Stage Renal Disease - ESRD)'
        },
        {
          img: 'mtm.jpeg',
          title: 'Medication Therapy Management',
          text: 'Medication Therapy Management is a distinct service or group of services that optimize therapeutic outcomes for individual Medicare patients, provided by a licensed pharmacist.'
        },
        {
          img: 'health.jpeg',
          title: 'Health',
          text: 'We also offer health insurance plans (for under 65), marketplace, short term, hospital indemnity, critical illness, cancer, dental and vision insurance, major medical.'
        },
        {
          img: 'life.jpeg',
          title: 'Long Term Care/Life Insurance',
          text: 'Long-term care (LTC) is a range of services and support for your personal care needs. Most long-term care isn’t medical care. Instead, most long-term care is help with basic personal tasks of everyday life like bathing, dressing, and using the bathroom, sometimes called activities of daily living. Medicare doesn’t cover long-term care (also known as custodial care) if that’s the only care you need. Most nursing home care is custodial care. You pay 100% for non-covered services, including most long-term care in addition to Term, Whole Life, or Universal Life Insurance. We can help you plan for that time.'
        },
      ],
      cares: [
        {
          title: 'Medicare Supplement',
          subtitle: 'Medicare Supplement plans, referred to as Medigap, are policies issued by private insurance companies that are designed to fill in some of the gaps in Medicare. Medicare Supplement policies pay some or all of Medicare’s deductibles and copayments.'
        },
        {
          title: 'Medicare Part D',
          subtitle: 'Medicare Part D adds Prescription drug benefit to Original Medicare, via a stand-alone Part D plan, or comes incorporated into a Medicare Part C ‘Advantage’ plan. It is an optional coverage through private prescription plans that contract with Medicare'
        },
        {
          title: 'Medicare Advantage Part C',
          subtitle: 'Medicare Advantage Plans are a type of Medicare health plan offered by a private company that contracts with Medicare to provide all your Part A and Part B benefits. Most Medicare Advantage Plans also offer prescription drug coverage. If you’re enrolled in a Medicare Advantage Plan, most Medicare services are covered through the plan. Your Medicare services aren’t paid for by Original Medicare.'
        },
      ]
    }
  },
}
</script>

<style scoped>

</style>