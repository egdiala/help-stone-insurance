<template>
  <div id="app">
    <nav class="navbar navbar-fixed-top navbar-expand-lg navbar-light bg-white">
      <div class="container-fluid">
        <a class="navbar-brand" href="/">
          <img src="@/assets/logo.png" alt="" class="img-fluid" width="80" height="80">
          <strong class="title-text">HelpStone Insurance</strong>
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarText">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link" aria-current="page" href="tel:(872) 529-6804"><i class="bi-telephone-fill me-2 fs-5 highlight"></i>Call Now</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="mailto:helpersstone@gmail.com"><i class="bi-envelope-fill me-2 fs-5 highlight"></i>Email Us</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#"><i class="bi-camera-video-fill me-2 fs-5 highlight"></i>Remote Meeting</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <router-view></router-view>
    <!-- Footer -->
    <footer class="text-center text-lg-start bg-light text-muted">
      <section class="">
        <div class="container text-center text-md-start mt-5">
          <div class="row pt-3">
            <div class="col-md-5 col-lg-5 col-xl-5 mx-auto text-start mb-4">
              <h4 class="text-uppercase fw-bold mb-4">
                <img src="@/assets/logo.png" alt="" class="img-fluid" width="100" height="100">HelpStone Insurance
              </h4>
            </div>
            <div class="col-md-3 col-lg-3 col-xl-3 mx-auto text-start ps-4 mb-4">
              <h5 class="text-uppercase fw-bold mb-4">
                Services
              </h5>
              <p>
                <a href="#Medicare" class="text-reset">Medicare</a>
              </p>
              <p>
                <a href="#Health" class="text-reset">Health</a>
              </p>
              <p>
                <a href="#Life" class="text-reset">Life</a>
              </p>
              <p>
                <a href="#Medication Therapy Management" class="text-reset">Medication Therapy Management</a>
              </p>
            </div>
            <div class="col-md-3 col-lg-3 col-xl-3 mx-auto text-start ps-4 mb-4">
              <h5 class="text-uppercase fw-bold mb-4">
                Contact
              </h5>
              <p><i class="bi bi-geo-alt-fill me-2"></i> Kokomo, Indiana, US</p>
              <p>
                <a href="mailto:helpersstone@gmail.com" class="link"><i class="bi bi-envelope-fill me-2"></i>
                helpersstone@gmail.com</a>
              </p>
              <p><a href="tel:(872) 529-6804" class="link"><i class="bi bi-phone-fill me-2"></i>(872) 529-6804</a></p>
              <p><a href="https://www.facebook.com/Helpstone-Insurance-100615752229210/" target="_blank" class="link"><i class="bi bi-facebook me-2"></i>Help Stone Insurance</a></p>
            </div>
          </div>
        </div>
      </section>
      <div class="text-center p-4" style="background-color: rgba(0, 0, 0, 0.05);">
      Copyright © {{ new Date().getFullYear() }} HelpStone Insurance - All Rights Reserved.
      </div>
    </footer>
    <!-- Footer -->
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  }
}
</script>
