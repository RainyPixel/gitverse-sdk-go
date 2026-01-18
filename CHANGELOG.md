# Журнал изменений

## [5.2.0] - 2026-01-17

### ✨ Features

- regenerate with getContent ContentsResponse type ([e734148](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/e734148e306170a899e400b71bef4d249080c799)) by @Ivan Bobchenkov

### 📝 Documentation

- add detailed error handling documentation ([275d8ee](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/275d8ee9ebda6bf0bfd49f5c8ab71b0fc84d07e6)) by @Ivan Bobchenkov

### 🔧 Chores

- lint fix ([5157280](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/5157280937930929d25b39b668cda37a865b47f6)) by @Ivan Bobchenkov

## [5.1.0] - 2026-01-17

### ✨ Features

- update to OpenAPI 1.2 ([d33ba32](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/d33ba3210e1febce23b25f2a67e6e6a8cf598887)) by @Ivan Bobchenkov

## [5.0.1] - 2026-01-15

## [5.0.0] - 2026-01-15

### ⚠️ BREAKING CHANGES

- sync with openapi v1.1 specification ([040ba8b](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/040ba8b2414930d2ec29f8b37d32f5fc786af454)) by @Ivan Bobchenkov

### ✅ Tests

- add full coverage for client and organizations API ([161d1d0](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/161d1d0b0fd96ece2bb01b30c7c7d61d1ce4fe44)) by @Ivan Bobchenkov

## [4.0.2] - 2025-11-24

### 🐛 Bug Fixes

- correct rate limit error detection for 429 responses ([4a01407](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/4a01407274f0c58a3b95308b911f3491f7e6b66a)) by @Ivan Bobchenkov

## [4.0.1] - 2025-11-17

### 🐛 Bug Fixes

- export types ([0d18e18](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/0d18e18eed0c769c6da8a107809dbfb531c37dfa)) by @Ivan Bobchenkov

### 🧹 Chores

- fix typo ([153f097](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/153f09716317189361b438ab2e0f92a3d44beecb)) by @Ivan Bobchenkov

## [4.0.0] - 2025-11-12

### ⚠️ BREAKING CHANGES

- **sdk:** add missing query parameters for pulls.list ([e714687](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/e714687ed6ef544534109ae571bb6614631f03b2)) by @esviridov

### ♻️ Refactoring

- **sdk:** inline pull request state filter constants ([28ee615](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/28ee6159d9cd586c395f3ab74837920ec3e7b2be)) by @esviridov
- **sdk:** assign search to url object directly instead of using template literal ([77ec35e](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/77ec35edac60cdacd54b8e9d6b14acc467e8ed56)) by @esviridov

### 📝 Documentation

- **sdk:** improve docs for list pull request params properties ([1baa144](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/1baa144d466ca9d7c99be166a2e0713a05c19121)) by @esviridov
- add roadmap and fix link to issues ([84bc04b](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/84bc04bdf9f1f2c2681fb05072c29279d21c4e68)) by @Ivan Bobchenkov

## [3.2.0] - 2025-11-10

### ✨ Features

- **sdk:** add request cancellation with abortsignal support ([99dd466](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/99dd4660851f1dd32a8f2bdb29db9bb49967bfac)) by @Ivan Bobchenkov
- **release:** add pre-major mode for 0.x.x version handling ([77ca79c](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/77ca79c526a50792e3480186c7819d96958ac684)) by @Ivan Bobchenkov

## [3.1.0] - 2025-11-06

### ✨ Features

- **sdk:** add pull request merge status check method ([f1bc2c6](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/f1bc2c6155391a68c566551b577e49658c452490)) by @Ivan Bobchenkov

### 🧹 Chores

- fix typo ([73c3029](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/73c3029ae6664f15fa476540d32a8a22750686a0)) by @Ivan Bobchenkov

## [3.0.0] - 2025-11-06

### ⚠️ BREAKING CHANGES

- restructure as monorepo with release automation ([4f61a7c](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/4f61a7cf4fb421aa679778a5932cb4875e83f561)) by @Ivan Bobchenkov

