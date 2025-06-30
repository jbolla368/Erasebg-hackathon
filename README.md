# Erasebg-hackathon
EraseBG — AI-powered, no-code background remover built with a single Bolt.new prompt for the World’s Largest Hackathon.
# ✨ EraseBG

## 🪄 What it does

**EraseBG** is a simple, AI-powered tool that lets anyone remove the background from an image instantly — no design skills, no expensive software, no hassle.  
Users can:
- Upload a JPG or PNG (≤ 10 MB)
- Click one button to remove the background using the Clipdrop API
- Download a clean, transparent PNG in seconds

Each user can remove up to **2 images per day** for free — perfect for **e-commerce sellers, designers, and social media creators** who need professional results fast.

---

## 💡 Inspiration

I wanted to solve a common pain point: making clean, background-free images without spending hours in Photoshop or paying for complex tools.  
With **EraseBG**, anyone can upload → click → download — and get pro results instantly.

---

## 🧩 How it works

Built with **Bolt.new**, **Tailwind CSS**, and the **Clipdrop Remove-Background API**.

- Fully no-code build: the entire app flow was generated using **one single prompt** in Bolt.
- Drag-and-drop or browse to upload images.
- Call the Clipdrop API with `multipart/form-data` and secure API key.
- Show a progress bar while processing.
- Display the final transparent PNG with a “Download” button.
- Friendly error toasts for issues like invalid files or daily quota exceeded.
- Rate limit: max **2 removals per IP per day** to manage API usage.

---

## 🏆 One-Shot Challenge Entry

This entire project was created from a **single prompt** inside Bolt.new — showcasing what’s possible with no-code + clear AI instructions.

**Prompt used:**
Create “EraseBG” – a one-click image background-remover that uses the Clipdrop Remove-Background API.

Core user flow
Landing page with hero headline, short tagline, and a prominent “Try It” CTA.

Drag-and-drop area (plus “Browse” button) accepts JPG or PNG ≤ 10 MB / 25 MP.

After an image is picked, show a thumbnail, file size, and a single “Remove Background” button.

On click, send a POST multipart/form-data request to https://clipdrop-api.co/remove-background/v1 with header x-api-key: CLIPDROP_KEY.

Display a progress bar while processing.

Success: replace the thumbnail with the processed image and show a “Download PNG” button.

Error: display a toast explaining the issue (e.g., quota exceeded, invalid file) and offer a retry link.

Rate-limit logic
Track calls per client IP for 24 hours.

Allow up to 2 removals per IP per day; if the limit is reached, return HTTP 429 with a clear JSON message.

Styling & UX
Dark-mode default, Tailwind utility classes.

Frosted-glass cards with soft shadows for a modern look.

Buttons: rounded-lg, subtle scale-up on hover, focus ring.

Below the hero, include two sample images users can click to test instantly.

Mobile-first responsive layout.

SEO-ready: proper title, meta description, and OpenGraph image.

Nice-to-have (stretch)
Batch upload of up to five images processed in parallel.

“Remove & Replace” option to fill the background with a user-selected solid color.

Deliverables
Production-ready codebase.


---

## 🏗️ Built with

- **Bolt.new** — No-code app builder  
- **Tailwind CSS** — Modern, mobile-first styling  
- **Clipdrop Remove-Background API** — AI background removal  
- **Netlify** — Hosting and deployment  
- *(Optional)* **Supabase** — Planned for user login & history in future

---

## ⚡ Challenges I faced

- Originally, I planned to add sign-in and user image history using Supabase, but setting up secure auth and storage was complex for a no-code hackathon timeframe. I decided to keep EraseBG open and simple instead.
- Managing API usage securely in a no-code environment.
- Handling large image uploads and clear error feedback.
- Designing a clean, mobile-first UI with good UX for each step.

---

## 🚀 What’s next

- Bring back **sign-in** and **image history** with Supabase or a similar backend.
- Add **batch uploads** for up to 5 images.
- Include a **“Remove & Replace”** option with solid background colors.
- Turn EraseBG into a **PWA** with an offline fallback page that explains background removal requires an internet connection.
- **Increase daily limit** from 2 to **10 images/day** to help more users.
- Add **pricing options** — Free, Basic, and Pro plans for more removals or premium features.

---

## 📌 How to run locally

1. Clone the Bolt.new workspace *(if shared)* or start your own from the prompt above.  
2. Add your **Clipdrop API key** securely.  
3. Deploy to **Netlify** or **Vercel**.  
4. Done!

---

## 🔗 Live demo

[**View the live app here →**](https://candid-taiyaki-01d09c.netlify.app/)

---

**Thank you for checking out EraseBG! 🙌**  
Built with AI, no-code, and a single prompt — one click at a time.



