<script lang='ts'>
import { ArrowDownLeftIcon } from "lucide-svelte";
import { Logo } from "~/components/svelte";
</script>

<footer class="pt-16 px-16 border-t border-gray-7 grid grid-rows-[auto_1fr_auto] grid-cols-4">
  <div class="col-span-full self-end">
    <Logo class="mb-16 font-medium text-5xl" />
  </div>
  <div class="col-span-2 self-start hidden lg:grid justify-items-start items-center">
    <ul class="flex flex-col gap-6 text-xl">
      <li class="flex gap-2">
        Bringing delight to Bento Design System
      </li>
      <li class="flex gap-2">
        Leading the IxD & Motion guild
      </li>
      <li class="flex gap-2">
        Envisioning the future of a platform
      </li>
      <li class="flex gap-2">
        Highlights from the past
      </li>
    </ul>
  </div>
  <div class="col-span-2 lg:col-span-1 self-start grid justify-items-start items-center">
    <ul class="flex flex-col gap-6 text-xl">
      <li class="flex gap-2">
        Home
      </li>
      <li class="flex gap-2">
        Projects
      </li>
      <li class="flex gap-2">
        About us
      </li>
      <li class="flex gap-2">
        Contact
      </li>
    </ul>
  </div>
  <div class="col-span-2 lg:col-span-1 self-start grid justify-items-start items-center">
    <ul class="flex flex-col gap-6 text-xl">
      <li class="flex gap-2">
        <span>
          Linkedin
        </span>
        <span>
          <ArrowDownLeftIcon class="rotate-180" size={24} />
        </span>
      </li>
      <li class="flex gap-2">
        <span>
          Twitter
        </span>
        <span>
          <ArrowDownLeftIcon class="rotate-180" size={24} />
        </span>
      </li>
      <li class="flex gap-2">
        <span>
          Facebook
        </span>
        <span>
          <ArrowDownLeftIcon class="rotate-180" size={24} />
        </span>
      </li>
      <li class="flex gap-2">
        <span>
          Instagram
        </span>
        <span>
          <ArrowDownLeftIcon class="rotate-180" size={24} />
        </span>
      </li>
    </ul>
  </div>
  <div class="col-span-4 border-t border-gray-7 mt-16 py-6 flex justify-center lg:justify-between items-center">
    <ul class="flex gap-4 items-center">
      <li>
        &copy; 2024
      </li>
      <li>
        -
      </li>
      <li class="-mt-3">
        <Logo />
      </li>
    </ul>
    <ul class="hidden lg:flex gap-8 items-center">
      <li>Privacy Policy</li>
      <li>Terms & Conditions</li>
    </ul>
  </div>
</footer>