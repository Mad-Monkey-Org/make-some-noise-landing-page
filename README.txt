MAKE SOME NOISE — creator landing page
Mad Monkey Hostels

WHAT THIS IS
Static page, no build step, no dependencies. Drop the folder on the server and
point a route at it. Everything works from file system alone.

FILES
  index.html                      the page (all CSS and JS inline)
  assets/hero-make-some-noise.png header artwork
  assets/tiktok-example.jpg       phone mockup in the "this is why" block
  assets/og-image.jpg             1200x630 link-preview card

BEFORE GOING LIVE — 1 REQUIRED CHANGE
In the <head>, replace every instance of
    https://madmonkeyhostels.com/creatorhub/allin
with the real URL of the page.

This matters most for og:image. It MUST be an absolute URL. Instagram,
WhatsApp and iMessage will not render a link preview from a relative path,
and the preview card is the whole point when this gets DM'd.

There are 4 instances: canonical, og:url, og:image, twitter:image.

NOTES
  - The page is set to noindex. Remove that meta tag if you want it in search.
  - The countdown targets 2026-09-30T23:59:59+07:00 (ICT). It swaps itself to a
    closing message after that, so nothing breaks if the page stays up.
    The date lives in one place, in the <script> at the bottom.
  - Copy-to-clipboard needs HTTPS to use the modern API. There is a fallback
    for non-secure contexts, but serve it over HTTPS anyway.
  - Poppins loads from Google Fonts with a system-font fallback stack. Self-host
    it if your CSP blocks fonts.googleapis.com.
  - Outbound links: the two Drive folders and six logo files, the TikTok example,
    and the CTA to /creatorhub/revenue. Check the Drive folders are set to
    "anyone with the link" or creators will hit a permission wall.
  - No tracking of any kind is included. Add your own GA/Meta pixel if wanted.
  - Single theme by design — it does not follow the OS dark mode setting.
