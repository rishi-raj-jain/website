---
locale: it
---

sing @capgo/capacitor-purchases пакет туториал

Этот туториал проведет вас через процесс использования пакета @capgo/capacitor-purchases для покупок в приложении в Capacitor

## Шаг 1: Установите пакет

Чтобы установить пакет @capgo/capacitor-purchases, откройте терминал и выполните следующую команду:

[[БЛОК_КОДА]]

## Шаг 2: Настройте платформу Android

Если вы нацеливаетесь на платформу Android, вам нужно добавить некоторую конфигурацию в файл android/app/src/main/AndroidManifest.xml Откройте файл и добавьте следующий код:

[[БЛОК_КОДА]]

## Шаг 3: Настройте пакет

Чтобы настроить пакет @capgo/capacitor-purchases, используйте метод `setup` с вашим API ключом и необязательным идентификатором пользователя приложения Вот пример:

[[БЛОК_КОДА]]

## Шаг 4: Обработайте событие обновления покупок

Вы можете прослушивать событие "purchasesUpdate", чтобы получить уведомление, когда произойдет изменение в покупках пользователя Вот пример того, как добавить слушателя для события:

[[БЛОК_КОДА]]

## Шаг 5: Получите доступные предложения

Вы можете использовать метод `getOfferings`, чтобы получить доступные предложения для пользователя Вот пример:

[[БЛОК_КОДА]]

## Шаг 6: Купите пакет

Чтобы сделать покупку, используйте метод `purchasePackage` с идентификатором пакета Вот пример:

[[БЛОК_КОДА]]

## Шаг 7: Восстановите покупки

Если вы хотите восстановить покупки пользователя, используйте метод `restorePurchases` Вот пример:

[[БЛОК_КОДА]]

## Вот и всё!

Вы успешно узнали, как использовать пакет @capgo/capacitor-purchases для покупок в приложении в Capacitor Удачного кодирования!