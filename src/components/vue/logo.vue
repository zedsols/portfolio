<script setup lang='ts'>
import gsap from "gsap";
import { useEffect, useStore } from "~/hooks/core.vue";
import { isMenuOpenStore } from "~/stores/menu";

const LOGO = "zedsols";

const isMenuOpen = useStore(isMenuOpenStore);

useEffect(() => {
	const logoTL = gsap.timeline({ defaults: { stagger: 0.15 } });

	logoTL.fromTo("#logo > span", { opacity: 0 }, { opacity: 1 });

	const letterSpanArray: HTMLElement[] = gsap.utils.toArray("#logo > span");

	for (const letter of letterSpanArray) {
		letter.addEventListener("mouseenter", () => {
			letter.classList.add("neonText");
			letter.previousElementSibling?.classList.add("neonText");
			letter.nextElementSibling?.classList.add("neonText");
		});
		letter.addEventListener("mouseleave", () => {
			letter.classList.remove("neonText");
			letter.previousElementSibling?.classList.remove("neonText");
			letter.nextElementSibling?.classList.remove("neonText");
		});
	}
});
</script>

<template>
  <a id="logo" class="lg:mb-10 lg:-mx-12 lg:-rotate-90 font-medium text-xl" href="/" @click="() => {
  isMenuOpen.value = false
}">
    <span class="opacity-0 transition-all" v-for="letter in LOGO.split('')">
      {{ `${letter} ` }}
    </span>
    <span class="opacity-0 transition-all font-bold text-3xl text-[#fe4164]">
      .
    </span>
  </a>
</template>