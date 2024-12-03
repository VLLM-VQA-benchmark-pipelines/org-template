# Организационный шаблон

Этот репозиторий содержит шаблон конфигурации для линтинга и форматирования Python-кода с использованием `black`, `ruff`, `isort` и `pre-commit`. Этот шаблон можно использовать для стандартизации процесса линтинга и форматирования в ваших Python проектах.

## Этапы установки и настройки
### Шаги для создания проекта на освное этого шаблона:

1. Перейдите на страницу репозитория [org-template](https://github.com/your-org/org-template).
2. Нажмите кнопку **"Use this template"** и создайте новый репозиторий.

### Шаги для применения шаблона к существующему репозиторию:
Предположим, у вас есть репозиторий my-org/project-a, и вы хотите применить настройки из шаблона, который вы создали в репозитории my-org/template-repo.
1. Склонируйте репозиторий, в который хотите применить шаблон:

		git clone https://github.com/my-org/project-a.git
		cd project-a
2. Добавьте файлы из шаблона: Перейдите в директорию вашего шаблона и скопируйте все необходимые конфигурационные файлы в репозиторий:
		
* .pre-commit-config.yaml
* pyproject.toml
* .github/workflows/lint.yml
3. Установите зависимости: 

	Важно установить все необходимые зависимости в репозитории.
* Убедитесь, что у вас активировано виртуальное окружение.
* Установите зависимости:

		pip install black ruff isort pre-commit
4. Настройка pre-commit hooks. Чтобы использовать pre-commit hooks, выполните команду:

		pre-commit install

	Это добавит конфигурацию в .git/hooks/pre-commit, чтобы запускать линтеры перед каждым коммитом.

5. Запустите линтеры и форматтеры вручную (по желанию):
* Для black:

		black .
* Для ruff:

		ruff check .
* Для isort:

		isort .

6. Проверьте настройку GitHub Actions (если используется):
	
	Убедитесь, что файл .github/workflows/lint.yml добавлен в ваш репозиторий и будет автоматически запускать линтеры и форматтеры при каждом push или pull request.