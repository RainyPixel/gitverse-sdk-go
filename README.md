# GitVerse Go SDK

Go клиент для [GitVerse API](https://gitverse.ru).

[![Go Reference](https://pkg.go.dev/badge/github.com/RainyPixel/gitverse-sdk-go.svg)](https://pkg.go.dev/github.com/RainyPixel/gitverse-sdk-go)
[![Go Report Card](https://goreportcard.com/badge/github.com/RainyPixel/gitverse-sdk-go)](https://goreportcard.com/report/github.com/RainyPixel/gitverse-sdk-go)

## Установка

```bash
go get github.com/RainyPixel/gitverse-sdk-go
```

## Быстрый старт

```go
package main

import (
    "context"
    "fmt"
    "log"

    gitverse "github.com/RainyPixel/gitverse-sdk-go"
)

func main() {
    client := gitverse.NewClient(gitverse.ClientConfig{
        Token: "your-token",
    })

    // Получить текущего пользователя
    user, err := client.GetAuthenticated(context.Background())
    if err != nil {
        log.Fatal(err)
    }
    fmt.Printf("Hello, %s!\n", user.Login)

    // Получить репозиторий
    repo, err := client.GetRepository(context.Background(), "owner", "repo")
    if err != nil {
        log.Fatal(err)
    }
    fmt.Printf("Repo: %s (%d stars)\n", repo.FullName, repo.StarsCount)
}
```

## Возможности

- Полное покрытие GitVerse API
- Автоматическая обработка Rate Limits
- Версионирование API с предупреждениями об устаревании
- Строго типизированные структуры
- Нет внешних зависимостей (только stdlib)

## API модули

| Модуль | Описание |
|--------|----------|
| Users | Пользователи и аутентификация |
| Repositories | Репозитории, ветки, коммиты, файлы |
| Issues | Issues и комментарии |
| Pulls | Pull requests |
| Releases | Релизы и ассеты |
| Actions | GitHub Actions, runners, secrets, variables |
| Organizations | Организации |
| Teams | Команды |
| Stars | Избранное |
| Emails | Email адреса пользователя |

## Примеры

### Работа с репозиториями

```go
// Список репозиториев пользователя
repos, err := client.ListForAuthenticatedUser(ctx, &gitverse.QueryOptions{
    PerPage: 10,
})

// Создать репозиторий
repo, err := client.CreateForAuthenticatedUser(ctx, gitverse.CreateRepositoryParams{
    Name:        "my-repo",
    Description: ptrStr("My awesome repo"),
    Private:     ptrBool(true),
})

// Получить содержимое файла
content, err := client.GetContent(ctx, "owner", "repo", "README.md")
```

### Работа с Issues

```go
// Список issues
issues, err := client.ListIssues(ctx, "owner", "repo", &gitverse.QueryOptions{
    State: "open",
})

// Получить комментарии
comments, err := client.ListComments(ctx, "owner", "repo", 1, nil)
```

### Работа с Pull Requests

```go
// Список PR
pulls, err := client.ListPulls(ctx, "owner", "repo", &gitverse.QueryOptions{
    State: "open",
})

// Создать PR
pr, err := client.CreatePullRequest(ctx, "owner", "repo", gitverse.CreatePullRequestParams{
    Title: "My PR",
    Head:  "feature-branch",
    Base:  "main",
})
```

### Работа с релизами

```go
// Список релизов
releases, err := client.ListReleases(ctx, "owner", "repo", nil)

// Создать релиз
release, err := client.CreateRelease(ctx, "owner", "repo", gitverse.CreateReleaseParams{
    TagName: "v1.0.0",
    Name:    ptrStr("Release v1.0.0"),
    Body:    ptrStr("Release notes here"),
})
```

## Обработка ошибок

```go
user, err := client.GetByUsername(ctx, "nonexistent")
if err != nil {
    var apiErr *gitverse.APIError
    if errors.As(err, &apiErr) {
        fmt.Printf("API Error: %d - %s\n", apiErr.StatusCode, apiErr.Message)
    }

    var rateLimitErr *gitverse.RateLimitError
    if errors.As(err, &rateLimitErr) {
        fmt.Printf("Rate limited. Reset at: %s\n", rateLimitErr.ResetAt)
    }
}
```

## Конфигурация

```go
client := gitverse.NewClient(gitverse.ClientConfig{
    Token:      "your-token",
    BaseURL:    "https://api.gitverse.ru",  // опционально
    APIVersion: "1",                         // опционально
    HTTPClient: &http.Client{               // опционально
        Timeout: 30 * time.Second,
    },
    OnAPIVersionWarning: func(info gitverse.APIVersionInfo) {
        log.Printf("API version warning: %s", info.DeprecationMessage)
    },
})
```

## Связанные проекты

- [gitverse-api-sdk](https://www.npmjs.com/package/gitverse-api-sdk) — TypeScript SDK
- [gitverse-release](https://www.npmjs.com/package/gitverse-release) — Инструмент автоматизации релизов

## Лицензия

MIT
