# lesson 4

# по ссылке вы найдете 
https://miro.com/app/board/uXjVNNCmN2s=/?share_link_id=196892319855

- схема до (вместе с посчитанным instability)

- схема после

---

# Что нужно сделать

- матчинг выносим отдельно т.к. ни от чего не зависит, при выносе сервис будет стабильным потому что он получает данные, обрабатывает и возвращает назад

- заменить везде коммуникации на асинхронные

- списание и счет средств переносим внутрь контекста сервис 1 (выполнение заказов)

- энтити сервис воркеров (4) переносим в контест сервиса 1 (выполнения заказов), и размазываем локику по всему контексту, тк это не является отдельным сервисом и привносит нестабильность в систему


# когда есть свободные люди и ресурсы, а опыта и (или) инфраструктуры нет

нужно начинать с простых вещей.

- вынести матчинг в отдельный сервис, тк ничего не аффектит, будет возможность потренироваться

- списание средств перенести внутрь, тк просто дублируем код в монолит

- заменить везде коммуникации на асинхронные

- перенести энтити воркер внутрь контекста тк это выглядит как самая сложная часть системы

# когда свободных людей и ресурсов нет, а опыт и (или) инфраструктура есть

нужно начинать с того что сейчас важно.

- перенести воркер сервис внутрь сервиса 1 (выполнение заказов) тк он не приносит пользы и привносит нестабильность в систему

- заменить везде коммуникации на асинхронные, тк это важно для стабильности системы

- перенос списания средств внутрь контекста 

- вынести матчинг отдельно
