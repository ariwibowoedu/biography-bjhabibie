<script setup>
import { ref } from "vue";

const profile = {
  name: "B.J. Habibie",
  role: "Bapak Teknologi Indonesia.",
};
const timeline = [
  { year: 1936, event: "Born in Parepare. Indonesia" },
  {
    year: 1965,
    event:
      "Pursued higher education in engineering. from Bandung Institute of Technology (ITB). then specialized in aerospace engineering in Germany.",
  },
  {
    year: 1974,
    event:
      "Returned to Indonesia and was tasked by President Soeharto with building the nation's advanced technology sector.",
  },
  {
    year: 1978,
    event:
      "Served as the Minister of Research and Technology, where he played a key role in advancing Indonesia's technological capabilities.",
  },
  {
    year: 1998,
    event: "Became the third President of Indonesia.",
  },
  {
    year: 2019,
    event:
      "Died on September 11, 2019, leaving behind a legacy of technological advancement and national development.",
  },
];
</script>

<template class="max-w-4xl mx-auto flex flex-col items-center justify-center bg-white shadow-lg overflow-hidden">
  <header
    class="w-full text-center p-10 bg-gradient-to-r from-slate-800 to-gray-700 text-white"
  >
    <h1 class="text-4xl font-extrabold mb-2">{{ profile.name }}</h1>
    <p class="text-lg font-medium italic">{{ profile.role }}</p>
  </header>
  <main class="p-8 space-y-8">
    <figure class="flex flex-col items-center text-center">
      <img
        class="rounded-xl shadow-md mb-4 border"
        width="200"
        src="/images/b.j.habibie.jpg"
        alt="presiden soekarno"
      />
      <figcaption class="text-sm text-gray-400">
        Oleh Office of the Vice PresidentThe Republic of Indonesia -
        <a
          rel="nofollow"
          class="external free"
          href="https://www.wapresri.go.id/zoobicon/2015/09/DDI_5965.jpg"
          >https://www.wapresri.go.id/zoobicon/2015/09/DDI_5965.jpg</a
        >, Domain Publik,
        <a href="https://commons.wikimedia.org/w/index.php?curid=73334378"
          >Pranala</a
        >
      </figcaption>
    </figure>
    <section id="tribute-info">
      <h2 class="text-2xl font-bold text-center mb-6">
        Time Line of {{ profile.name }}
      </h2>
      <ul
        class="space-y-4 border-l-4 border-red-500 pl-6 max-w-2xl mx-auto text-justify"
      >
        <li v-for="item in timeline" :key="item.year">
          <span class="font-bold">{{ item.year }}</span> - {{ item.event }}
        </li>
      </ul>
    </section>
    <footer class="text-center pt-6 border-t mt-6">
      <p class="text-gray-500 text-bold font-medium">
        Read more his story on
        <a
          href="https://id.wikipedia.org/wiki/B.j.habibie"
          target="_blank"
          class="text-blue-400 hover:underline"
          >Wikipedia</a
        >.
      </p>
      <p class="text-gray-400 text-md font-light">
        Made with ❤️ . by
        <a
          class="hover:underline"
          href="https://ariwibowoedu.github.io/portofolio-v6"
          target="_blank"
        >
          ariwibowoedu.github.io
        </a>
      </p>
    </footer>
  </main>
</template>


