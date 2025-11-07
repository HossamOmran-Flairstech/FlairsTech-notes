Documentation file for homepage 


page REST API 
https://flairstech.flairsrealtor.com/wp-json/wp/v2/pages?slug=home&acf_format=standard

Rank math 
https://flairstech.flairsrealtor.com/wp-json/rankmath/v1/getHead?url=https://flairstech.flairsrealtor.com/home

#Homepage Components
## 🧩 Component 2: `homepage_hero_with_animation_and_service_cards`

### 📐 Fields:
| Field Name                         | Type       | Description                                  |
|-----------------------------------|------------|----------------------------------------------|
| hero_section_heading              | `string`   | Main heading (e.g., "Scale Smart Your")     |
| repeated_text_that_will_show_in_hero | `array`    | Array of `{ text: string }` lines           |
| hero_section_sub_heading          | `string`   | Subheading                                   |
| hero_section_short_descripsion    | `string`   | Paragraph text                               |
| cta                               | `object`   | CTA button with `title`, `url`, `target`     |
| soical_media_follow_text          | `string`   | Label like "Follow us:"                      |
| facebook / linkedin / instagram   | `object`   | Social link objects (`title`, `url`, `target`)|
| twitter_x                         | `string`   | (optional) Not used                          |
| service_heading_white_text        | `string`   | Heading part 1                               |
| services_heading_gradiant_text    | `string`   | Heading part 2 (styled differently)          |
| service_subheading                | `string`   | Description                                  |
| service_cards_loop                | `array`    | List of service cards (see below)           |
| last_service_card_cta             | `object`   | Final CTA button                             |

### 🧱 Service Cards Structure
Each item in `service_cards_loop` includes:
| Field               | Type     | Description                              |
|--------------------|----------|------------------------------------------|
| badge_icon         | `object` | Image object (full ACF image array)     |
| badge_text         | `string` | Label above card title                   |
| card_heading       | `string` | Title of the card                        |
| card_short_description | `string` | Description paragraph                 |
| card_cta           | `object` | Optional CTA object                      |

### Edge Cases & Content Rules
All fields are OPTONAL unless specified otherwise.
Heading Hierarchy:
Hero section main heading → <h1>
Example:
<h1>Scale Smart Your <span>Teams.</span><span>Systems.</span><span>Success.</span></h1>

Paragraphs:
Always wrapped in <p> tags.

Free Text Logic:
If user sends <strong>Bold Text</strong>, render as Bold Text (without printing HTML).

Colored Text:
Wrap text in <span class="gradient-text">Colored Text</span>.
Example:
<h2>Strengthen your reach, <span class="gradient-text">enhance your ROI</span></h2>



### 🔍 Example JSON (from real API):
```json
  {
          "acf_fc_layout": "homepage_hero_with_animation_and_service_cards",
          "hero_section_heading": "Scale Smart Your",
          "repeated_text_that_will_show_in_hero": [
            {
              "text": "Teams."
            },
            {
              "text": "Systems."
            },
            {
              "text": "Success."
            }
          ],
          "hero_section_sub_heading": "with AI-Powered Technology Managed Services designed to simplify lives.",
          "hero_section_short_descripsion": "\u003Cp\u003EJoin 100+ organizations worldwide who drive measurable results daily from one accountable partner they trust.\u003C/p\u003E\n",
          "cta": {
            "title": "GET IN TOUCH",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          },
          "soical_media_follow_text": "Follow us:",
          "facebook": {
            "title": "",
            "url": "https://www.facebook.com/",
            "target": ""
          },
          "linkedin": {
            "title": "",
            "url": "https://www.linkedin.com/feed/",
            "target": ""
          },
          "instagram": {
            "title": "",
            "url": "https://www.instagram.com/",
            "target": ""
          },
          "twitter_x": "",
          "service_heading_white_text": "Strengthen your reach,",
          "services_heading_gradiant_text": "enhance your ROI",
          "service_subheading": "At the core of our company is a commitment to delivering high-impact",
          "service_cards_loop": [
            {
              "badge_icon": {
                "ID": 7337,
                "id": 7337,
                "title": "doubledCircle",
                "filename": "doubledCircle.svg",
                "filesize": 505,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                "link": "https://flairstech.flairsrealtor.com/home/doubledcircle",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "doubledcircle",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:14",
                "modified": "2025-11-06 21:21:14",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Software Development",
              "card_heading": "Application Maintenance",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "badge_icon": {
                "ID": 7338,
                "id": 7338,
                "title": "settings",
                "filename": "settings.svg",
                "filesize": 4295,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                "link": "https://flairstech.flairsrealtor.com/home/settings",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "settings",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:22",
                "modified": "2025-11-06 21:21:22",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Business Operations",
              "card_heading": "Technical Support",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "Read More",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "badge_icon": {
                "ID": 7339,
                "id": 7339,
                "title": "Vector",
                "filename": "Vector.svg",
                "filesize": 850,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                "link": "https://flairstech.flairsrealtor.com/home/vector",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "vector",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:30",
                "modified": "2025-11-06 21:21:30",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Support Services",
              "card_heading": "Accounting",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "Read More",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "badge_icon": {
                "ID": 7339,
                "id": 7339,
                "title": "Vector",
                "filename": "Vector.svg",
                "filesize": 850,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                "link": "https://flairstech.flairsrealtor.com/home/vector",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "vector",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:30",
                "modified": "2025-11-06 21:21:30",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Digital Solutions",
              "card_heading": "Digital Transformation",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "Read More",
                "url": "https://flairstech.com/blog",
                "target": ""
              }
            },
            {
              "badge_icon": {
                "ID": 7340,
                "id": 7340,
                "title": "circle",
                "filename": "circle.svg",
                "filesize": 1292,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                "link": "https://flairstech.flairsrealtor.com/home/circle",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "circle",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:35",
                "modified": "2025-11-06 21:21:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Software Development",
              "card_heading": "Software Development",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "badge_icon": false,
              "badge_text": "Digital Solutions",
              "card_heading": "Platform Development",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "badge_icon": {
                "ID": 7337,
                "id": 7337,
                "title": "doubledCircle",
                "filename": "doubledCircle.svg",
                "filesize": 505,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                "link": "https://flairstech.flairsrealtor.com/home/doubledcircle",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "doubledcircle",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:14",
                "modified": "2025-11-06 21:21:14",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/doubledCircle.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Customer Experience",
              "card_heading": "Customer Experience Management",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "badge_icon": {
                "ID": 7339,
                "id": 7339,
                "title": "Vector",
                "filename": "Vector.svg",
                "filesize": 850,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                "link": "https://flairstech.flairsrealtor.com/home/vector",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "vector",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:30",
                "modified": "2025-11-06 21:21:30",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "badge_text": "Customer Experience",
              "card_heading": "Sales Support",
              "card_short_description": "Lorem Ipsum is simply dummy text of the printing and type setting industry.",
              "card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            }
          ],
          "last_service_card_cta": {
            "title": "All Services",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          }
        }

```

## 🧩 Component 2: `global_intro_map`

### 📐 Fields
| Field Name                 | Type     | Description                                      |
|---------------------------|----------|--------------------------------------------------|
| badge_icon                | `object` | Image object (full ACF image array)              |
| badge_text                | `string` | Text label above heading                         |
| black_heading_            | `string` | Main heading in black                            |
| continue_gradiant_heading| `string` | Gradient colored heading                         |
| free_text                 | `string` | Rich text (HTML string with <p>, <strong>, etc.) |
| map_elements              | `array`  | List of country blocks (see below)               |

### 🧱 Map Elements Structure
Each item in `map_elements` includes:
| Field         | Type     | Description                                     |
|---------------|----------|-------------------------------------------------|
| country_flag  | `object` | Flag image (ACF image object, return_format: array) |
| country_name  | `string` | Name of the country                             |
| short_text    | `string` | Short description text for the country          |

---
### Edge Cases & Content Rules
All fields are OPTONAL unless specified otherwise.
Heading Hierarchy:
Any non hero section heading → <h2>
Example:
<h2>Global Services <span class="gradiant-text">Local feel</span></h2>
Paragraphs:
Always wrapped in <p> tags.

Free Text Logic:
If user sends <strong>Bold Text</strong>, render as Bold Text (without printing HTML).


