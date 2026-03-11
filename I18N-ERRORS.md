# Multi-language Error Messages (i18n)

Design principle: return a stable error code (for systems) and a localized message (for humans). The code stays the same across languages.

## Table: ERROR_MESSAGES
- error_code (e.g., BANK_DECLINED, RISK_REJECTED)
- language_code (e.g., en, bg, tl)
- message (translated text)

Primary key: (error_code, language_code)

## Behavior
- Select language via Accept-Language header or merchant default
- If translation is missing, fallback to English
