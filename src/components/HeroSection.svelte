<script lang="ts">
  import Logo from "../assets/Logo.svelte";

  const handleScroll = () => {
    const meinElement = document.getElementById("card")!;
    meinElement.style.transform = `rotateY(${window.scrollY * 0.04}deg)`;
  };
</script>

<svelte:window on:scroll={handleScroll} />

<section>
  <div class="card h-dvh flex flex-col gap-4 p-8" id="card">
    <header class="flex justify-between">
      <Logo size={80} />
      <div class="w-14 h-14 bg-gray-600"></div>
    </header>
  </div>
</section>

<style>
  section {
    perspective: 1500px;
  }

  .card {
    background: radial-gradient(
      circle at 75% 55%,
      white,
      rgb(217, 217, 217),
      rgb(217, 217, 217)
    );
  }
</style>
