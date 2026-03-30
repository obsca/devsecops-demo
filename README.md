# DevSecOps Demo

Простой пример пайплайна CI/CD/DevSecOps:

- Flask приложение
- Unit и integration tests
- SAST (Bandit)
- DAST (OWASP ZAP)
- Docker build + push
- Multi-stage deploy: dev -> staging -> production

### Ветки

- `dev` - разработка, запускается пайплайн
- `main` - merge после успешного теста и сканов

1. Форкнуть репозиторий
2. Настроить секреты:
   - `DOCKER_USER`
   - `DOCKER_PASS`
3. Push в `dev` -> пайплайн запускается автоматически
4. Для деплоя в prod использовать `workflow_dispatch` с `allow_deploy=true`
