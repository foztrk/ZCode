## Summary

This PR adds native **Turkish (`tr-TR`)** language support to ZCode, providing comprehensive localization for Turkish developers with 100% key parity against v3.16.2 (over 7,310 i18n keys).

Following guidance from the Z.ai Developer Support team, this contribution brings full upstream Turkish support directly to the official codebase.

---

## Changes

1. **`packages/ui/src/i18n/locales/tr-TR.ts`**
   - Added complete Turkish locale dictionary containing **7,311 keys**.
   - Fully covers Desktop Shell, Chat, Settings, MCP Form & Configuration, Remote SSH/Docker/WSL Sources, Skills & Commands, and Plugin Marketplace.

2. **`packages/shared/src/protocol.ts`**
   - Extended `Locale` type to `"zh-CN" | "en-US" | "tr-TR"`.

3. **`packages/ui/src/i18n/IntlProvider.tsx`**
   - Registered `tr-TR` translations in `MESSAGES` mapping.

4. **`packages/ui/src/i18n/LocaleSwitcher.tsx`**
   - Added `tr-TR` ("Tr") to the locale cycle and label dictionary.

---

## Verification & Testing

- **Local Verification:** Verified against live ZCode v3.16.2 client on Windows 11 x64.
- **UI Integrity:** Confirmed accurate rendering across:
  - Main workspace, Chat & Composer
  - Settings (Model Providers, MCP, Remote Devices, Docker/SSH)
  - Plugin Marketplace & Skills catalog
  - Markdown tables, tooltips, and contextual action menus
- **Syntax & Schema:** Validated TypeScript export schema and placeholder parameters (`{count}`, `{name}`, `{time}`, etc.) for complete consistency with `en-US.ts`.

---

Thank you to the ZCode team for building such a great open-source harness! Looking forward to having native Turkish available in future official releases.