### 🧩 Example JSON (as returned by API)
```json
  {
          "acf_fc_layout": "global_intro_map",
          "badge_icon": {
            "ID": 7345,
            "id": 7345,
            "title": "Primary",
            "filename": "Primary.svg",
            "filesize": 1115,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
            "link": "https://flairstech.flairsrealtor.com/home/primary",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "primary",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:30:06",
            "modified": "2025-11-06 21:30:06",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "badge_text": "We serve Globally",
          "black_heading_": "Global Services",
          "continue_gradiant_heading": "Local feel",
          "free_text": "\u003Cp\u003EFlairstech is a trusted global technology partner, delivering high-quality software solutions to clients across the US, Europe, and the Middle East.\u003C/p\u003E\n\u003Cp\u003EWe specialize in building scalable web, mobile, and enterprise systems tailored to each client&#8217;s unique business goals.\u003C/p\u003E\n",
          "map_elements": [
            {
              "country_flag": {
                "ID": 7349,
                "id": 7349,
                "title": "flag-for-saudi-arabia_svgrepo.com",
                "filename": "flag-for-saudi-arabia_svgrepo.com_.svg",
                "filesize": 11520,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                "link": "https://flairstech.flairsrealtor.com/home/flag-for-saudi-arabia_svgrepo-com",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "flag-for-saudi-arabia_svgrepo-com",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:32:35",
                "modified": "2025-11-06 21:32:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "country_name": "Saudi Arabia",
              "short_text": "we have a multiply of account inside KSA"
            },
            {
              "country_flag": {
                "ID": 7349,
                "id": 7349,
                "title": "flag-for-saudi-arabia_svgrepo.com",
                "filename": "flag-for-saudi-arabia_svgrepo.com_.svg",
                "filesize": 11520,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                "link": "https://flairstech.flairsrealtor.com/home/flag-for-saudi-arabia_svgrepo-com",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "flag-for-saudi-arabia_svgrepo-com",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:32:35",
                "modified": "2025-11-06 21:32:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "country_name": "Egypt",
              "short_text": "we have a multiply of account inside Egypt"
            },
            {
              "country_flag": {
                "ID": 7349,
                "id": 7349,
                "title": "flag-for-saudi-arabia_svgrepo.com",
                "filename": "flag-for-saudi-arabia_svgrepo.com_.svg",
                "filesize": 11520,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                "link": "https://flairstech.flairsrealtor.com/home/flag-for-saudi-arabia_svgrepo-com",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "flag-for-saudi-arabia_svgrepo-com",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:32:35",
                "modified": "2025-11-06 21:32:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "country_name": "United Arab Kingdom",
              "short_text": "we have a multiply of account inside UAE"
            },
            {
              "country_flag": {
                "ID": 7349,
                "id": 7349,
                "title": "flag-for-saudi-arabia_svgrepo.com",
                "filename": "flag-for-saudi-arabia_svgrepo.com_.svg",
                "filesize": 11520,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                "link": "https://flairstech.flairsrealtor.com/home/flag-for-saudi-arabia_svgrepo-com",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "flag-for-saudi-arabia_svgrepo-com",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:32:35",
                "modified": "2025-11-06 21:32:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "country_name": "Canada",
              "short_text": "we have a multiply of account inside CA"
            },
            {
              "country_flag": {
                "ID": 7349,
                "id": 7349,
                "title": "flag-for-saudi-arabia_svgrepo.com",
                "filename": "flag-for-saudi-arabia_svgrepo.com_.svg",
                "filesize": 11520,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                "link": "https://flairstech.flairsrealtor.com/home/flag-for-saudi-arabia_svgrepo-com",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "flag-for-saudi-arabia_svgrepo-com",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:32:35",
                "modified": "2025-11-06 21:32:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "country_name": "United States of America",
              "short_text": "we have a multiply of account inside USA"
            },
            {
              "country_flag": {
                "ID": 7349,
                "id": 7349,
                "title": "flag-for-saudi-arabia_svgrepo.com",
                "filename": "flag-for-saudi-arabia_svgrepo.com_.svg",
                "filesize": 11520,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                "link": "https://flairstech.flairsrealtor.com/home/flag-for-saudi-arabia_svgrepo-com",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "flag-for-saudi-arabia_svgrepo-com",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:32:35",
                "modified": "2025-11-06 21:32:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/flag-for-saudi-arabia_svgrepo.com_.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "country_name": "Saudi Arabia",
              "short_text": "we have a multiply of account inside KSA"
            }
          ]
        },
```
## 🧩 Component 3: `bg_video_section_for_aimy_with_floating_why_flairstech`

### 📐 Fields
| Field Name | Type | Description |
|-------------|------|-------------|
| background_placeholder_image | `object` | Background fallback image (ACF image array) |
| background_video_url | `string` | Background video file URL |
| first_badge_icon | `object` | Image for the first badge (AIMY AI section) |
| first_badge_text | `string` | Text label for the first badge |
| first_heading | `string` | Main heading for AIMY section |
| first_sub_heading | `string` | Supporting subheading |
| first_free_text | `string (HTML)` | HTML content for AIMY section text |
| loop_paragraph_fixed_part | `string` | Static prefix text before animated loop words |
| loop_pargrph_repeated_text | `array` | List of objects with `{ repeated_text: string }` |
| cta | `object` | CTA button object with `title`, `url`, and `target` |
| right_side_cards | `array` | Performance cards shown on right side (see structure below) |
| watch_video_button_text | `string` | Label for “Watch Video” button |
| watch_video_youtube_code | `string` | YouTube video ID (used in modal embed) |
| second_badge_icon | `object` | Icon for the second badge (Why Flairstech section) |
| second_badge_text | `string` | Text for the second badge |
| second_heading | `string` | Heading for Why Flairstech section |
| second_free_text | `string (HTML)` | Description text (supports <p>, <strong>, <em> tags) |
| why_flairstech_grid | `array` | List of “flip cards” with stats and details (see structure below) |

---
### Edge Cases & Content Rules

SAME AS previous component main heading h2 
subheadings and any text will be in p tag

#### Videos
1-we will have a placeholder image that will load at first to minimize network load 
2-we will get the background video url from our server like this "https://flairstech.flairsrealtor.com/app/uploads/2025/11/file_example_MP4_480_1_5MG.mp4"
3-clicking the CTA for the video will show a popup and play the video using embeded youtube video content editors will  you will recieve only the video code from the api and you have to make it to work for example 

script example 
<script>
function playVideo(element, videoCode) {
    const iframe = document.createElement('iframe');
    iframe.src = `https://www.youtube.com/embed/${videoCode}?autoplay=1`;
    iframe.setAttribute("allow", "autoplay; encrypted-media");
    iframe.allowFullscreen = true;
    element.innerHTML = ""; // Clear placeholder content
    element.appendChild(iframe);
}
</script>
or whatever will work with next.js

### 🧱 Right Side Cards Structure
Each item in `right_side_cards` includes:
| Field | Type | Description |
|--------|------|-------------|
| insert_numbers_with_percentage | `string` | Number or percentage text (e.g., "98%", "x3") |
| short_text | `string` | Description explaining the metric |

### 🧱 Why Flairstech Grid Structure
Each item in `why_flairstech_grid` includes:
| Field | Type | Description |
|--------|------|-------------|
| upper_text_before_flip | `string` | Top text shown before flipping animation |
| upper_text_after_flip | `string` | Top text after flipping animation |
| front_card_numbers_with_percentage | `string` | Main number (e.g., “98%”) |
| front_short_text_after_numbers | `string` | Short descriptive label under number |
| lower_back_short_text_after_flip | `string` | Backside text after flip |

---

