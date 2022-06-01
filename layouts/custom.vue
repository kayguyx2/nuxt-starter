<template>
  <div class="min-h-screen flex flex-col justify-between">
    <div>
      <Header />
      <main class="container mx-auto my-5">
        <slot />
      </main>
    </div>
    <footer></footer>
  </div>
</template>
