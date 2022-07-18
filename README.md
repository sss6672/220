Расширение Docker упрощает создание, управление и развертывание контейнерных приложений из Visual Studio Code. Он также обеспечивает отладку одним щелчком мыши Node.js , Python и .NET Core внутри контейнера.

Обзор расширения Docker

Для начала ознакомьтесь с разделом "Работа с контейнерами" на сайте документации по коду Visual Studio.

Вики-страница расширения Docker содержит советы по устранению неполадок и дополнительную техническую информацию.

Установка
Установите Docker на свой компьютер и добавьте его в системный путь.

В Linux вы должны включить Docker без корней и установить для созданного контекста Docker значение "без корней" (более безопасный) или включить Docker CLI для учетной записи пользователя, не являющегося пользователем root (менее безопасный), которая будет использоваться для запуска VS Code.

Чтобы установить расширение, откройте представление расширений, выполните поиск для dockerфильтрации результатов и выберите расширение Docker, созданное корпорацией Майкрософт.

Обзор возможностей расширения
Редактирование файлов Docker
Вы можете получить IntelliSense при редактировании Dockerfileфайлов docker-compose.ymlи с дополнениями и справкой по синтаксису для общих команд.

IntelliSense для Dockerfiles

Кроме того, вы можете использовать панель проблем (Ctrl+Shift+Mв Windows / Linux, Shift+Command+Mна Mac) для просмотра распространенных ошибок Dockerfileи docker-compose.ymlфайлов.

Создание файлов Docker
Вы можете добавлять файлы Docker в свою рабочую область, открыв палитру команд (F1) и используя команду Docker: Добавить файлы Docker в рабочую область. Команда сгенерирует Dockerfile.dockerignoreфайл и и добавит их в вашу рабочую область. Команда также спросит вас, хотите ли вы также добавить файлы Docker Compose, но это необязательно.

Расширение может создавать каркасы для файлов Docker для большинства популярных языков разработки (C #, Node.js , Python, Ruby, Go и Java) и соответствующим образом настраивает сгенерированные файлы Docker. При создании этих файлов мы также создаем необходимые артефакты для обеспечения первоклассной поддержки отладки для Node.js , Python и .NET (C #).

Docker Explorer
Расширение Docker добавляет представление Docker Explorer в VS Code. Docker Explorer позволяет просматривать ресурсы Docker и управлять ими: контейнеры, образы, тома, сети и реестры контейнеров. Если установлено расширение учетной записи Azure, вы также можете просматривать реестры контейнеров Azure.

Вызываемое правой кнопкой мыши меню предоставляет доступ к часто используемым командам для каждого типа ресурсов.

Контекстное меню Docker view

Панели представления Docker можно изменять, перетаскивая их вверх или вниз с помощью мыши, а затем использовать контекстное меню, чтобы скрыть или показать их.

Настройка представления Docker

Команды Docker
Многие из наиболее распространенных команд Docker встроены прямо в палитру команд:

Команды Docker

Вы можете запускать команды Docker для управления образами, сетями, томами, реестрами образов и Docker Compose. Кроме того, команда Docker: Prune System удалит остановленные контейнеры, зависшие изображения и неиспользуемые сети и тома.

Docker Compose
Docker Compose позволяет определять и запускать многоконтейнерные приложения с помощью Docker. Наша языковая служба Compose в расширении Docker предоставляет вам функции IntelliSense и табуляции при создании docker-compose.ymlфайлов. НажмитеCtrl+Space, чтобы просмотреть список допустимых директив Compose.

Docker Compose IntelliSense

Мы также предоставляем всплывающие подсказки при наведении курсора мыши на атрибут Docker Compose YAML.

Всплывающие подсказки Docker Compose

While Compose Up allows you to run all of your services at once, our new feature Compose Up - Select Services lets you select any combination of the services you want to run.

Docker Compose Up - Select Subset

Once your Compose Up command completes, navigate to the Docker Explorer to view your services as a Compose Group. This allows you to start, stop, and view the logs of each service as a group.

Docker создает группы

Использование реестров образов
You can display the content and push, pull, or delete images from Docker Hub and Azure Container Registry:

Azure Container Registry content

An image in an Azure Container Registry can be deployed to Azure App Service directly from VS Code. See Deploy images to Azure App Service to get started. For more information about how to authenticate to and work with registries, see Using container registries.

Debugging services running inside a container
You can debug services built using Node.js, Python, or .NET (C#) that are running inside a container. The extension offers custom tasks that help with launching a service under the debugger and with attaching the debugger to a running service instance. For more information, see Debug containerized apps and Customize the Docker extension.

Azure CLI integration
You can start Azure CLI (command-line interface) in a standalone, Linux-based container with Docker Images: Run Azure CLI command. This gives you access to the full Azure CLI command set in an isolated environment. For more information on available commands, see Get started with Azure CLI.

Contributing
Идеи и рекомендации по улучшению расширения см. В руководстве по внесению вклада. Спасибо!

Кодекс поведения
В этом проекте принят Кодекс поведения Microsoft с открытым исходным кодом. Для получения дополнительной информации см. Часто задаваемые вопросы по Кодексу поведения или свяжитесь с opencode@microsoft.com с любыми дополнительными вопросами или комментариями.

Телеметрия
VS Code собирает данные об использовании и отправляет их в корпорацию Майкрософт, чтобы помочь улучшить наши продукты и услуги. Прочитайте наше заявление о конфиденциальности, чтобы узнать больше. Если вы не хотите отправлять данные об использовании в корпорацию Майкрософт, вы можете установить telemetry.telemetryLevelзначение off. Узнайте больше в нашем FAQ.

Лицензия
MIT