### 🧩 Example JSON (as returned by API)
```json
      {
          "acf_fc_layout": "bg_video_section_for_aimy_with_floating_why_flairstech",
          "background_placeholder_image": {
            "ID": 7353,
            "id": 7353,
            "title": "about",
            "filename": "about.png",
            "filesize": 1103972,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about.png",
            "link": "https://flairstech.flairsrealtor.com/home/about-2",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "about-2",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:40:11",
            "modified": "2025-11-06 21:40:11",
            "menu_order": 0,
            "mime_type": "image/png",
            "type": "image",
            "subtype": "png",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 1440,
            "height": 810,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about-150x150.png",
              "thumbnail-width": 150,
              "thumbnail-height": 150,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about-300x169.png",
              "medium-width": 300,
              "medium-height": 169,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about-768x432.png",
              "medium_large-width": 768,
              "medium_large-height": 432,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about-1024x576.png",
              "large-width": 1024,
              "large-height": 576,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about.png",
              "1536x1536-width": 1440,
              "1536x1536-height": 810,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/about.png",
              "2048x2048-width": 1440,
              "2048x2048-height": 810
            }
          },
          "background_video_url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/file_example_MP4_480_1_5MG.mp4",
          "first_badge_icon": {
            "ID": 7358,
            "id": 7358,
            "title": "Primary (1)",
            "filename": "Primary-1.svg",
            "filesize": 1643,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
            "link": "https://flairstech.flairsrealtor.com/home/primary-1",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "primary-1",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:45:47",
            "modified": "2025-11-06 21:45:47",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-1.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "first_badge_text": "AIMY AI",
          "first_heading": "Business, Simplified with AIMY.",
          "first_sub_heading": "Our vision is to simplify lives using technology, so we created AIMY.",
          "first_free_text": "\u003Cp\u003EA series of AI agents and tools that power our managed services to boost \u003Cstrong\u003Eoutcomes and streamline\u003C/strong\u003E internal operations, maximizing our productivity.\u003C/p\u003E\n",
          "loop_paragraph_fixed_part": "AIMY is for Artificial Intelligence my",
          "loop_pargrph_repeated_text": [
            {
              "repeated_text": "CX."
            },
            {
              "repeated_text": "Data Processing."
            },
            {
              "repeated_text": "Service."
            },
            {
              "repeated_text": "QA"
            },
            {
              "repeated_text": "Maintinance"
            }
          ],
          "cta": {
            "title": "Learn more",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          },
          "right_side_cards": [
            {
              "insert_numbers_with_percentage": "100%",
              "short_text": "boost in customer satisfaction"
            },
            {
              "insert_numbers_with_percentage": "98%",
              "short_text": "knowledge retrieval accuracy"
            },
            {
              "insert_numbers_with_percentage": "80%",
              "short_text": "reduction in data entry efforts"
            },
            {
              "insert_numbers_with_percentage": "x3",
              "short_text": "more contact quality audits"
            }
          ],
          "watch_video_button_text": "watch a video",
          "watch_video_youtube_code": "MRKNV6EWxKY",
          "second_badge_icon": {
            "ID": 7359,
            "id": 7359,
            "title": "Primary (2)",
            "filename": "Primary-2.svg",
            "filesize": 1207,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
            "link": "https://flairstech.flairsrealtor.com/home/primary-2",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "primary-2",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:46:43",
            "modified": "2025-11-06 21:46:43",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-2.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "second_badge_text": "Why Flairstech",
          "second_heading": "Differentiators That Move the Needle. ",
          "second_free_text": "\u003Cp\u003EWe’re more than just a software provider — we’re a strategic partner committed to your success. Here’s why leading \u003Cem\u003E\u003Cstrong\u003Ebusinesses choose us\u003C/strong\u003E\u003C/em\u003E:\u003C/p\u003E\n",
          "why_flairstech_grid": [
            {
              "upper_text_before_flip": "Presence in",
              "upper_text_after_flip": "Net Promoter Score (NPS)",
              "front_card_numbers_with_percentage": "98%",
              "front_short_text_after_numbers": "Net Promoter Score (NPS)",
              "lower_back_short_text_after_flip": "A reflection of ourcommitment to client satisfaction"
            },
            {
              "upper_text_before_flip": "Certified ",
              "upper_text_after_flip": "Certified Professionals",
              "front_card_numbers_with_percentage": "1000+ ",
              "front_short_text_after_numbers": "Certified Professionals",
              "lower_back_short_text_after_flip": "A reflection of ourcommitment to client satisfaction"
            },
            {
              "upper_text_before_flip": "Centers",
              "upper_text_after_flip": "Delivery Centers",
              "front_card_numbers_with_percentage": "5",
              "front_short_text_after_numbers": "Delivery Centers",
              "lower_back_short_text_after_flip": "A reflection of ourcommitment to client satisfaction"
            },
            {
              "upper_text_before_flip": "Partners",
              "upper_text_after_flip": "Partners",
              "front_card_numbers_with_percentage": "100+",
              "front_short_text_after_numbers": "Partners",
              "lower_back_short_text_after_flip": "A reflection of ourcommitment to client satisfaction"
            },
            {
              "upper_text_before_flip": "Support",
              "upper_text_after_flip": "Support Center",
              "front_card_numbers_with_percentage": "24/7",
              "front_short_text_after_numbers": "Support Center",
              "lower_back_short_text_after_flip": "A reflection of ourcommitment to client satisfaction"
            },
            {
              "upper_text_before_flip": "Average Customer Tenure",
              "upper_text_after_flip": "Years",
              "front_card_numbers_with_percentage": "5+",
              "front_short_text_after_numbers": "Years",
              "lower_back_short_text_after_flip": "A reflection of ourcommitment to client satisfaction"
            }
          ]
        }
```
## 🧩 Component: `logos_carsuol_with_heading`

### 📐 Fields

| Field Name        | Type      | Description                                  |
|-------------------|-----------|----------------------------------------------|
| heading           | `string`  | Main section heading                         |
| repeated_logos    | `array`   | Array of uploaded logo objects (see below)   |

---

### 🖼️ Logos Structure

Each logo in `repeated_logos` includes:

| Field Name  | Type     | Description                              |
|-------------|----------|------------------------------------------|
| upload_logo | `object` | ACF image object containing: `url`, `title`, `link` |

---

### Example Data

```json
 {
          "acf_fc_layout": "logos_carsuol_with_heading",
          "heading": "Trusted by 500+ global companies",
          "repeated_logos": [
            {
              "upload_logo": {
                "ID": 7362,
                "id": 7362,
                "title": "aws 2",
                "filename": "aws-2.svg",
                "filesize": 5840,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                "link": "https://flairstech.flairsrealtor.com/home/aws-2",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "aws-2",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:55:53",
                "modified": "2025-11-06 21:55:53",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              }
            },
            {
              "upload_logo": {
                "ID": 7363,
                "id": 7363,
                "title": "aws 2 (1)",
                "filename": "aws-2-1.svg",
                "filesize": 8736,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                "link": "https://flairstech.flairsrealtor.com/home/aws-2-1",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "aws-2-1",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:55:55",
                "modified": "2025-11-06 21:55:55",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-1.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              }
            },
            {
              "upload_logo": {
                "ID": 7364,
                "id": 7364,
                "title": "aws 2 (2)",
                "filename": "aws-2-2.svg",
                "filesize": 11840,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                "link": "https://flairstech.flairsrealtor.com/home/aws-2-2",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "aws-2-2",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:55:57",
                "modified": "2025-11-06 21:55:57",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-2.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              }
            },
            {
              "upload_logo": {
                "ID": 7365,
                "id": 7365,
                "title": "aws 2 (3)",
                "filename": "aws-2-3.svg",
                "filesize": 135255,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                "link": "https://flairstech.flairsrealtor.com/home/aws-2-3",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "aws-2-3",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:55:59",
                "modified": "2025-11-06 21:55:59",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/aws-2-3.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              }
            }
          ]
        },
```
## 🧩 Component: `case_studies_manual_insertion`

### 📐 Fields
| Field Name                 | Type     | Description |
|---------------------------|----------|-------------|
| background_color          | `string` | Background color hex  | if  returned empty it should be the default colors in homepage design
| text_color                | `string` | Text color hex  |if  returned empty it should be the default colors in homepage design
| badge_icon                | `object` | ACF image object for badge |
| badge_text                | `string` | Text label for badge |
| heading_white_text        | `string` | White part of section heading |
| continue_gradiant_heading | `string` | Gradient-styled part of heading |
| right_side_free_text      | `string (HTML)` | Paragraph shown beside the cards |
| cta                       | `object` | CTA button with `title`, `url`, `target` |
| card_repeater             | `array`  | List of manually inserted case study cards (see structure below) |

---

### 🧱 Card Repeater Structure

Each item in `card_repeater` includes:

| Field                         | Type     | Description |
|------------------------------|----------|-------------|
| card_image                   | `object` | Main image of the case study |
| left_side_card_badge_text    | `string` | Region or label badge (e.g., "KSA") |
| right_side_client_logo       | `object` | Client logo (ACF image object) |
| card_heading                 | `string` | Title of the case study |
| card_short_description       | `string` | Summary/preview text |
| cta_                         | `object` | CTA button object (`title`, `url`, `target`) |

---

### ⚙️ Frontend Notes

- Each card contains both left-side region badge and right-side logo you should also know that right side logo can be empty that means the cards should show corretly if we didn't add a logo for our clients.
- Support responsive image rendering with appropriate `alt`, `srcset`, and fallback handling
- All HTML text must be rendered safely
- Empty `title` in CTA can be skipped or fallback to “Read More”
- Main section title is h2
- Each card title is H3
- any other normal text is p tag

---

