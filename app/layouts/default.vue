<script setup lang="ts">

</script>

<template>
  <div class="flex min-h-svh flex-col overflow-x-clip">
    <a
      href="#main-content"
      class="
        fixed top-4 left-4 z-50 -translate-y-24 rounded-md bg-background px-4
        py-2 text-sm font-medium shadow-lg
        focus:translate-y-0
        focus-visible:ring-2 focus-visible:ring-ring
      "
    >
      {{ $t('layouts.links.skip_to_content') }}
    </a>

    <!-- Header -->
    <header>
      <div
        class="
          fixed z-20 w-full border-b bg-background/80
          pt-[env(safe-area-inset-top)] text-foreground backdrop-blur-3xl
        "
      >
        <div class="mx-auto max-w-6xl px-6">
          <div
            class="
              flex items-center justify-between gap-6 py-3
              lg:py-4
            "
          />
        </div>
      </div>
    </header>

    <!-- Main Content -->
    <main
      id="main-content"
      class="flex flex-1 flex-col pt-[calc(5rem+env(safe-area-inset-top))]"
    >
      <slot />
    </main>

    <!-- Footer -->
    <footer
      class="
        border-t bg-background pt-8 pb-[calc(2rem+env(safe-area-inset-bottom))]
        text-foreground
      "
    >
      <div class="mx-auto max-w-6xl px-6">
        <div
          class="
            flex flex-col items-center gap-6 pt-2
            md:flex-row md:justify-between
          "
        />
      </div>
    </footer>
  </div>
</template>
