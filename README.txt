FITTRACK PRO v33 — REAL AI COACH

WHAT'S NEW
- Real AI Coach screen
- Daily Coach
- Workout adjustment
- Weekly AI review
- Nutrition Coach
- Sends authenticated requests to a Supabase Edge Function
- The function reads the signed-in customer's own profile, workout history, PRs and meal plan
- AI provider API key stays server-side and never appears in GitHub/index.html
- AI-created workout can be applied to the active workout
- v32 structured cloud and all prior features retained

IMPORTANT
The app UI is ready immediately, but the AI button will show "AI setup required" until the
Supabase Edge Function is deployed and provider secrets are configured.

FILES FOR GITHUB PAGES
- index.html
- manifest.webmanifest
- sw.js

SUPABASE EDGE FUNCTION
Source:
supabase/functions/fittrack-ai-coach/index.ts

Server secrets required:
AI_PROVIDER_URL
AI_PROVIDER_API_KEY
AI_MODEL

AI_PROVIDER_URL is expected to be a complete OpenAI-compatible chat-completions endpoint.
Choose your provider/model separately and keep credentials only in Supabase secrets.

No database SQL changes are required for v33; it uses the v32 structured tables.