### 🧩 Example JSON (as returned by API)
```json
 {
          "acf_fc_layout": "case_studies_manual_insertion",
          "background_color": "",
          "text_color": "",
          "badge_icon": {
            "ID": 7366,
            "id": 7366,
            "title": "Primary (3)",
            "filename": "Primary-3.svg",
            "filesize": 2256,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
            "link": "https://flairstech.flairsrealtor.com/home/primary-3",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "primary-3",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:57:35",
            "modified": "2025-11-06 21:57:35",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "badge_text": "Case Studies",
          "heading_white_text": "Real Impact,",
          "continue_gradiant_heading": "Real Results",
          "right_side_free_text": "\u003Cp\u003EExplore how our solutions have helped businesses streamline operations, enhance user experiences, and scale with confidence.\u003C/p\u003E\n",
          "cta": {
            "title": "Read More",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          },
          "card_repeater": [
            {
              "card_image": {
                "ID": 7367,
                "id": 7367,
                "title": "a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "filename": "a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                "filesize": 995131,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                "link": "https://flairstech.flairsrealtor.com/home/a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:45",
                "modified": "2025-11-06 22:01:45",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1200,
                "height": 675,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-300x169.png",
                  "medium-width": 300,
                  "medium-height": 169,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-768x432.png",
                  "medium_large-width": 768,
                  "medium_large-height": 432,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-1024x576.png",
                  "large-width": 1024,
                  "large-height": 576,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                  "1536x1536-width": 1200,
                  "1536x1536-height": 675,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                  "2048x2048-width": 1200,
                  "2048x2048-height": 675
                }
              },
              "left_side_card_badge_text": "Gulf Area",
              "right_side_client_logo": {
                "ID": 7369,
                "id": 7369,
                "title": "image 53",
                "filename": "image-53.svg",
                "filesize": 206515,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                "link": "https://flairstech.flairsrealtor.com/home/image-53",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "image-53",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:02:37",
                "modified": "2025-11-06 22:02:37",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_short_description": "Lorem ipsum dolor sit amet, consectetur",
              "cta_": {
                "title": "",
                "url": "https://flairstech.com/contact-us/book",
                "target": "_blank"
              }
            },
            {
              "card_image": {
                "ID": 7368,
                "id": 7368,
                "title": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "filename": "1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "filesize": 1616495,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "link": "https://flairstech.flairsrealtor.com/home/1029d30a922ae6c512188eb157f60a8ee179951f",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:57",
                "modified": "2025-11-06 22:01:57",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1482,
                "height": 840,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-300x170.png",
                  "medium-width": 300,
                  "medium-height": 170,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-768x435.png",
                  "medium_large-width": 768,
                  "medium_large-height": 435,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-1024x580.png",
                  "large-width": 1024,
                  "large-height": 580,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "1536x1536-width": 1482,
                  "1536x1536-height": 840,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "2048x2048-width": 1482,
                  "2048x2048-height": 840
                }
              },
              "left_side_card_badge_text": "Africa",
              "right_side_client_logo": {
                "ID": 7369,
                "id": 7369,
                "title": "image 53",
                "filename": "image-53.svg",
                "filesize": 206515,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                "link": "https://flairstech.flairsrealtor.com/home/image-53",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "image-53",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:02:37",
                "modified": "2025-11-06 22:02:37",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_short_description": "Lorem ipsum dolor sit amet, consectetur",
              "cta_": {
                "title": "",
                "url": "https://flairstech.com/blog",
                "target": ""
              }
            },
            {
              "card_image": {
                "ID": 7367,
                "id": 7367,
                "title": "a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "filename": "a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                "filesize": 995131,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                "link": "https://flairstech.flairsrealtor.com/home/a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:45",
                "modified": "2025-11-06 22:01:45",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1200,
                "height": 675,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-300x169.png",
                  "medium-width": 300,
                  "medium-height": 169,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-768x432.png",
                  "medium_large-width": 768,
                  "medium_large-height": 432,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-1024x576.png",
                  "large-width": 1024,
                  "large-height": 576,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                  "1536x1536-width": 1200,
                  "1536x1536-height": 675,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                  "2048x2048-width": 1200,
                  "2048x2048-height": 675
                }
              },
              "left_side_card_badge_text": "Europ",
              "right_side_client_logo": {
                "ID": 7369,
                "id": 7369,
                "title": "image 53",
                "filename": "image-53.svg",
                "filesize": 206515,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                "link": "https://flairstech.flairsrealtor.com/home/image-53",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "image-53",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:02:37",
                "modified": "2025-11-06 22:02:37",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_short_description": "Lorem ipsum dolor sit amet, consectetur",
              "cta_": {
                "title": "",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "card_image": {
                "ID": 7368,
                "id": 7368,
                "title": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "filename": "1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "filesize": 1616495,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "link": "https://flairstech.flairsrealtor.com/home/1029d30a922ae6c512188eb157f60a8ee179951f",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:57",
                "modified": "2025-11-06 22:01:57",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1482,
                "height": 840,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-300x170.png",
                  "medium-width": 300,
                  "medium-height": 170,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-768x435.png",
                  "medium_large-width": 768,
                  "medium_large-height": 435,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-1024x580.png",
                  "large-width": 1024,
                  "large-height": 580,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "1536x1536-width": 1482,
                  "1536x1536-height": 840,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "2048x2048-width": 1482,
                  "2048x2048-height": 840
                }
              },
              "left_side_card_badge_text": "KSA",
              "right_side_client_logo": {
                "ID": 7369,
                "id": 7369,
                "title": "image 53",
                "filename": "image-53.svg",
                "filesize": 206515,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                "link": "https://flairstech.flairsrealtor.com/home/image-53",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "image-53",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:02:37",
                "modified": "2025-11-06 22:02:37",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_short_description": "Lorem ipsum dolor sit amet, consectetur",
              "cta_": {
                "title": "",
                "url": "https://flairstech.com/blog",
                "target": ""
              }
            },
            {
              "card_image": {
                "ID": 7367,
                "id": 7367,
                "title": "a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "filename": "a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                "filesize": 995131,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                "link": "https://flairstech.flairsrealtor.com/home/a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "a23d6be2d62be08db19a6f16c190ae7d7cf21317",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:45",
                "modified": "2025-11-06 22:01:45",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1200,
                "height": 675,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-300x169.png",
                  "medium-width": 300,
                  "medium-height": 169,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-768x432.png",
                  "medium_large-width": 768,
                  "medium_large-height": 432,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317-1024x576.png",
                  "large-width": 1024,
                  "large-height": 576,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                  "1536x1536-width": 1200,
                  "1536x1536-height": 675,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/a23d6be2d62be08db19a6f16c190ae7d7cf21317.png",
                  "2048x2048-width": 1200,
                  "2048x2048-height": 675
                }
              },
              "left_side_card_badge_text": "UAE",
              "right_side_client_logo": {
                "ID": 7369,
                "id": 7369,
                "title": "image 53",
                "filename": "image-53.svg",
                "filesize": 206515,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                "link": "https://flairstech.flairsrealtor.com/home/image-53",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "image-53",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:02:37",
                "modified": "2025-11-06 22:02:37",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_short_description": "Lorem ipsum dolor sit amet, consectetur",
              "cta_": {
                "title": "",
                "url": "https://flairstech.com/services",
                "target": ""
              }
            },
            {
              "card_image": {
                "ID": 7368,
                "id": 7368,
                "title": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "filename": "1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "filesize": 1616495,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "link": "https://flairstech.flairsrealtor.com/home/1029d30a922ae6c512188eb157f60a8ee179951f",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:57",
                "modified": "2025-11-06 22:01:57",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1482,
                "height": 840,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-300x170.png",
                  "medium-width": 300,
                  "medium-height": 170,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-768x435.png",
                  "medium_large-width": 768,
                  "medium_large-height": 435,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-1024x580.png",
                  "large-width": 1024,
                  "large-height": 580,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "1536x1536-width": 1482,
                  "1536x1536-height": 840,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "2048x2048-width": 1482,
                  "2048x2048-height": 840
                }
              },
              "left_side_card_badge_text": "TEst",
              "right_side_client_logo": {
                "ID": 7369,
                "id": 7369,
                "title": "image 53",
                "filename": "image-53.svg",
                "filesize": 206515,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                "link": "https://flairstech.flairsrealtor.com/home/image-53",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "image-53",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:02:37",
                "modified": "2025-11-06 22:02:37",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/image-53.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_short_description": "Lorem ipsum dolor sit amet, consectetur",
              "cta_": {
                "title": "",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            }
          ]
        }
```

## 🧩 Component: `general_testimonials`

### 📐 Fields

| Field Name                        | Type         | Description                                         |
|----------------------------------|--------------|-----------------------------------------------------|
| badge_icon                       | `object`     | Icon image (ACF image array)                        |
| badge_text                       | `string`     | Small badge label shown above heading               |
| heading                          | `string`     | Main heading                                        |
| free_text                        | `string(HTML)` | HTML description text                              |
| cta                              | `object`     | Call to action button with `title`, `url`, `target` |
| upper_testimonials_cards         | `array`      | List of testimonials shown in the upper section     |
| lower_testimonials_cards         | `array`      | List of testimonials shown in the lower section     |

---

### 🧱 Testimonials Card Structure

Each testimonial includes:

