[<h1 align="center"><img alt="Deployed with FTP Deploy Action" src="https://img.shields.io/badge/Deployed With-FTP DEPLOY ACTION-%3CCOLOR%3E?style=for-the-badge&color=d00000"></h1>](https://github.com/SamKirkland/FTP-Deploy-Action)

##### _Production build_ deployed here: [ildan-dev.ru](https://ildan-dev.ru)
##### _Feature stand_ deployed here: [feature.ildan-dev.ru](https://feature.ildan-dev.ru)
## Sonar statisctics
[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=1ldaun_stormrage&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=1ldaun_stormrage)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=1ldaun_stormrage&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=1ldaun_stormrage)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=1ldaun_stormrage&metric=coverage)](https://sonarcloud.io/summary/new_code?id=1ldaun_stormrage)
## Structure
Feature-sliced design has been taken to this project:
```sh
└── src/                        #
    ├── processes/              # Layer: Processes (optional)
    |   ├── {some-process}/     #     Slice: (e.g. CartPayment process)
    |   |   ├── lib/            #         Segment: Infrastructure-logic (helpers/utils)
    |   |   └── model/          #         Segment: Business Logic
    |   ...                     #
    |                           #
    ├── pages/                  # Layer: Pages
    |   ├── {some-page}/        #     Slice: (e.g. ProfilePage page)
    |   |   ├── lib/            #         Segment: Infrastructure-logic (helpers/utils)
    |   |   ├── model/          #         Segment: Business Logic
    |   |   └── ui/             #         Segment: UI logic
    |   ...                     #
    |                           #
    ├── widgets/                # Layer: Widgets
    |   ├── {some-widget}/      #     Slice: (e.g. Header widget)
    |   |   ├── lib/            #         Segment: Infrastructure-logic (helpers/utils)
    |   |   ├── model/          #         Segment: Business Logic
    |   |   └── ui/             #         Segment: UI logic
    |                           #
    ├── entities/               # Layer: Business entities
    |   ├── {some-entity}/      #     Slice: (e.g. entity User)
    |   |   ├── lib/            #         Segment: Infrastructure-logic (helpers/utils)
    |   |   ├── model/          #         Segment: Business Logic
    |   |   └── ui/             #         Segment: UI logic
    |   ...                     #
    |                           #
    ├── shared/                 # Layer: Reused resources
    |   ├── api/                #         Segment: Logic of API requests
    |   ├── config/             #         Segment: Application configuration
    |   ├── lib/                #         Segment: Infrastructure-application logic
    |   └── ui/                 #         Segment: UIKit of the application
    |   ...                     #
    |                           #
    ├── App.tsx                 #
    └── index.tsx/              #
```
