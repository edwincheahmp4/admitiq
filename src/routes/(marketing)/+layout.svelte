<script lang="ts">
  import { WebsiteName } from "./../../config"
  import "../../app.css"

  interface Props {
    children?: import("svelte").Snippet
  }

  let { children }: Props = $props()
</script>

<div class="navbar bg-base-100 mx-auto shadow-md">
  <div class="flex-1">
    <a class="btn btn-ghost normal-case text-xl" href="/">{WebsiteName}</a>
  </div>
  <div class="flex-none">
    <ul class="menu menu-horizontal px-1 hidden sm:flex font-bold text-lg">
      <li class="md:mx-4">
        <!-- 
  <a
    href="https://github.com/CriticalMoments/CMSaasStarter"
    class="border border-primary">★ us on Github</a>
-->

      </li>
      <li class="md:mx-2">
        <a href="/#why-help" on:click|preventDefault={() => { document.getElementById('why-help')?.scrollIntoView({ behavior: 'smooth' }); }}>
          Mission
        </a>
      </li>
      <li class="md:mx-2"><a href="/#services" on:click|preventDefault={() => { document.getElementById('services')?.scrollIntoView({ behavior: 'smooth' }); }}>
          Services
        </a></li>
      <li class="md:mx-2">
        <a href="/#free-guides" on:click|preventDefault={() => { document.getElementById('free-guides')?.scrollIntoView({ behavior: 'smooth' }); }}>
          Free Guide
        </a>
      </li>
      <li class="md:mx-0">
      </li>
    </ul>
    <div class="dropdown dropdown-end sm:hidden">
      <!-- svelte-ignore a11y_label_has_associated_control -->
      <!-- svelte-ignore a11y_no_noninteractive_tabindex -->
      <label tabindex="0" class="btn btn-ghost btn-circle">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          ><path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h7"
          /></svg
        >
      </label>
      <!-- svelte-ignore a11y_no_noninteractive_tabindex -->
      <ul
        tabindex="0"
        class="menu menu-lg dropdown-content mt-3 z-1 p-2 shadow-sm bg-base-100 rounded-box w-52 font-bold"
      >
        <li>
          <a href="/#why-help" on:click|preventDefault={() => { document.getElementById('why-help')?.scrollIntoView({ behavior: 'smooth' }); }}>
            Mission
          </a>
        </li>
        <li>
          <a href="/#services" on:click|preventDefault={() => { document.getElementById('services')?.scrollIntoView({ behavior: 'smooth' }); }}>
            Services
          </a>
        </li>
        <li>
          <a href="/#free-guides" on:click|preventDefault={() => { document.getElementById('free-guides')?.scrollIntoView({ behavior: 'smooth' }); }}>
            Free Guides
          </a>
        </li>
      </ul>
    </div>
  </div>
</div>

<div class="">
  {@render children?.()}
</div>

<!-- Spacer grows so the footer can be at bottom on short pages -->
<div class="grow"></div>
<div class="">
  <div class="border-t max-w-[1000px] mx-auto"></div>
  <footer
    class="footer md:footer-horizontal p-10 gap-x-48 lg:gap-x-64 xl:gap-x-96 place-content-center text-base"
  >
    <div class="w-full flex flex-col items-center text-center">
      <div class="text-md text-[#2d174d] opacity-60 mb-2">
        AdmitIQ | Initiative by Edwin Cheah, a 45 IB perfect scorer and full-ride student at Wesleyan University.
      </div>
      <div class="flex flex-col sm:flex-row gap-3 items-center justify-center text-[#2d174d] mt-2">
        <a href="https://wa.me/6586875399" class="flex items-center gap-2 link link-hover text-primary" target="_blank" rel="noopener">
          <svg class="w-5 h-5" viewBox="0 0 32 32"><path d="M16.003 2.667c-7.364 0-13.333 5.969-13.333 13.333 0 2.354.627 4.646 1.814 6.662l-1.922 7.031a1.333 1.333 0 0 0 1.625 1.625l7.031-1.922a13.26 13.26 0 0 0 6.785 1.833h.001c7.364 0 13.333-5.969 13.333-13.333s-5.969-13.333-13.334-13.333zm0 24c-2.063 0-4.09-.537-5.857-1.553a1.333 1.333 0 0 0-.885-.137l-5.57 1.523 1.523-5.57a1.333 1.333 0 0 0-.137-.885c-1.016-1.767-1.553-3.794-1.553-5.857 0-6.065 4.936-11 11-11s11 4.935 11 11-4.935 11-11 11zm6.09-7.41c-.334-.167-1.978-.978-2.285-1.09-.307-.112-.531-.167-.755.167-.223.334-.862 1.09-1.057 1.313-.195.223-.39.251-.724.084-.334-.167-1.409-.519-2.687-1.653-.993-.885-1.664-1.977-1.861-2.311-.195-.334-.021-.513.146-.68.15-.149.334-.39.501-.584.167-.195.223-.334.334-.557.112-.223.056-.418-.028-.585-.084-.167-.755-1.823-1.034-2.495-.272-.654-.548-.564-.755-.574l-.643-.011c-.223 0-.584.084-.89.418-.306.334-1.172 1.146-1.172 2.797 0 1.651 1.199 3.247 1.366 3.472.167.223 2.36 3.605 5.715 4.914.799.345 1.422.551 1.908.705.803.256 1.534.22 2.112.134.644-.096 1.978-.808 2.259-1.588.279-.779.279-1.447.195-1.588-.084-.14-.306-.223-.64-.39z"/></svg>
          Whatsapp: +65 8687 5399
        </a>
        <a href="mailto:echeah@wesleyan.edu" class="flex items-center gap-2 link link-hover text-primary">
          <svg class="w-5 h-5" viewBox="0 0 24 24"><path d="M20 4H4C2.897 4 2 4.897 2 6v12c0 1.103.897 2 2 2h16c1.103 0 2-.897 2-2V6c0-1.103-.897-2-2-2zm0 2v.511l-8 6.222-8-6.222V6h16zM4 20v-9.489l7.445 5.794a1 1 0 0 0 1.11 0L20 10.511V20H4z"/></svg>
          Email: echeah@wesleyan.edu
        </a>
      </div>
    </div>
  </footer>
</div>