| Field                                | Type       | Description                                       |
|--------------------------------------|------------|---------------------------------------------------|
| reviewer_image                       | `object`   | Reviewer image (ACF image array)                  |
| reviewer_name                        | `string`   | Name of the reviewer                              |
| reviewer_job_title_and_company_name | `string`   | Job title and company                             |
| review_content                       | `string(HTML)` | Testimonial content with HTML support         |

---

### ✅ Content Rules

- HTML in `review_content` supports `<p>`, `<strong>`, and `<em>`.
- Upper and lower cards may use same or different testimonial data.
- Headings are wrapped in `<h2>`, free text in `<p>`.
- we will only have h2 which is the headingin this section.

---

### 🧩 Example JSON (as returned by API)

```json
{
          "acf_fc_layout": "general_testimonials",
          "badge_icon": {
            "ID": 7339,
            "id": 7339,
            "title": "Vector",
            "filename": "Vector.svg",
            "filesize": 850,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
            "link": "https://flairstech.flairsrealtor.com/home/vector",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "vector",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:21:30",
            "modified": "2025-11-06 21:21:30",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "badge_text": "What our clients say",
          "heading": "Hear first-hand from our incredible community of customers.",
          "free_text": "\u003Cp\u003EHear first-hand from our incredible community of customers.\u003C/p\u003E\n",
          "cta": {
            "title": "All Testimonials",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          },
          "upper_testimonials_cards": [
            {
              "reviewer_image": {
                "ID": 7372,
                "id": 7372,
                "title": "f4c82c8a581b76f6653078258a28f9a42e75b7f1",
                "filename": "f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                "filesize": 91657,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                "link": "https://flairstech.flairsrealtor.com/home/f4c82c8a581b76f6653078258a28f9a42e75b7f1",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "f4c82c8a581b76f6653078258a28f9a42e75b7f1",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:03",
                "modified": "2025-11-06 22:08:03",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Karim Tahamy",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7373,
                "id": 7373,
                "title": "6239febb788d15352e5535fbad6deaf92bbadfa8",
                "filename": "6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                "filesize": 100275,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                "link": "https://flairstech.flairsrealtor.com/home/6239febb788d15352e5535fbad6deaf92bbadfa8",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "6239febb788d15352e5535fbad6deaf92bbadfa8",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:05",
                "modified": "2025-11-06 22:08:05",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Saleh El-Attar",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7374,
                "id": 7374,
                "title": "061ca1d39a2e8727ab83ff54d7f2ac817230ea0b",
                "filename": "061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                "filesize": 26748,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                "link": "https://flairstech.flairsrealtor.com/home/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "061ca1d39a2e8727ab83ff54d7f2ac817230ea0b",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:07",
                "modified": "2025-11-06 22:08:07",
                "menu_order": 0,
                "mime_type": "image/jpeg",
                "type": "image",
                "subtype": "jpeg",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 400,
                "height": 400,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b-150x150.jpg",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b-300x300.jpg",
                  "medium-width": 300,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "medium_large-width": 400,
                  "medium_large-height": 400,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "large-width": 400,
                  "large-height": 400,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "1536x1536-width": 400,
                  "1536x1536-height": 400,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "2048x2048-width": 400,
                  "2048x2048-height": 400
                }
              },
              "reviewer_name": "Yaser Ayoub",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7375,
                "id": 7375,
                "title": "83ab462a89a08fdba266b544d03bce6d41e497cd",
                "filename": "83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                "filesize": 85996,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                "link": "https://flairstech.flairsrealtor.com/home/83ab462a89a08fdba266b544d03bce6d41e497cd",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "83ab462a89a08fdba266b544d03bce6d41e497cd",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:10",
                "modified": "2025-11-06 22:08:10",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Ahmed El-Attar",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7376,
                "id": 7376,
                "title": "4db2c58ee144939af54a2e2c4062c663362d6e55",
                "filename": "4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                "filesize": 69702,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                "link": "https://flairstech.flairsrealtor.com/home/4db2c58ee144939af54a2e2c4062c663362d6e55",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "4db2c58ee144939af54a2e2c4062c663362d6e55",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:11",
                "modified": "2025-11-06 22:08:11",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Sabry Al-Attar",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            }
          ],
          "lower_testimonials_cards": [
            {
              "reviewer_image": {
                "ID": 7372,
                "id": 7372,
                "title": "f4c82c8a581b76f6653078258a28f9a42e75b7f1",
                "filename": "f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                "filesize": 91657,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                "link": "https://flairstech.flairsrealtor.com/home/f4c82c8a581b76f6653078258a28f9a42e75b7f1",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "f4c82c8a581b76f6653078258a28f9a42e75b7f1",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:03",
                "modified": "2025-11-06 22:08:03",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/f4c82c8a581b76f6653078258a28f9a42e75b7f1.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Ahmed El-Attar",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7373,
                "id": 7373,
                "title": "6239febb788d15352e5535fbad6deaf92bbadfa8",
                "filename": "6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                "filesize": 100275,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                "link": "https://flairstech.flairsrealtor.com/home/6239febb788d15352e5535fbad6deaf92bbadfa8",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "6239febb788d15352e5535fbad6deaf92bbadfa8",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:05",
                "modified": "2025-11-06 22:08:05",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/6239febb788d15352e5535fbad6deaf92bbadfa8.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Yaser Ayoub",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7374,
                "id": 7374,
                "title": "061ca1d39a2e8727ab83ff54d7f2ac817230ea0b",
                "filename": "061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                "filesize": 26748,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                "link": "https://flairstech.flairsrealtor.com/home/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "061ca1d39a2e8727ab83ff54d7f2ac817230ea0b",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:07",
                "modified": "2025-11-06 22:08:07",
                "menu_order": 0,
                "mime_type": "image/jpeg",
                "type": "image",
                "subtype": "jpeg",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 400,
                "height": 400,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b-150x150.jpg",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b-300x300.jpg",
                  "medium-width": 300,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "medium_large-width": 400,
                  "medium_large-height": 400,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "large-width": 400,
                  "large-height": 400,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "1536x1536-width": 400,
                  "1536x1536-height": 400,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/061ca1d39a2e8727ab83ff54d7f2ac817230ea0b.jpg",
                  "2048x2048-width": 400,
                  "2048x2048-height": 400
                }
              },
              "reviewer_name": "Saleh El-Attar",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7375,
                "id": 7375,
                "title": "83ab462a89a08fdba266b544d03bce6d41e497cd",
                "filename": "83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                "filesize": 85996,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                "link": "https://flairstech.flairsrealtor.com/home/83ab462a89a08fdba266b544d03bce6d41e497cd",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "83ab462a89a08fdba266b544d03bce6d41e497cd",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:10",
                "modified": "2025-11-06 22:08:10",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/83ab462a89a08fdba266b544d03bce6d41e497cd.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Karim Tahamy",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            },
            {
              "reviewer_image": {
                "ID": 7376,
                "id": 7376,
                "title": "4db2c58ee144939af54a2e2c4062c663362d6e55",
                "filename": "4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                "filesize": 69702,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                "link": "https://flairstech.flairsrealtor.com/home/4db2c58ee144939af54a2e2c4062c663362d6e55",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "4db2c58ee144939af54a2e2c4062c663362d6e55",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:08:11",
                "modified": "2025-11-06 22:08:11",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 200,
                "height": 200,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "medium-width": 200,
                  "medium-height": 200,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "medium_large-width": 200,
                  "medium_large-height": 200,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "large-width": 200,
                  "large-height": 200,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "1536x1536-width": 200,
                  "1536x1536-height": 200,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/4db2c58ee144939af54a2e2c4062c663362d6e55.png",
                  "2048x2048-width": 200,
                  "2048x2048-height": 200
                }
              },
              "reviewer_name": "Sabry Al-Attar",
              "reviewer_job_title_and_company_name": "Client Title, Company Name",
              "review_content": "\u003Cp\u003ELorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget efficitur mauris, nec vestibulum erat. In id convallis turpis, non malesuada risus.\u003C/p\u003E\n"
            }
          ]
        },
```
## 🏭 industries_with_clickable_text_to_show_images

This layout is designed to present clickable industry names on the left, showing corresponding images and content on the right.

### 📐 Fields

| Field Name                          | Type       | Description                                                                 |
|------------------------------------|------------|-----------------------------------------------------------------------------|
| acf_fc_layout                      | `string`   | Layout identifier                                                           |
| badge_icon                         | `object`   | Image object for the badge icon                                            |
| badge_text                         | `string`   | Text displayed on the badge                                                |
| heading                            | `string`   | Main heading                                                               |
| industry_repeater                  | `array`    | List of industries (clickable items)                                       |
| general_cta                        | `object`   | CTA button at the bottom (title, url, target)                              |

### 🧱 Industry Repeater Structure

Each item in `industry_repeater` includes:

