### .gitignore

Этот `.gitignore` файл указывает, какие файлы и директории следует игнорировать Git при коммитах. Вот что из него будет проигнорировано:

1. **#**
   - Все строки начинающиеся с символа `#` Не будут прочтены программой. (Используются для коментариев).

2. **Local .terraform directories:**
   - `**.terraform/*` это означает что все файлы и директории, находящиеся во всех поддиректориях с именем .terraform, будут проигнорированы. 
Это связано с локальными данными Terraform, которые не должны включаться в репозиторий.

3. **.tfstate files:**
   - Все файлы с расширением `*.tfstate` и `*.tfstate.*` будут игнорироваться. Это файлы состояния Terraform, которые могут содержать важные данные.

4. **Crash log files:**
   - Файлы с именем `crash.log` и `crash.*.log` будут игнорироваться. Это файлы с записями о сбоях.

5. **.tfvars files:**
   - Все файлы с расширением `*.tfvars` и `*.tfvars.json` будут игнорироваться. Эти файлы могут содержать важные данные, такие как пароли, ключи и другие секреты.

6. **Override files:**
   - Файлы с именем `override.tf`, `override.tf.json`, `*_override.tf`, и `*_override.tf.json` будут игнорироваться. 
Эти файлы обычно используются для локальных изменений и не должны контролироваться версиями.

7. **Include override files:** (если раскомментировать)
   - Если необходимо добавить какой-то файл с паттерном `*_override.tf` в контроль версий, используя отрицательный паттерн, как в `!example_override.tf`.

8. **tfplan files:** (если раскомментировать)
   - Файлы, содержащие `*tfplan*`, будут игнорироваться. Эти файлы являются результатом команды `terraform plan -out=tfplan` и обычно не включаются в репозиторий.

9. **CLI configuration files:**
   - Файлы `.terraformrc` и `terraform.rc` будут игнорироваться. Это файлы конфигурации для Terraform CLI.

Все эти правила позволяют избежать ненамеренного включения важных данных и локальных настроек Terraform в репозиторий,
что является хорошей практикой для безопасности и совместной работы.