<template>
  <div class="home">
    <div id="carouselExampleCaptions" class="carousel carousel-dark slide" data-bs-ride="carousel">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/60a976f203e0d49218fb90075ecfb494.Slide-2.jpg" class="d-block w-100" alt="...">
      <div class="carousel-caption">
        <h5>Medicare</h5>
      </div>
    </div>
    <div class="carousel-item">
      <img src="https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/8d7b1bde752f9448e5f51138bc453637.Slide-3.jpg" class="d-block w-100" alt="...">
      <div class="carousel-caption">
        <h5>Medication Therapy Management</h5>
      </div>
    </div>
    <div class="carousel-item">
      <img src="https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/6d1979b5b941f2a702b8e6ff057548ed.Slide-1.jpg" class="d-block w-100" alt="...">
      <div class="carousel-caption">
        <h5>Health</h5>
      </div>
    </div>
    <div class="carousel-item">
      <img src="https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/e884c74c2eadf9fe7482081ce45bccbb.Slide-4.jpg" class="d-block w-100" alt="...">
      <div class="carousel-caption">
        <h5>Life</h5>
      </div>
    </div>
  </div>
</div>
      <div class="d-flex justify-content-center my-2"><i class="bi bi-arrow-down down fs-3"></i></div>
    <div class="container">
      <div class="row d-flex justify-content-center">
        <div class="col-lg-8 col-md-12 col-sm-12 d-flex align-items-center">
          <div class="my-2 text-center">
            <h2 class="title-text fw-bolder fs-3">WELCOME TO HELPSTONE MEDICARE, MEDICATION THERAPY MANAGEMENT, HEALTH, LTC/LIFE</h2>
            <p class="subtitle-text">Insurance plans are supported on <strong class="highlight">HelpStone</strong>. We have a range of services and support for your personal wellbeing at no price! Call today for a no cost, no obligation Medicare Planning Review</p>
            <a class="btn btn-success br-15" href="tel:(872) 529-6804">Call Now<i class="bi-phone-vibrate ms-2"></i></a>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-2 py-5">
      <h2 class="text-center fw-bold">Products</h2>
          <p class="text-center pb-3">We specialize in helping people understand the rights and options they have with Medicare.</p>
        <div class="row row-cols-1 row-cols-md-4 g-4 mx-2">
          <div v-for="(service, s) in services" :key="s" class="col" :id="service.title">
            <div class="card br-15 h-100">
              <img :src="service.img" class="card-img-top br-15" alt="">
              <div class="card-body">
                <h5 class="card-title">{{service.title}}</h5>
                <p class="card-text">{{service.text}}</p>

              </div>
            </div>
          </div>
        </div> 
    </div>
    <div class="container py-5">
      <div class="row">
        <div class="col-md-8 mx-auto">
          <h2 class="text-center fw-bold">Contact Us Today</h2>
          <p class="text-center pb-3">Let us start helping you today for a no cost, no obligation Medicare Planning Review</p>
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
              <button class="btn btn-success br-15 px-3 float-end">Send<i class="bi-chevron-right ms-2"></i></button>
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
          img: 'https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/60a976f203e0d49218fb90075ecfb494.Slide-2.jpg',
          title: 'Medicare',
          text: 'A Medicare Supplement Insurance (Medigap) policy, sold by private companies, can help pay some of the health care costs that Original Medicare doesn’t, like co-payments, co-insurance, and deductibles.'
        },
        {
          img: 'https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/8d7b1bde752f9448e5f51138bc453637.Slide-3.jpg',
          title: 'Medication Therapy Management',
          text: 'Medication Therapy Management is a distinct service or group of services that optimize therapeutic outcomes for individual Medicare patients, provided by a licensed pharmacist'
        },
        {
          img: 'https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/6d1979b5b941f2a702b8e6ff057548ed.Slide-1.jpg',
          title: 'Health',
          text: 'Medicare health plans offered by private companies are plans that contracts with Medicare to provide all your Medicare and Medication Therapy Management benefits.'
        },
        {
          img: 'https://cdn-cepin.nitrocdn.com/rnNgBGqLqNeaHIQTmZxdsByxcthuuOtr/assets/static/optimized/wp-content/uploads/2020/05/e884c74c2eadf9fe7482081ce45bccbb.Slide-4.jpg',
          title: 'Life',
          text: 'We also offer health insurance plans (for under 65, marketplace, short term major medical) in addition to Term, Whole life, or Universal Life Insurance.'
        }
      ]
    }
  },
}
</script>
