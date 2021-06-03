<template>
    <div class="mb-50">
        <div class="container">
            <div class="row">
                <h3 class="fw-bolder">REMOTE MEETING</h3>
                <p class="fs-5">
<strong class="fs-4">Doing Business During COVID-19:</strong> During the Coronavirus pandemic, we are happy to accommodate any client who wishes to meet remotely vs. “in-person”. At our clients request, we are able to pick up any essential documents (fax them, or leave them outside and we will pickup) and conduct most business over the phone, or by remote meeting.</p>
            </div>
            <hr class="px-5">
            <div class="row">
                <h3 class="fw-bolder">DURING THESE DIFFICULT TIMES, WE MAKE IT EASY TO CONNECT!</h3>
                <p class="fs-5">Please choose your preferred method to contact us below:</p>
                <div class="col">
                <ol class="list-group mb-4">
                    <li class="list-group-item d-flex justify-content-between align-items-start">
                        <div class="ms-2 fs-5 me-auto">
                        <div class="fs-4 fw-bold">CALL OR EMAIL US NOW</div>
                        Contact us at your convenience. If you’re calling during our normal hours and get our voicemail, leave the best time to call you back and we will call you back, usually within an hour or less!
                        <p>
                        <a href="mailto:helpersstone@gmail.com" class="highlight"><i class="bi bi-envelope-fill me-2"></i>
                EMAIL US: helpersstone@gmail.com</a></p>
              <p><a href="tel:(872) 529-6804" class="highlight"><i class="bi bi-phone-fill me-2"></i>(872) 529-6804</a></p>
                        </div>
                    </li>
                    <li class="list-group-item d-flex justify-content-between align-items-start">
                        <div class="ms-2 fs-5 me-auto">
                        <div class="fs-4 fw-bold">SCHEDULE A VIDEO CALL</div>
                        If you want to setup a time to chat via a Zoom Meeting, Skype Call or Facebook Messenger Call please fill the form below to pick a time to meet via any preferred platform of your choice.
                        </div>
                    </li>
                </ol>
                        <form name="schedule"
                            method="POST"
                            data-netlify="true"
                            data-netlify-honeypot="bot-field" class="row g-3">
                            <input type="hidden" name="form-name" value="schedule" />
                            <div class="col-md-6">
                            <label for="name">Name</label>
                            <input type="text" name="name" class="form-control" placeholder="Name" required>
                            </div>
                            <div class="col-md-6">
                            <label for="email">Email</label>
                            <input type="email" name="email" class="form-control" placeholder="Email" required>
                            </div>
                            <div class="col-md-6">
                            <label for="phone">Phone</label>
                            <input type="text" name="phone" class="form-control" placeholder="Phone" required>
                            </div>
                            <div class="col-md-6">
                            <label for="service">Service</label>
                            <select name="service" class="form-select" id="autoSizingSelect" required>
                                <option value="Medicare">Medicare</option>
                                <option value="Health">Health</option>
                                <option value="Life">Life</option>
                                <option value="Medication Therapy Management">Medication Therapy Management</option>
                            </select>
                            </div>
                            <div class="col-md-4">
                            <label for="platform">Social Platform</label>
                            <select name="platform" class="form-select" id="autoSizingSelect" required>
                                <option value="Zoom">Zoom</option>
                                <option value="Skype">Skype</option>
                                <option value="Facebook Messenger">Facebook Messenger</option>
                            </select>
                            </div>
                            <div class="col-md-4">
                            <label for="date">Date</label>
                            <input type="date" name="date" class="form-control" required>
                            </div>
                            <div class="col-md-4">
                            <label for="age">Age</label>
                            <input type="text" name="age" class="form-control" placeholder="Age" required>
                            </div>
                            <div class="col-md-12">
                            <label for="message">Message</label>
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