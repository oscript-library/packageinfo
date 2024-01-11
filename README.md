# PackageInfo

Это маленькая библиотека для получения информации о пакете.

Довольно часто при создании приложений на oscript нам необходимо выводить информацию о нашем приложении. (Версию, автора и тд и тп) Эта библиотека как раз для этого.

## Пример использования

```bsl
#Использовать packageinfo

Функция ВерсияПриложения() Экспорт

    // Указываем путь до packagedef с информацией о приложении.
    ПутьКМанифесту = ОбъединитьПути(ТекущийСценарий().Каталог, "..", "packagedef");

    ОписаниеПакета = Новый ИнформацияОПакете(ПутьКМанифесту);

    Возврат СтрШаблон("Версия приложения <%1>", ОписаниеПакета.Версия());
КонецФункции
```