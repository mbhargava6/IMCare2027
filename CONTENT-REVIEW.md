# Content review — 2026 rebuild

Every page, bio, service and resource link from the previous site was carried
over. This file lists the places where wording is **new** or was **corrected**,
so it can be checked by a clinician before the site goes live on imcare.ca.

## New wording added (please confirm or delete)

| Where | Text | File |
| --- | --- | --- |
| Home hero | "Specialist care, close to home at IMCare" | `_layouts/home.html` |
| Home hero card | "New here? Ask your family doctor to fax a referral to (855) 755-7771, or download our referral form." | `_layouts/home.html` |
| Services | Plain-language `note:` lines under echocardiography, Holter monitoring, stress testing, ABPM and cryotherapy | `_data/services.yml` |
| Services | Group summaries used on the home page cards | `_data/services.yml` |
| Team | The three group headings and their one-line descriptions | `_data/team_groups.yml` |
| Contact | Emergency callout: "If you are having chest pain, difficulty breathing, signs of a stroke…" | `contact.md` |
| Contact | "For referring providers" section | `contact.md` |
| Directions | "When you arrive" — bring health card, medication list, test results | `directions.md` |
| Services | "Echocardiograms are performed in our own echocardiography lab at the Port Hope office by registered cardiac sonographers." | `_data/services.yml` |
| Privacy | "Your personal health information is confidential… ask to speak with our privacy contact." | `privacy-policy.md` |
| Footer | "This website does not provide medical advice. In an emergency, call 911." | `_includes/footer.html` |
| 404 page | Whole page (the old site had none) | `404.html` |

Nothing above states a clinical fact, a wait time, a credential or an hours of
operation that was not already on the old site.

## Corrections made

- **"Defribrillator" → "Defibrillator"** (Patient Tools, two entries).
- **Two identical ICD links merged** into one entry, "Implantable Cardioverter
  Defibrillator (ICD)".
- **"ABC of Melanoma" → "ABCDEs of Melanoma"** to match the page it links to.
- **Broken link fixed:** *Exercise for Bone Health* had a stray apostrophe in
  the URL (`osteoporosis.ca/exercise'`) and did not work.
- **Broken link fixed:** *Portfolio diet* was missing its leading slash, so it
  broke on every page except the home page.
- **Duplicate removed:** "Skin cancer screening" appeared twice in the
  dermatology service list.
- **"Mcgill" → "McGill"** in Dr. Boivin's biography.
- **"Specialist Referrals"** ended with a stray ". ." — removed.
- **Removed a spam link.** The previous Directions page carried a hidden
  "Internet Provider" link to `kbj9qpmy.com`, injected by the third-party map
  embed generator that was used. The map is now a plain Google Maps embed with
  no third-party code and no API key.

## Confirmed by Dr. Bhargava, 5 September 2026

- **Pulmonary Medicine removed.** The service group, its two items and every
  mention in the page descriptions and search metadata are gone. IMCare does
  not offer this service.
- **Clinic hours published:** Monday to Friday, 9:00 am – 5:00 pm, by
  appointment only. They now appear on the home page action strip, the
  Directions page, the Contact page, the footer of every page, and in the
  site's structured data (so Google can show them in search results).
- **No Chest Pain Clinic.** Nothing was added, and nothing referring to one
  exists on the site.
- **Echocardiography lab named.** IMCare's own echo lab is now stated on the
  Services page and in the site description.

## Still worth deciding before launch

1. **The privacy page** on the old site actually contained the practice's
   founding history, not a privacy policy. That text now lives on
   `/about/`, and `/privacy-policy/` links to the privacy PDF.
2. **`/about/` used to be the team page.** It is now a genuine About page that
   links to `/team/`. Any external links to `imcare.ca/about/` will still work
   but will land somewhere different.
3. **13 team members are hidden** (`hidden: true` in `_data/team.yml`) because
   their profiles were switched off on the old site. Worth checking whether any
   should be restored: Darius Seidler, Khalid Pasha, Natasha Thompson, Kaitlin
   Dizon, Sohayla Arabi, Kathleen Bowles, Sarah Saunders, Shannon Murphy, Darla
   Murphy, Kathy Boon, Loretta Tamburello. Obed Adarkwah and Simran Jeet were
   hidden on 8 September 2026 at Dr. Bhargava's request.
4. **External links were not machine-checked.** 60 of the 77 Patient Tools
   links point to other organisations' websites (Ottawa Heart, AAD, Cleveland
   Clinic, Vimeo, YouTube). They should be clicked through once before launch.
