# 장고 커스텀 커맨드.

## 커스텀 커맨드의 위치

- app folder/management/commands/<command.py>

```
from django.core.management.base import BaseCommand

class Command(BaseCommand):
    help = "help text"

    def add_arguments(self, parser):
        parser.add_argument("--<action>", help="help text")

    def handle(self, *args, **options):         #실행 코드
        actions = options.get("<action>")
```
