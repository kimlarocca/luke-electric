<template>
  <div class="home">
    <content-card
      background="/images/home1.jpg"
      title="Worried about your electrical system overheating?"
      description="Talk to Luke, a local electrician in Hampton NJ or Clinton NJ about a panel upgrade"
      to="contact"
    />
    <div class="fancy-card">
      <div class="content">
        <h3>Let an Expert Handle Your Electrical System</h3>
        <v-spacer />
        <h5>Work with a local electrician in Hampton or Clinton, NJ</h5>
        <v-spacer size="triple" />
        <p>
          Do you need to
          <nuxt-link to="new-construction-electrical"
            >install wiring and appliances</nuxt-link
          >
          in a newly constructed property? Are you having issues with your
          home's electrical system? Whenever you need electrical services in
          Hampton or Clinton, NJ, turn to Luke Electric. We have over a decade
          of experience to pull from, so you can rest assured that your property
          is in good hands. As your local electrician, we can take care of
          important work like
          <nuxt-link to="panel-upgrades">replacing outdated panels</nuxt-link>
          or
          <nuxt-link to="electrical-repairs">fixing faulty outlets</nuxt-link>
          .
        </p>
        <v-spacer />
        <p>Contact us today to schedule electrical services.</p>
      </div>
    </div>
    <div class="fancy-grid">
      <div>
        <nuxt-link to="panel-upgrades">
          <img src="/images/panel-upgrades.jpg" alt="panel upgrades" />
          <div class="fancy-card-content">
            <h4>Panel Upgrades</h4>
            <v-spacer />
            <p>ELECTRICAL PANEL UPGRADES WILL MAKE YOUR ENTIRE SYSTEM SAFER.</p>
          </div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="new-construction-electrical">
          <img
            src="/images/new-construction-electrical.jpg"
            alt="panel upgrades"
          />
          <div class="fancy-card-content">
            <h4>New Construction</h4>
            <v-spacer />
            <p>
              A NEW CONSTRUCTION ELECTRICIAN CAN WORK ALONGSIDE YOUR
              CONSTRUCTION COMPANY.
            </p>
          </div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="electrical-repairs">
          <img src="/images/electrical-repairs.jpg" alt="panel upgrades" />
          <div class="fancy-card-content">
            <h4>Electrical Repairs</h4>
            <v-spacer />
            <p>
              COUNT ON US FOR FAST TROUBLESHOOTING AND ELECTRICAL REPAIR
              SERVICES.
            </p>
          </div>
        </nuxt-link>
      </div>
      <div>
        <nuxt-link to="outdoor-lighting">
          <img src="/images/outdoor-lighting.jpg" alt="panel upgrades" />
          <div class="fancy-card-content">
            <h4>Outdoor Lighting</h4>
            <v-spacer />
            <p>
              HIGHLIGHT LANDSCAPE FEATURES WITH AN OUTDOOR LIGHTING
              INSTALLATION.
            </p>
          </div>
        </nuxt-link>
      </div>
    </div>
    <content-card
      background="/images/home2.jpg"
      title="Brighten Up Your Property With New Lights"
      description="Pick us for outdoor lighting installations in Hampton NJ or Clinton NJ"
      to="ourdoor-lighting"
    />
    <div class="grid">
      <div class="image-fill">
        <img
          src="/images/light-bulbs.jpg"
          alt="luke electric new jersey electrician"
        />
      </div>
      <div class="padding">
        <h4>WHAT SETS US APART FROM OTHER ELECTRICIANS?</h4>
        <v-spacer />
        <p>
          You can count on us for excellent customer service at a great price.
          We're a preferred local electrician because:
        </p>
        <v-spacer />
        <ul>
          <li>Our owner is on every job site</li>
          <li>We educate our customers on our services</li>
          <li>We work carefully to avoid electrical hazards</li>
        </ul>
        <v-spacer />
        <p>
          We offer residential and commercial services. If you have any
          questions about our services, call us today at 908-246-8546. We look
          forward to working with you.
        </p>
      </div>
    </div>
    <content-card
      background="/images/home3.jpg"
      title="Outfit Your New Property With Electrical Equipment"
      description="WE CAN HANDLE A WIDE RANGE OF INSTALLATIONS"
      to="contact"
    />
  </div>
</template>

<script>
import ContentCard from '../components/ContentCard'

export default {
  name: 'Home',
  components: {
    ContentCard
  }
}
</script>