### ✨ Features

- **ci:** use release tool for automated releases ([84d7b10](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/84d7b105d562a3153e985be3db48c66585516783)) by @Ivan Bobchenkov

### 📝 Documentation

- translate release readme to russian and unify documentation ([5e51c62](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/5e51c623f4623eb4467265662e6e1c22f9b03b52)) by @Ivan Bobchenkov

### 💄 Styles

- **docs:** update formating in package.jsons and fix typo in readme.md ([e782a09](https://gitverse.ru/RainyPixel/gitverse-sdk/commit/e782a094ff3f3efbbef1ecd3cb5cb838f4d3cd35)) by @Ivan Bobchenkov

## [2.0.1](https://gitverse.ru/rainypixel/gitverse-sdk/compare/v2.0.0...v2.0.1) (2025-10-29)


### 🐛 Исправления

* workaround для дублированных URL в ответах GitVerse API ([557b69b](https://gitverse.ru/rainypixel/gitverse-sdk/commit/557b69bf29f0febb60763b6e05d4d3550be9e4c9))

## [2.0.0](https://gitverse.ru/rainypixel/gitverse-sdk/compare/v1.2.0...v2.0.0) (2025-10-20)


### ⚠ BREAKING CHANGES

* Исправлена конфигурация semantic-release. Все breaking changes из предыдущего коммита (90+ endpoints, новые error классы, изменение API paths) теперь корректно отражены в версии 2.0.0.

### 🐛 Исправления

* semantic-release configuration for breaking changes ([64a9759](https://gitverse.ru/rainypixel/gitverse-sdk/commit/64a97591d248d23d58378f7cf3ebc0d8bb242d75))

## [1.2.0](https://gitverse.ru/rainypixel/gitverse-sdk/compare/v1.1.1...v1.2.0) (2025-10-20)


### ⚠ BREAKING CHANGES

* Изменена структура ошибок API - теперь используются специализированные классы GitVerseApiError и RateLimitError вместо общих Error. Изменен формат заголовка Accept и baseURL. Удален метод forks.list(). Изменено поведение stars.check() - теперь возвращает boolean вместо выброса ошибки при 404.

### 🚀 Новая функциональность

* complete API coverage with 90+ endpoints and breaking changes ([13fa079](https://gitverse.ru/rainypixel/gitverse-sdk/commit/13fa07902639668ddbd28b2fd3c4f0b4d65d2caa))

## [1.1.1](https://gitverse.ru/rainypixel/gitverse-sdk/compare/v1.1.0...v1.1.1) (2025-06-11)


### 🐛 Исправления

* 🐛 Исправлена сборка (не собирался NPM пакет) ([473f7d5](https://gitverse.ru/rainypixel/gitverse-sdk/commit/473f7d587d31e303078813077e49182ccd274804))

## [1.1.0](https://gitverse.ru/rainypixel/gitverse-sdk/compare/v1.0.0...v1.1.0) (2025-06-11)


### 🚀 Новая функциональность

* ✨ Внедрение tree-shakable структуры модулей ([bdc3301](https://gitverse.ru/rainypixel/gitverse-sdk/commit/bdc330141d62659875ce8e5eb70ee4617b19ed20))


### 📚 Документация

* 📝 Обновлен README в соответствии с актуальным названием пакена в NPM Registry ([3509be4](https://gitverse.ru/rainypixel/gitverse-sdk/commit/3509be45d81e397c67bb3413b8de660d64f020e1))

## 1.0.0 (2025-06-11)

### ⚠ BREAKING CHANGES

- Первая публичная версия SDK

### 🚀 Новая функциональность

- ✨ Первая версия
  ([aba3f3d](https://gitverse.ru/rainypixel/gitverse-sdk/commit/aba3f3d97342549cefdfeccd8d1547b831157148))
- 🚀 Первый релиз GitVerse TypeScript SDK
  ([9e39ec2](https://gitverse.ru/rainypixel/gitverse-sdk/commit/9e39ec20df5f2867fd37ffddf7a55771233a348c))
