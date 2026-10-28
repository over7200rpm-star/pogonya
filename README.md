# Погоня в Рязани: сборка .ipa через GitHub Actions

Игра: `www/index.html` (версия 3.34). Обёртка: Capacitor 8 (iOS, Swift Package Manager).

Как это работает: при каждом push в ветку main/master или по кнопке Actions → Build IPA → Run workflow
GitHub запускает macOS-сервер, который собирает НЕПОДПИСАННОЕ приложение и кладёт его в артефакт `App-ipa` (файл `App.ipa`).
Подпись ставится позже на вашем компьютере программой Sideloadly (вашим Apple ID).

Папка `ios` не хранится в репозитории: workflow создаёт её сам (`npx cap add ios`).

Обновить игру: замените файл `www/index.html` в репозитории и запустите сборку заново.

Идентификатор приложения: `com.pogonya.ryazan` (файл `capacitor.config.json`).
Подробная инструкция: см. github_instruction.pdf.