| Field Name                          | Type       | Description                                                                 |
|------------------------------------|------------|-----------------------------------------------------------------------------|
| left_side_industry_name            | `string`   | Industry name shown on the left side                                        |
| right_side_large_bg_image          | `object`   | Background image object shown on right side                                |
| icon_before_right_side_card_heading | `object`   | Icon object shown before the heading                                        |
| right_side_card_heading_after_icon | `string`   | Heading text after the icon on the right                                   |
| right_side_short_paragraph         | `string`   | Paragraph of text displayed next to the image                              |
| right_side_card_cta                | `object`   | CTA button with `title`, `url`, `target`                                   |
---
### ✅ Content Rules

- HTML in `free text` supports `<p>`, `<strong>`, and `<em>`.
- Headings are wrapped in `<h2>`, free text in `<p>`.
- we will only have h2 which is the headingin this section.
- right side heading is p tag

```json
  {
          "acf_fc_layout": "industries_with_clickable_text_to_show_images",
          "badge_icon": {
            "ID": 7340,
            "id": 7340,
            "title": "circle",
            "filename": "circle.svg",
            "filesize": 1292,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
            "link": "https://flairstech.flairsrealtor.com/home/circle",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "circle",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 21:21:35",
            "modified": "2025-11-06 21:21:35",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "badge_text": "Industries we serve",
          "heading": "Serving sectors, creating impact",
          "industry_repeater": [
            {
              "left_side_industry_name": "Travel",
              "right_side_large_bg_image": {
                "ID": 7379,
                "id": 7379,
                "title": "Frame 1618873053",
                "filename": "Frame-1618873053.png",
                "filesize": 1063436,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                "link": "https://flairstech.flairsrealtor.com/home/frame-1618873053",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "frame-1618873053",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:12:28",
                "modified": "2025-11-06 22:12:28",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 646,
                "height": 835,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053-232x300.png",
                  "medium-width": 232,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "medium_large-width": 646,
                  "medium_large-height": 835,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "large-width": 646,
                  "large-height": 835,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "1536x1536-width": 646,
                  "1536x1536-height": 835,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "2048x2048-width": 646,
                  "2048x2048-height": 835
                }
              },
              "icon_before_right_side_card_heading": {
                "ID": 7380,
                "id": 7380,
                "title": "Icon",
                "filename": "Icon.svg",
                "filesize": 1125,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                "link": "https://flairstech.flairsrealtor.com/home/icon",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "icon",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:12:59",
                "modified": "2025-11-06 22:12:59",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Icon.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "right_side_card_heading_after_icon": "Travel",
              "right_side_short_paragraph": "\u003Cp\u003EEmpowering travel platforms with seamless booking systems, personalized user experiences, and real-time analytics.\u003C/p\u003E\n",
              "right_side_card_cta": {
                "title": "Read More",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "left_side_industry_name": "Healthcare",
              "right_side_large_bg_image": {
                "ID": 7382,
                "id": 7382,
                "title": "Frame 1618873056",
                "filename": "Frame-1618873056.png",
                "filesize": 865486,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                "link": "https://flairstech.flairsrealtor.com/home/frame-1618873056",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "frame-1618873056",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:15:36",
                "modified": "2025-11-06 22:15:36",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 646,
                "height": 835,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056-232x300.png",
                  "medium-width": 232,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "medium_large-width": 646,
                  "medium_large-height": 835,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "large-width": 646,
                  "large-height": 835,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "1536x1536-width": 646,
                  "1536x1536-height": 835,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "2048x2048-width": 646,
                  "2048x2048-height": 835
                }
              },
              "icon_before_right_side_card_heading": {
                "ID": 7338,
                "id": 7338,
                "title": "settings",
                "filename": "settings.svg",
                "filesize": 4295,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                "link": "https://flairstech.flairsrealtor.com/home/settings",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "settings",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:22",
                "modified": "2025-11-06 21:21:22",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/settings.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "right_side_card_heading_after_icon": "Healthcare",
              "right_side_short_paragraph": "\u003Cp\u003EEmpowering travel platforms with seamless booking systems, personalized user experiences, and real-time analytics.\u003C/p\u003E\n",
              "right_side_card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "left_side_industry_name": "Banking",
              "right_side_large_bg_image": {
                "ID": 7379,
                "id": 7379,
                "title": "Frame 1618873053",
                "filename": "Frame-1618873053.png",
                "filesize": 1063436,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                "link": "https://flairstech.flairsrealtor.com/home/frame-1618873053",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "frame-1618873053",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:12:28",
                "modified": "2025-11-06 22:12:28",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 646,
                "height": 835,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053-232x300.png",
                  "medium-width": 232,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "medium_large-width": 646,
                  "medium_large-height": 835,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "large-width": 646,
                  "large-height": 835,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "1536x1536-width": 646,
                  "1536x1536-height": 835,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "2048x2048-width": 646,
                  "2048x2048-height": 835
                }
              },
              "icon_before_right_side_card_heading": {
                "ID": 7339,
                "id": 7339,
                "title": "Vector",
                "filename": "Vector.svg",
                "filesize": 850,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                "link": "https://flairstech.flairsrealtor.com/home/vector",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "vector",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:30",
                "modified": "2025-11-06 21:21:30",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Vector.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "right_side_card_heading_after_icon": "Banking",
              "right_side_short_paragraph": "\u003Cp\u003EEmpowering travel platforms with seamless booking systems, personalized user experiences, and real-time analytics.\u003C/p\u003E\n",
              "right_side_card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "left_side_industry_name": "Telecommunication",
              "right_side_large_bg_image": {
                "ID": 7382,
                "id": 7382,
                "title": "Frame 1618873056",
                "filename": "Frame-1618873056.png",
                "filesize": 865486,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                "link": "https://flairstech.flairsrealtor.com/home/frame-1618873056",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "frame-1618873056",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:15:36",
                "modified": "2025-11-06 22:15:36",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 646,
                "height": 835,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056-232x300.png",
                  "medium-width": 232,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "medium_large-width": 646,
                  "medium_large-height": 835,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "large-width": 646,
                  "large-height": 835,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "1536x1536-width": 646,
                  "1536x1536-height": 835,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "2048x2048-width": 646,
                  "2048x2048-height": 835
                }
              },
              "icon_before_right_side_card_heading": {
                "ID": 7340,
                "id": 7340,
                "title": "circle",
                "filename": "circle.svg",
                "filesize": 1292,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                "link": "https://flairstech.flairsrealtor.com/home/circle",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "circle",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:21:35",
                "modified": "2025-11-06 21:21:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/circle.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "right_side_card_heading_after_icon": "Telecommunication",
              "right_side_short_paragraph": "\u003Cp\u003EEmpowering travel platforms with seamless booking systems, personalized user experiences, and real-time analytics.\u003C/p\u003E\n",
              "right_side_card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "left_side_industry_name": "Automotive",
              "right_side_large_bg_image": {
                "ID": 7382,
                "id": 7382,
                "title": "Frame 1618873056",
                "filename": "Frame-1618873056.png",
                "filesize": 865486,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                "link": "https://flairstech.flairsrealtor.com/home/frame-1618873056",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "frame-1618873056",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:15:36",
                "modified": "2025-11-06 22:15:36",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 646,
                "height": 835,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056-232x300.png",
                  "medium-width": 232,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "medium_large-width": 646,
                  "medium_large-height": 835,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "large-width": 646,
                  "large-height": 835,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "1536x1536-width": 646,
                  "1536x1536-height": 835,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873056.png",
                  "2048x2048-width": 646,
                  "2048x2048-height": 835
                }
              },
              "icon_before_right_side_card_heading": {
                "ID": 7345,
                "id": 7345,
                "title": "Primary",
                "filename": "Primary.svg",
                "filesize": 1115,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                "link": "https://flairstech.flairsrealtor.com/home/primary",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "primary",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:30:06",
                "modified": "2025-11-06 21:30:06",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "right_side_card_heading_after_icon": "Automotive",
              "right_side_short_paragraph": "\u003Cp\u003EEmpowering travel platforms with seamless booking systems, personalized user experiences, and real-time analytics.\u003C/p\u003E\n",
              "right_side_card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "left_side_industry_name": "Transportation",
              "right_side_large_bg_image": {
                "ID": 7379,
                "id": 7379,
                "title": "Frame 1618873053",
                "filename": "Frame-1618873053.png",
                "filesize": 1063436,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                "link": "https://flairstech.flairsrealtor.com/home/frame-1618873053",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "frame-1618873053",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:12:28",
                "modified": "2025-11-06 22:12:28",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 646,
                "height": 835,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053-232x300.png",
                  "medium-width": 232,
                  "medium-height": 300,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "medium_large-width": 646,
                  "medium_large-height": 835,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "large-width": 646,
                  "large-height": 835,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "1536x1536-width": 646,
                  "1536x1536-height": 835,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Frame-1618873053.png",
                  "2048x2048-width": 646,
                  "2048x2048-height": 835
                }
              },
              "icon_before_right_side_card_heading": {
                "ID": 7366,
                "id": 7366,
                "title": "Primary (3)",
                "filename": "Primary-3.svg",
                "filesize": 2256,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                "link": "https://flairstech.flairsrealtor.com/home/primary-3",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "primary-3",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 21:57:35",
                "modified": "2025-11-06 21:57:35",
                "menu_order": 0,
                "mime_type": "image/svg+xml",
                "type": "image",
                "subtype": "svg+xml",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 0,
                "height": 0,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                  "thumbnail-width": 1,
                  "thumbnail-height": 1,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                  "medium-width": 1,
                  "medium-height": 1,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                  "medium_large-width": 1,
                  "medium_large-height": 1,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                  "large-width": 1,
                  "large-height": 1,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                  "1536x1536-width": 1,
                  "1536x1536-height": 1,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-3.svg",
                  "2048x2048-width": 1,
                  "2048x2048-height": 1
                }
              },
              "right_side_card_heading_after_icon": "Transportation",
              "right_side_short_paragraph": "\u003Cp\u003EEmpowering travel platforms with seamless booking systems, personalized user experiences, and real-time analytics.\u003C/p\u003E\n",
              "right_side_card_cta": {
                "title": "BOOK NOW",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            }
          ],
          "general_cta": {
            "title": "All Industries",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          }
        },


```
## 🎯 `cta_with_bg_purple_and_white_text`  
This component displays a call-to-action (CTA) section with a **purple background** and **white text**, used to highlight strategic actions like booking consultations. It includes a badge icon, headline, descriptive text, and a CTA button.

