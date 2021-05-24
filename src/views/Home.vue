<template>
  <div class="home">
    <div class="container">
      <div class="row d-flex justify-content-between">
        <div class="col-lg-5 col-md-12 col-sm-12 ps-4 d-flex align-items-center">
          <div class="my-2">
            <h2 class="title-text fw-bolder fs-2">Instantly schedule<br> appointments with Doctors.</h2>
            <p class="subtitle-text">Insurance plans are supported on <strong class="highlight">Help Stone</strong>. We have a range of services and support for your personal wellbeing at no price! Just call or email for free consultation.</p>
            <a class="btn btn-success br-15" href="tel:(872) 529-6804">Contact us<i class="bi-phone-vibrate ms-2"></i></a>
          </div>
        </div>
        <div class="col-lg-6 col-md-12 col-sm-12 my-2">
          <div id="carouselExampleFade" class="carousel slide carousel-fade px-3" data-bs-ride="carousel">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80" alt="" class="d-block w-100 br-15">
              </div>
              <div class="carousel-item">
                <img src="https://images.unsplash.com/photo-1542884748-2b87b36c6b90?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=750&q=80" class="d-block w-100 br-15" alt="">
              </div>
              <div class="carousel-item">
                <img src="https://images.unsplash.com/photo-1576765974497-b41831d52f83?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=757&q=80" class="d-block w-100 br-15" alt="...">
              </div>
            </div>
            <button class="carousel-control-prev ps-3" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next pe-3" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="visually-hidden">Next</span>
            </button>
          </div>
        </div>
      </div>
      <div class="d-flex justify-content-center my-2"><i class="bi bi-arrow-down down fs-3"></i></div>
      
    </div>
    <div class="bg-2 py-5">
      <h2 class="text-center fw-bold pb-3">Our Services</h2>
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2 g-4">
          <div v-for="(service, s) in services" :key="s" class="col" :id="service.title">
            <div class="card br-15 h-100">
              <img :src="service.img" class="card-img-top br-15" alt="" height="300">
              <div class="card-body">
                <h5 class="card-title">{{service.title}}</h5>
                <p class="card-text">{{service.text}}</p>
              </div>
            </div>
          </div>
        </div>
      </div>      
    </div>
    <div class="container py-5">
      <div class="row">
        <div class="col-md-8 mx-auto">
          <h2 class="text-center fw-bold pb-3">Schedule an appointment</h2>
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
            <div class="col-md-6">
              <input type="text" name="phone" class="form-control" placeholder="Phone" required>
            </div>
            <div class="col-md-6">
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
          img: 'https://images.unsplash.com/photo-1601582037073-b36af0b8ea81?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          title: 'Medicare',
          text: 'A Medicare Supplement Insurance (Medigap) policy, sold by private companies, can help pay some of the health care costs that Original Medicare doesn’t, like co-payments, co-insurance, and deductibles.'
        },
        {
          img: 'https://images.unsplash.com/photo-1612277795054-a7a98257dd6d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          title: 'Health',
          text: 'We provide all round checkup for you to ensure you are in a complete healthy consdition.'
        },
        {
          img: 'https://images.unsplash.com/photo-1587854692152-cbe660dbde88?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          title: 'Medication Therapy Management',
          text: 'We offer medication therapy management for Medicare recipients. This adds drug coverage to the Original Medicare plan.'
        },
        {
          img: 'https://images.unsplash.com/photo-1554331292-735256644d5f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=755&q=80',
          title: 'Life',
          text: 'We also offer health insurance plans (for under 65, marketplace, short term major medical) in addition to Term, Whole life, or Universal Life Insurance.'
        }
      ]
    }
  },
}
</script>
