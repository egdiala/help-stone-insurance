<template>
  <div class="home mb-50">
    <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="3" aria-label="Slide 4"></button>
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="@/assets/img/medicare.jpeg" class="d-block w-100">
      <div class="carousel-caption mb-4">
        <h1>Medicare</h1>
      </div>
    </div>
    <div class="carousel-item">
      <img src="@/assets/img/mtm.jpeg" class="d-block w-100">    
        <div class="carousel-caption mb-4">
          <h1>Medication Therapy Management</h1>
        </div>
    </div>
    <div class="carousel-item">
      <img src="@/assets/img/health.jpeg" class="d-block w-100">
      <div class="carousel-caption mb-4">
        <h1>Health</h1>
      </div>
    </div>
    <div class="carousel-item">
      <img src="@/assets/img/life.jpeg" class="d-block w-100">
      <div class="carousel-caption mb-4">
        <h1>Life</h1>
      </div>
    </div>
  </div>
</div>
      <div class="d-flex justify-content-center my-2"><i class="bi bi-arrow-down down fs-3"></i></div>
    <div class="container">
      <div class="row d-flex justify-content-center">
        <div class="col-lg-8 col-md-12 col-sm-12 d-flex align-items-center">
          <div class="my-2 text-center">
            <h2 class="title-text fw-bolder fs-3">WELCOME TO HELPSTONE INSURANCE</h2>
            <p class="fs-5">We have a range of services and support for your personal wellbeing at no cost to you! We provide Medicare, Health, and Life insurance solutions also Medication Therapy Management services. Call today for a no cost, no obligation Medicare Planning Review.</p>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-2 py-5">
      <h2 class="text-center fw-bold">Product and Services</h2>
          <p class="text-center fs-5 pb-3">We specialize in helping people understand the rights and options they have with Medicare.</p>
        <div class="row row-cols-1 row-cols-md-4 g-4 mx-2">
          <div v-for="(service, s) in services" :key="s" class="col" :id="service.title">
            <div class="card br-15 h-100">
              <img :src="require(`@/assets/img/${service.img}`)" class="card-img-top br-15" alt="">
              <div class="card-body">
                <h3 class="card-title fw-bolder">{{service.title}}</h3>
                <p class="card-text fs-5" v-text="str(service.text)"></p>
              </div>
                <div class="text-end card-footer bg-white"><a :href="`/services/#${s}`" class="btn btn-sm btn-outline-primary">Learn more</a></div>
            </div>
          </div>
        </div> 
    </div>
    <div class="container py-5">
      <div class="row">
        <div class="col-md-8 mx-auto">
          <h2 class="text-center fw-bold">Contact Us Today</h2>
          <p class="text-center fs-5 pb-3">Let us start helping you today for a no cost, no obligation Medicare Planning Review</p>
          <form name="contact"
              method="POST"
              data-netlify="true"
              data-netlify-honeypot="bot-field" class="row g-3">
              <input type="hidden" name="form-name" value="contact" />
            <div class="col-md-6">
              <input type="text" name="name" class="form-control" placeholder="Name" required>
            </div>
            <div class="col-md-6">
              <input type="email" name="email" class="form-control" placeholder="Email" required>
            </div>
            <div class="col-md-5">
              <input type="text" name="phone" class="form-control" placeholder="Phone" required>
            </div>
            <div class="col-md-2">
              <input type="text" name="age" class="form-control" placeholder="Age" required>
            </div>
            <div class="col-md-5">
              <select name="service" class="form-select" id="autoSizingSelect" required>
                <option value="Medicare">Medicare</option>
                <option value="Health">Health</option>
                <option value="Life">Life</option>
                <option value="Medication Therapy Management">Medication Therapy Management</option>
              </select>
            </div>
            <div class="col-md-12">
              <textarea name="message" class="form-control" placeholder="Leave a message here" rows="5"></textarea>
            </div>
            <div class="d-grid gap-2 col-md-6 mx-auto">
              <button class="btn btn-success br-15 px-3 fs-5 float-end">Send<i class="bi-chevron-right ms-2"></i></button>
            </div>
          </form>
        </div>
      </div>
    </div>
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
          text: 'We also offer health insurance plans (for under 65), marketplace, short term and major medical.'
        },
        {
          img: 'life.jpeg',
          title: 'Long Term Care/Life Insurance',
          text: 'Long-term care (LTC) is a range of services and support for your personal care needs. Most long-term care isn’t medical care. Instead, most long-term care is help with basic personal tasks of everyday life like bathing, dressing, and using the bathroom, sometimes called activities of daily living. Medicare doesn’t cover long-term care (also known as custodial care) if that’s the only care you need. Most nursing home care is custodial care. You pay 100% for non-covered services, including most long-term care. We can help you plan for that time. We also offer health insurance plans (for under 65, marketplace, short term major medical) in addition to Term, Whole life, or Universal Life Insurance.'
        },
      ]
    }
  },
  methods: {
    str(line) {
      var words = line.split(" ");
      if (words.length > 20) {
        let elips = ["..."]
        return words.slice(0, 20).concat(elips).join(" ");
      } else {
        return words.slice(0, 20).join(" ");
      }
      
    }
  }
}
</script>
