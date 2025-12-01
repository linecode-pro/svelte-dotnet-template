<script lang="ts">
  import { page } from '$app/state';

  let props = $props();
  let { href, class: className, children } = props;

  // pathname как реактивное значение
  const pathname = $derived(page.url.pathname);

  // класс на основе текущего pathname
  const activeClass = $derived(href === pathname ? 'active' : '');
</script>

<a class="{className} {activeClass}" href={href}>
  {@render children()}
</a>