Heading is H2 and and you have to handle the free text .
the background will be static .
### 📐 Fields:
| Field Name       | Type     | Description                                                                 |
|------------------|----------|-----------------------------------------------------------------------------|
| `badge_icon`     | `object` | Image object used as a badge/icon (full ACF image object – includes URL, alt, etc.) |
| `badge_text`     | `string` | Small label shown near the badge (e.g., "Schedule a meeting")              |
| `left_heading`   | `string` | Main heading on the left side (e.g., "What can you improve today?")        |
| `right_free_text`| `string` | Descriptive paragraph or HTML content on the right                         |
| `cta`            | `object` | Call-to-action object with `title`, `url`, and optional `target`           |

### ✅ Example Data:
```json
  {
          "acf_fc_layout": "cta_with_bg_purple_and_white_text",
          "badge_icon": {
            "ID": 7394,
            "id": 7394,
            "title": "Primary (4)",
            "filename": "Primary-4.svg",
            "filesize": 1471,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
            "link": "https://flairstech.flairsrealtor.com/home/primary-4",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "primary-4",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 22:23:36",
            "modified": "2025-11-06 22:23:36",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-4.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "badge_text": "Schedule a meeting",
          "left_heading": "What can you improve today?",
          "right_free_text": "\u003Cp\u003EWith decades of combined experience, our specialists across regions are well-prepared for any challenge you may be facing\u003C/p\u003E\n",
          "cta": {
            "title": "Book a free consultation",
            "url": "https://flairstech.com/contact-us/book",
            "target": ""
          }
        },
```
## 🧩 Component: `blogs_and_news_manual_insertion`

This section manually lists news/blog cards with images and CTAs, using static data (not auto pulled). It is used to showcase selected content like press releases or thought leadership blogs.

### 📐 Fields

| Field Name         | Type     | Description                                             |
|--------------------|----------|---------------------------------------------------------|
| badge_icon         | `object` | Image object used as badge icon                         |
| badge_text         | `string` | Small label text above the main heading                 |
| heading            | `string` | Section heading                                         |
| repeated_cards     | `array`  | List of blog/news cards (see structure below)           |
| last_card_cta      | `object` | Final CTA button with `title`, `url`, and `target`      |

### 🧱 Blog / News Cards Structure

Each item in `repeated_cards` includes:

| Field                | Type     | Description                                         |
|---------------------|----------|-----------------------------------------------------|
| card_badge_text     | `string` | A label such as "Blog" or "News"                    |
| card_image          | `object` | ACF image object (thumbnail, alt, etc.)             |
| card_heading        | `string` | Title of the article or news                        |
| card_cta            | `object` | CTA object including `title`, `url`, and `target`   |

---

### 📦 Notes for Development

- The layout allows flexible manual selection of featured blogs.
- Each card should render an image, badge, heading, and CTA.
- Images must support responsive behavior (`srcset`, `sizes`).
- Consider lazy-loading images for performance.
- Use `<section>` with semantic tags like `<article>` per card.
- Card Titles are h3 
- Section heading is H2

---

### 🧪 Example JSON

