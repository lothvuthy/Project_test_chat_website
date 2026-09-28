# Sabay (Nuxt 3)

Fun social network prototype built with Nuxt 3 (SPA mode). Pages: Home, Friends, Groups, Chat, Alerts, Profile, Explore, and Games.

## Run
```
npm install
npm run dev        # http://localhost:3000
npm run generate   # static build in .output/public
```

## Structure
- `app.vue` layout, nav, scroll progress bar, story overlay, toast
- `pages/` social workflows for feed, friends, groups, chat, alerts, profile, explore, and games
- `components/PostCard.vue` post with reactions and comments
- `composables/useSabay.ts` data, state, saving (localStorage)
- `plugins/fx.client.ts` `v-reveal` scroll-reveal directive + click burst effect
- `assets/main.css` styles and animations

## Animations
Scroll: reveal on every page (`v-reveal="delay"`), top progress bar, tilting logo, animated level bar.
Click: emoji burst + button bounce, reaction pop, page slide transitions, post add/remove, comment expand, chat bubbles + typing dots, story zoom, toast slide.
All motion is disabled for users who prefer reduced motion.

## Social workflows
- Home feed: create posts, react, comment, share, save, and filter all / own / saved posts.
- Friends: accept or decline requests, search friends, remove friends, and send demo requests.
- Groups: discover, join, create, and post to local group discussions.
- Chat, alerts, and profile data are also local demo workflows.

All data is stored in this browser's `localStorage`. Friend suggestions and chat replies are demo characters; there are no real accounts, shared server database, cross-device sync, or private realtime messaging. Use a backend such as Supabase or Firebase before treating this as a multi-user social network.
