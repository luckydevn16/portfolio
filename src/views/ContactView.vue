<template>
  <section class="contact-section" id="contact">
    <div class="container">
      <h2 class="section-heading">Contact</h2>
      <div class="contact-wrapper">
        <div class="contact-wrapper-column">
          <ContactSet />
        </div>
        <div class="contact-animation-column">
          <ContactAnimation />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ContactSet from '@/components/ContactSet.vue';
import ContactAnimation from '@/components/ContactAnimation.vue';

export default {
  name: 'contact',
  components: {
    ContactSet,
    ContactAnimation
  }
}
</script>

<style>
.contact-section .section-heading {
  color: var(--contact-color);
}

.contact-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.contact-wrapper-column,
.contact-animation-column {
  width: 49%;
}

.contact-animation-column {
  position: relative;
  height: 100%;
  min-height: 32rem;
}

@media (max-width: 991.98px) {
  .contact-wrapper {
    flex-direction: column;
  }

  .contact-wrapper-column,
  .contact-animation-column {
    width: 100%;
  }
}</style>