```json
  {
          "acf_fc_layout": "blogs_and_news_manual_insertion",
          "badge_icon": {
            "ID": 7401,
            "id": 7401,
            "title": "Primary (5)",
            "filename": "Primary-5.svg",
            "filesize": 858,
            "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
            "link": "https://flairstech.flairsrealtor.com/home/primary-5",
            "alt": "",
            "author": "17",
            "description": "",
            "caption": "",
            "name": "primary-5",
            "status": "inherit",
            "uploaded_to": 5082,
            "date": "2025-11-06 22:25:58",
            "modified": "2025-11-06 22:25:58",
            "menu_order": 0,
            "mime_type": "image/svg+xml",
            "type": "image",
            "subtype": "svg+xml",
            "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
            "width": 0,
            "height": 0,
            "sizes": {
              "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
              "thumbnail-width": 1,
              "thumbnail-height": 1,
              "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
              "medium-width": 1,
              "medium-height": 1,
              "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
              "medium_large-width": 1,
              "medium_large-height": 1,
              "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
              "large-width": 1,
              "large-height": 1,
              "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
              "1536x1536-width": 1,
              "1536x1536-height": 1,
              "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/Primary-5.svg",
              "2048x2048-width": 1,
              "2048x2048-height": 1
            }
          },
          "badge_text": "Latest News",
          "heading": "Keep updated with our news and blog",
          "repeated_cards": [
            {
              "card_badge_text": "blog",
              "card_image": {
                "ID": 7402,
                "id": 7402,
                "title": "d39e17085325bb86e2740d2674ef754e2e5c137f",
                "filename": "d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                "filesize": 1144242,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                "link": "https://flairstech.flairsrealtor.com/home/d39e17085325bb86e2740d2674ef754e2e5c137f",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "d39e17085325bb86e2740d2674ef754e2e5c137f",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:28:20",
                "modified": "2025-11-06 22:28:20",
                "menu_order": 0,
                "mime_type": "image/jpeg",
                "type": "image",
                "subtype": "jpeg",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1500,
                "height": 971,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-150x150.jpg",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-300x194.jpg",
                  "medium-width": 300,
                  "medium-height": 194,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-768x497.jpg",
                  "medium_large-width": 768,
                  "medium_large-height": 497,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-1024x663.jpg",
                  "large-width": 1024,
                  "large-height": 663,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                  "1536x1536-width": 1500,
                  "1536x1536-height": 971,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                  "2048x2048-width": 1500,
                  "2048x2048-height": 971
                }
              },
              "card_heading": "Sales Support Team Functions Your Business Need in 2025",
              "card_cta": {
                "title": "Read Article",
                "url": "https://flairstech.com/blog",
                "target": ""
              }
            },
            {
              "card_badge_text": "News",
              "card_image": {
                "ID": 7403,
                "id": 7403,
                "title": "296c7d98b214bbd0a52db12f69312a945e6c0e95",
                "filename": "296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                "filesize": 1170688,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                "link": "https://flairstech.flairsrealtor.com/home/296c7d98b214bbd0a52db12f69312a945e6c0e95",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "296c7d98b214bbd0a52db12f69312a945e6c0e95",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:28:27",
                "modified": "2025-11-06 22:28:27",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1472,
                "height": 832,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-300x170.png",
                  "medium-width": 300,
                  "medium-height": 170,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-768x434.png",
                  "medium_large-width": 768,
                  "medium_large-height": 434,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-1024x579.png",
                  "large-width": 1024,
                  "large-height": 579,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                  "1536x1536-width": 1472,
                  "1536x1536-height": 832,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                  "2048x2048-width": 1472,
                  "2048x2048-height": 832
                }
              },
              "card_heading": "Do Customers like AI Customer Support? Find Out!",
              "card_cta": {
                "title": "Read Article",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "card_badge_text": "Blog",
              "card_image": {
                "ID": 7404,
                "id": 7404,
                "title": "23cbe888a5d29f78947d18b0109974e00906d8fd (1)",
                "filename": "23cbe888a5d29f78947d18b0109974e00906d8fd-1.png",
                "filesize": 1272419,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1.png",
                "link": "https://flairstech.flairsrealtor.com/home/23cbe888a5d29f78947d18b0109974e00906d8fd-1",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "23cbe888a5d29f78947d18b0109974e00906d8fd-1",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:28:39",
                "modified": "2025-11-06 22:28:39",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1920,
                "height": 1080,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1-300x169.png",
                  "medium-width": 300,
                  "medium-height": 169,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1-768x432.png",
                  "medium_large-width": 768,
                  "medium_large-height": 432,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1-1024x576.png",
                  "large-width": 1024,
                  "large-height": 576,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1-1536x864.png",
                  "1536x1536-width": 1536,
                  "1536x1536-height": 864,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/23cbe888a5d29f78947d18b0109974e00906d8fd-1.png",
                  "2048x2048-width": 1920,
                  "2048x2048-height": 1080
                }
              },
              "card_heading": "AI in Software Maintenance Support: What is New?",
              "card_cta": {
                "title": "Read Article",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "card_badge_text": "Blog",
              "card_image": {
                "ID": 7368,
                "id": 7368,
                "title": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "filename": "1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "filesize": 1616495,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                "link": "https://flairstech.flairsrealtor.com/home/1029d30a922ae6c512188eb157f60a8ee179951f",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "1029d30a922ae6c512188eb157f60a8ee179951f",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:01:57",
                "modified": "2025-11-06 22:01:57",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1482,
                "height": 840,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-300x170.png",
                  "medium-width": 300,
                  "medium-height": 170,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-768x435.png",
                  "medium_large-width": 768,
                  "medium_large-height": 435,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f-1024x580.png",
                  "large-width": 1024,
                  "large-height": 580,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "1536x1536-width": 1482,
                  "1536x1536-height": 840,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/1029d30a922ae6c512188eb157f60a8ee179951f.png",
                  "2048x2048-width": 1482,
                  "2048x2048-height": 840
                }
              },
              "card_heading": "AI, Artificial Intelligence, AI Technology, Applications - RWS",
              "card_cta": {
                "title": "Read Article",
                "url": "https://flairstech.com/blog",
                "target": ""
              }
            },
            {
              "card_badge_text": "News",
              "card_image": {
                "ID": 7402,
                "id": 7402,
                "title": "d39e17085325bb86e2740d2674ef754e2e5c137f",
                "filename": "d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                "filesize": 1144242,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                "link": "https://flairstech.flairsrealtor.com/home/d39e17085325bb86e2740d2674ef754e2e5c137f",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "d39e17085325bb86e2740d2674ef754e2e5c137f",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:28:20",
                "modified": "2025-11-06 22:28:20",
                "menu_order": 0,
                "mime_type": "image/jpeg",
                "type": "image",
                "subtype": "jpeg",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1500,
                "height": 971,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-150x150.jpg",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-300x194.jpg",
                  "medium-width": 300,
                  "medium-height": 194,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-768x497.jpg",
                  "medium_large-width": 768,
                  "medium_large-height": 497,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f-1024x663.jpg",
                  "large-width": 1024,
                  "large-height": 663,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                  "1536x1536-width": 1500,
                  "1536x1536-height": 971,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/d39e17085325bb86e2740d2674ef754e2e5c137f.jpg",
                  "2048x2048-width": 1500,
                  "2048x2048-height": 971
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_cta": {
                "title": "Read Article",
                "url": "https://flairstech.com/contact-us/book",
                "target": ""
              }
            },
            {
              "card_badge_text": "Blog",
              "card_image": {
                "ID": 7403,
                "id": 7403,
                "title": "296c7d98b214bbd0a52db12f69312a945e6c0e95",
                "filename": "296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                "filesize": 1170688,
                "url": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                "link": "https://flairstech.flairsrealtor.com/home/296c7d98b214bbd0a52db12f69312a945e6c0e95",
                "alt": "",
                "author": "17",
                "description": "",
                "caption": "",
                "name": "296c7d98b214bbd0a52db12f69312a945e6c0e95",
                "status": "inherit",
                "uploaded_to": 5082,
                "date": "2025-11-06 22:28:27",
                "modified": "2025-11-06 22:28:27",
                "menu_order": 0,
                "mime_type": "image/png",
                "type": "image",
                "subtype": "png",
                "icon": "https://flairstech.flairsrealtor.com/wp/wp-includes/images/media/default.png",
                "width": 1472,
                "height": 832,
                "sizes": {
                  "thumbnail": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-150x150.png",
                  "thumbnail-width": 150,
                  "thumbnail-height": 150,
                  "medium": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-300x170.png",
                  "medium-width": 300,
                  "medium-height": 170,
                  "medium_large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-768x434.png",
                  "medium_large-width": 768,
                  "medium_large-height": 434,
                  "large": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95-1024x579.png",
                  "large-width": 1024,
                  "large-height": 579,
                  "1536x1536": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                  "1536x1536-width": 1472,
                  "1536x1536-height": 832,
                  "2048x2048": "https://flairstech.flairsrealtor.com/app/uploads/2025/11/296c7d98b214bbd0a52db12f69312a945e6c0e95.png",
                  "2048x2048-width": 1472,
                  "2048x2048-height": 832
                }
              },
              "card_heading": "Lorem Ipsum is simply dummy text of the ",
              "card_cta": {
                "title": "Read Article",
                "url": "https://flairstech.com/blog",
                "target": ""
              }
            }
          ],
          "last_card_cta": {
            "title": "Read More",
            "url": "https://flairstech.com/blog",
            "target": ""
          }
        }
```

# Layout: General FAQ (`general_faq`)

## Purpose
Display a frequently asked questions (FAQ) section with a main heading, subheading, description, and list of questions with answers.

---

## Fields

| Field Name      | Type     | Description                                                   |
|-----------------|----------|---------------------------------------------------------------|
| `acf_fc_layout` | string   | Layout identifier. Always set to `general_faq`.              |
| `heading`       | string   | Main heading for the FAQ section.                             |
| `sub_heading`   | string   | Subtitle shown below the main heading.                        |
| `free_text`     | WYSIWYG  | Rich text field for introductory or descriptive content.       |
| `faq_repeater`  | repeater | A list of question/answer pairs.                              |
| `faq_repeater[].question` | string | The FAQ question.                                 |
| `faq_repeater[].answer`   | WYSIWYG | Rich text answer (can contain HTML).              |

---

## Example JSON

```json
  {
          "acf_fc_layout": "general_faq",
          "heading": "Frequently Asked Questions",
          "sub_heading": "Seeking Basic Information?",
          "free_text": "\u003Cp\u003EOur FAQ section is a ready reckoner with precise answers to the most probable queries\u003C/p\u003E\n",
          "faq_repeater": [
            {
              "question": "What is FlairsTech and what do you specialize in?",
              "answer": "\u003Cp\u003EFlairsTech is a technology-driven managed services provider. We deliver end-to-end solutions including technical support, application maintenance, IT help desk, PMO (project management), customer experience (CX), sales support, accounting, and more. We integrate \u003Cstrong\u003Eseamlessly into your operations\u003C/strong\u003E to simplify workflows, reduce overhead, and drive growth.\u003C/p\u003E\n"
            },
            {
              "question": "Who are your typical clients / industries you serve?",
              "answer": "\u003Cp\u003EFlairsTech is a technology-driven managed services provider. We deliver end-to-end solutions including technical support, application maintenance, IT help desk, PMO (project management), customer experience (CX), sales support, accounting, and more. We integrate \u003Cstrong\u003Eseamlessly into your operations\u003C/strong\u003E to simplify workflows, reduce overhead, and drive growth.\u003C/p\u003E\n"
            },
            {
              "question": "What makes FlairsTech different from other managed services providers?",
              "answer": "\u003Cp\u003EFlairsTech is a technology-driven managed services provider. We deliver end-to-end solutions including technical support, application maintenance, IT help desk, PMO (project management), customer experience (CX), sales support, accounting, and more. We integrate \u003Cstrong\u003Eseamlessly into your operations\u003C/strong\u003E to simplify workflows, reduce overhead, and drive growth.\u003C/p\u003E\n"
            },
            {
              "question": "How do you begin working with a new client?",
              "answer": "\u003Cp\u003EFlairsTech is a technology-driven managed services provider. We deliver end-to-end solutions including technical support, application maintenance, IT help desk, PMO (project management), customer experience (CX), sales support, accounting, and more. We integrate \u003Cstrong\u003Eseamlessly into your operations\u003C/strong\u003E to simplify workflows, reduce overhead, and drive growth.\u003C/p\u003E\n"
            }
          ]
        }

```

## Developer Notes

- All answers support HTML formatting.
- Use `<details>` / `<summary>` elements or Accordion component in frontend.
- Sanitize WYSIWYG content if rendering user inputs.

