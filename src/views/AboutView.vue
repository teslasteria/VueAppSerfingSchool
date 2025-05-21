<template>
 <!-- intro -->
 <section class="intro">
      <h1 class="main-title">About Us</h1>
    </section>

    <!-- nav -->
    <NavBar />

    <!-- about content -->
    <section class="about-content">
      <h2>Our Story</h2>
      <p id="takeText">
        Shell Surfing School was born in 2010 from a deep love for the ocean and
        a passion for sharing the thrill of surfing with the world. Founded by a
        group of seasoned surfers and ocean enthusiasts, our mission has always
        been to make surfing accessible, safe, and enjoyable for everyone,
        regardless of age or skill level.
      </p>
      <h3>Humble Beginnings</h3>
      <p>
        It all started on the sunny beaches of California, where our founders,
        Jake Thompson and Sarah Miller, spent their days riding waves and
        teaching friends how to surf. What began as informal lessons on the
        beach quickly grew into a small but dedicated community of surfers. Word
        spread about their unique teaching methods, which combined technical
        expertise with a fun, laid-back approach. Soon, they realized they could
        turn their passion into a business that would inspire others to connect
        with the ocean.
      </p>
      <h3>Building a Legacy</h3>
      <p>
        In 2012, Shell Surfing School officially opened its doors in Malibu,
        California. With just a handful of instructors and a few surfboards, we
        welcomed our first students. Our early days were filled with challenges,
        but our commitment to quality and safety helped us grow. By 2015, we had
        expanded to multiple locations along the West Coast, including San Diego
        and Santa Cruz.
      </p>
      <h3>Innovation and Growth</h3>
      <p>
        As the demand for surfing lessons grew, so did our vision. We introduced
        innovative programs like personalized coaching, group sessions, and even
        surf camps for kids. Our team of certified instructors grew, each
        bringing their unique expertise and love for the sport. We also
        partnered with top surfboard and wetsuit brands to provide our students
        with the best equipment available. In 2018, we launched our online
        platform, offering virtual lessons and surf tutorials. This allowed us
        to reach aspiring surfers worldwide, from the shores of Australia to the
        beaches of Europe. Our commitment to sustainability also became a core
        part of our mission. We started organizing beach cleanups and partnered
        with environmental organizations to protect the oceans we love.
      </p>
      <h3>A Global Community</h3>
      <p>
        Today, Shell Surfing School is more than just a business—it’s a global
        community of surfers united by a shared passion for the ocean. We’ve
        taught thousands of students, from complete beginners to advanced riders
        looking to refine their skills. Our alumni include competitive surfers,
        ocean advocates, and everyday people who simply love the thrill of
        catching a wave.
      </p>
      <h3>Our Philosophy</h3>
      <p>
        At Shell Surfing School, we believe surfing is more than just a
        sport—it’s a way of life. It’s about connecting with nature, challenging
        yourself, and finding joy in the simple act of riding a wave. Our
        instructors are not just teachers; they’re mentors who inspire
        confidence, respect for the ocean, and a sense of adventure.
      </p>
      <h3>Looking Ahead</h3>
      <p>
        As we look to the future, our goal is to continue spreading the stoke of
        surfing while staying true to our roots. We’re exploring new locations,
        developing eco-friendly surf gear, and creating programs that make
        surfing accessible to underserved communities. Whether you’re a
        first-timer or a seasoned pro, we invite you to join us on this
        incredible journey.
      </p>

      <img src="@/assets/img/pavel-neznanov-8Iil9NNZauk-unsplash.jpg" alt="About Us" />
    </section>
    <AppFooter />
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import AppFooter from '@/components/AppFooter.vue'
export default {
  name: 'AboutView',
  components: {
    NavBar,
    AppFooter
  }
}
</script>

<style scoped>
@import '@/assets/css/style.css';
@import '@/assets/css/about.css';
</style>