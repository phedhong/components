<script lang="ts">
  import { ComponentChildren } from "preact";
  import { children } from "solid-js";

  type Props = {
    children: ComponentChildren;
  };

  const menus = [
      {
        title: "Documentation",
        children: [
          { name: "Getting Started", href: "#" },
          { name: "Guide", href: "#" },
          { name: "API", href: "#" },
          { name: "Showcase", href: "#" },
          { name: "Pricing", href: "#" },
        ],
      },
      {
        title: "Community",
        children: [
          { name: "Forum", href: "#" },
          { name: "Discord", href: "#" },
        ],
      },
    ];

  const currentYear = new Date().getFullYear();

</script>

<footer>  
    <div class="flex flex-col md:flex-row w-full max-w-screen-lg gap-8 md:gap-16 text-sm">
      <div class="flex-1 space-y-2">
        <div class="flex items-center gap-1">
          <div class="font-bold text-2xl">
            Footer
          </div>
        </div>
        <div class="text-gray-500">
          Full Stack Framework
        </div>
        <div class="text-gray-500">
            Copyright © 2020 DenoLand<br />
            All right reserved.
          <a
            href="https://github.com/denoland/fresh"
            class="inline-block hover:text-black"
          >
          </a>
        </div>
      </div>

      {#each menus as item}
        
        <div key={item.title}>
          <div class="font-bold">{item.title}</div>
          <ul class="mt-2">

            {#each item.children as child}

              <li class="mt-2" key={child.name}>
                <a
                  class="text-gray-500 hover:text-gray-700"
                  href={child.href}
                >
                  {child.name}
                </a>
              </li>
              {/each}
          </ul>
        </div>

      {/each}

    </div>
</footer>






