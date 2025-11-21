<script lang="ts">
  const startDate = new Date("August 20, 2016 00:20:18");
  const endDate = new Date();
  const diffYears = endDate.getFullYear() - startDate.getFullYear();
</script>

<section
  class="relative z-10 flex flex-col items-center justify-between max-w-7xl mx-auto my-16 px-4 lg:flex-row lg:my-[15vh] gap-12"
>
  <!-- Left Side: Name -->
  <div class="w-full lg:w-1/2 text-center lg:text-left">
    <h1
      class="font-sans font-black tracking-tighter leading-none text-6xl sm:text-8xl lg:text-9xl bg-clip-text text-transparent bg-gradient-to-r from-gray-900 to-gray-600 dark:from-white dark:to-gray-400"
    >
      Camran<br />Ahmad
    </h1>
  </div>

  <!-- Right Side: About Me -->
  <div class="w-full lg:w-1/2 max-w-xl">
    <div
      class="p-6 rounded-2xl bg-white/5 backdrop-blur-sm border border-white/10 shadow-xl"
    >
      <p
        class="text-lg sm:text-xl leading-relaxed text-gray-700 dark:text-gray-300 font-medium"
      >
        I am a software developer with {diffYears} years of experience specializing
        in
        <span class="text-blue-600 dark:text-blue-400 font-bold"
          >AEM, Java, and JavaScript</span
        >. My work focuses on building stable, scalable, and maintainable
        digital solutions that support both user experience and long-term
        business needs. I have experience developing new features, improving
        existing systems, and collaborating across teams to deliver consistent,
        high-quality results. In my free time, I spend time with my family and
        enjoy playing
        <span class="text-green-600 dark:text-green-400 font-bold"
          >disc golf and Magic: The Gathering</span
        >.
      </p>
    </div>
  </div>
</section>
