# Country Flag Custom Template for Home Assistant
  
Generates flag emojis and Twemoji URLs from country names or ISO-2 codes.

Features:
- 190+ countries with multilingual name support
- Dynamic Unicode calculation for flag emojis
- Twemoji PNG/SVG URLs with different sizes
- Accent character normalization
- Robust input validation and error handling

Usage:
------
`{%- from 'country_flags.jinja' import flag_emoji, flag_svg, flag_png, flag_info -%}`

Examples:
- `{{ flag_emoji('Germany') }}`     → 🇩🇪
- `{{ flag_png('DE') }}`           → PNG URL
- `{{ flag_svg('Deutschland') }}`  → SVG URL
- `{{ flag_info('Japan') }}`       → Complete info as JSON


Author: Alexander Kentner <github@akentner.de>

Version: 1.0
