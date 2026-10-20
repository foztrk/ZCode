### Update for ZCode v3.16.2: 100% Translation Parity (7,311 Keys) & Ready Upstream Branch

Following the helpful guidance from the Z.ai Developer Support team, we have completed the full Turkish localization update for the latest **ZCode v3.16.2** release and prepared the complete upstream integration branch.

#### 1. Implementation Details
The native integration is prepared in accordance with ZCode's monorepo architecture on our fork:
- 🔗 **Branch:** [foztrk/ZCode@feat/add-turkish-language-support](https://github.com/foztrk/ZCode/tree/feat/add-turkish-language-support)
- 🔗 **Direct Commit:** [a6f4c92](https://github.com/foztrk/ZCode/commit/a6f4c92454641982b6832db441e9766935c102a7)

**Key Files Changed:**
- `packages/ui/src/i18n/locales/tr-TR.ts`: Comprehensive Turkish locale dictionary containing **7,311 keys** with 100% coverage (Desktop, Chat, Settings, MCP, Tools, Remote SSH/Docker sources, Plugin Store, and Skills).
- `packages/shared/src/protocol.ts`: Extended `Locale` union type to `"zh-CN" | "en-US" | "tr-TR"`.
- `packages/ui/src/i18n/IntlProvider.tsx`: Registered `tr-TR` message dictionary in `MESSAGES`.
- `packages/ui/src/i18n/LocaleSwitcher.tsx`: Added `tr-TR` (`"Tr"`) to the language cycle selector.

#### 2. Note on Pull Request
We attempted to open a PR directly to `zai-org/ZCode`, but the repository currently restricts `CreatePullRequest` permissions for external contributors. 
Therefore, maintainers can directly pull or cherry-pick the changes from our branch:
```bash
git remote add foztrk https://github.com/foztrk/ZCode.git
git fetch foztrk feat/add-turkish-language-support
git merge foztrk/feat/add-turkish-language-support
```

#### 3. Verification
The changes have been thoroughly tested on Windows 11 x64 with real-world workloads, ensuring zero UI overflows, correct pluralization/parameter interpolation (`{count}`, `{name}`, etc.), and adherence to standard developer terminology.

We would be delighted to see native Turkish support available for the global developer community in upcoming official releases!
