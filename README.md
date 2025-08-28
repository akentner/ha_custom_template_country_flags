[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)
![Version](https://img.shields.io/github/v/release/akentner/home-assistant-custom-template-country-flags)
[![Buy me a coffe](https://img.shields.io/static/v1.svg?label=%20&message=Buy%20me%20a%20coffee&color=6f4e37&logo=buy%20me%20a%20coffee&logoColor=white)](https://buymeacoffee.com/akentner)
[![Paypal](https://img.shields.io/badge/PayPal-00457C?&color=00457c&logo=paypal&logoColor=white)](https://www.paypal.com/paypalme/akentner)


# Country Flag Custom Template for Home Assistant
  
Generates flag emojis and Twemoji URLs from country names or ISO-2 codes.

Features:
- 190+ countries with multilingual name support
- Dynamic Unicode calculation for flag emojis
- Twemoji PNG/SVG URLs with different sizes
- Accent character normalization
- Robust input validation and error handling

## How to install
Home Assistant 2025.8 or higher is required to use this macro (perhaps also below, did not test it).

This custom template is compatible with [HACS](https://hacs.xyz/), which means that you can easily download and manage updates for it. Custom templates are supported in HACS 2.0 or when you enable experimental features in the HACS settings of versions prior to 2.0. 

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=akentner&repository=home-assistant-custom-template-country-flags&category=template)


For a manual install you can copy the contents of `country_flags.jinja` to a jinja file in your `custom_templates` folder.
Run the `homeassistant.reload_custom_templates` service call to load the file.


## Usage

`{%- from 'country_flags.jinja' import flag_emoji, flag_svg, flag_png, flag_info -%}`

Examples:
- `{{ flag_emoji('Germany') }}`     → 🇩🇪
- `{{ flag_png('DE') }}`           → PNG URL
- `{{ flag_svg('Deutschland') }}`  → SVG URL
- `{{ flag_info('Japan') }}`       → Complete info as JSON


Author: Alexander Kentner <github@akentner.de>

Version: 1.0
