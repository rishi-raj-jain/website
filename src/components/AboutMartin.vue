<script setup lang="ts">
import type { Locales } from '@/services/locale'
import translations from '@/services/translations'
import { getRelativeLocaleUrl } from 'astro:i18n'

const props = defineProps<{ locale: Locales }>()
</script>

<template>
  <div class="mx-auto max-w-7xl rounded-lg px-4 py-8 text-[#a1a1aa] shadow-lg md:px-0">
    <div class="flex flex-col items-start gap-8 md:flex-row">
      <img
        src="/martindonadieu.webp"
        :alt="translations['martin_donadieu_on_a_motorcycle_with_a_rainbow_in_the_background'][props.locale]"
        class="md:w-144 mx-auto h-auto w-3/4 rounded-lg object-cover md:mx-0"
      />
      <div class="flex-1 space-y-4">
        <p class="text-2xl text-white">
          <span class="font-bold">👋 {{ translations['hi_there_im_martin_donadieu'][props.locale] }} </span>
        </p>
        <p>
          🇫🇷 {{ translations['im_a_french_software_engineer'][props.locale] }}<br />
          {{ translations['living_best_life'][props.locale] }} 🏝️. <br />{{ translations['made_capgo_with_passion'][props.locale] }}
        </p>
        <p>
          <span class="font-bold">🌟 {{ translations['i_m_a_huge_believer_in_open_source'][props.locale] }}</span
          ><br />
          {{ translations['capgo_proudly_stands_as_the_largest_ecosystem_of_open_source_plugins_for_capacitor'][props.locale] }} <br />{{
            translations['we_re_committed_to_fostering_a_community_where_developers_can_learn_contribute_and_grow_together'][props.locale]
          }}
        </p>
        <p>
          📧 {{ translations['each_time_you_contact_capgo_you_re_reaching_out_to_me_directly'][props.locale] }}<br />
          {{ translations['i_personally_handle_all_support_through_email_chat_or_discord_because_i_believe_in_real_connections'][props.locale] }} <br /><span class="font-bold"
            >🫶 {{ translations['your_challenges_are_my_challenges'][props.locale] }}</span
          >
        </p>
        <p>
          {{
            translations['when_im_not_working_on_capgo_you_ll_find_me_scaling_climbing_walls_🧗‍♂️_dancing_to_zouk_rhythms_💃_or_exploring_madeiras_stunning_nature_🌿'][props.locale]
          }}
        </p>
        <p>
          🐦 {{ translations['my_commitment_to_transparency_extends_to_everything_i_do'][props.locale] }} <br />{{
            translations['you_can_see_my_entire_process_unfold_on_twitter'][props.locale]
          }}
          <a href="https://twitter.com/martindonadieu" class="text-white hover:underline">@martindonadieu</a>
          {{ translations['and_hear_more_about_my_journey_on_the'][props.locale] }} <a href="https://solos.ventures" class="text-white hover:underline">solos.ventures</a> podcast.
        </p>
        <p class="font-bold text-white">{{ translations['lets_make_app_development_amazing_together'][props.locale] }} 🤝</p>
        <div class="pt-4">
          <div class="group relative mt-10 inline-flex">
            <div
              class="transitiona-all animate-tilt absolute -inset-px rounded-xl bg-gradient-to-r from-[#44BCFF] via-[#FF44EC] to-[#FF675E] opacity-70 blur-lg duration-1000 group-hover:-inset-1 group-hover:opacity-100 group-hover:duration-200"
            />
            <a
              :href="getRelativeLocaleUrl(props.locale, 'register')"
              :title="translations['get_quote_now'][props.locale]"
              class="font-pj relative inline-flex items-center justify-center rounded-xl bg-gray-900 px-8 py-4 text-lg font-bold text-white transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-gray-900 focus:ring-offset-2"
              role="button"
            >
              {{ translations['start_now'][props.locale] }}
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
