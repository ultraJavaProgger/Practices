# Практическая работа №6
## Создание автоматизированных Unit-тестов

### Цель работы
Провести тестирование разработанных программных модулей с использованием средств автоматизации Microsoft Visual Studio методом "белого ящика".

---

## Выполненные шаги

### 1. Создание проекта для тестирования
- В **Microsoft Visual Studio** создан консольный проект **Bank**.
- Реализован класс **BankAccount** с методами `Debit` и `Credit`.
- Проверена работоспособность проекта.

### 2. Создание проекта модульного тестирования
- Добавлен проект **Bank**.
- Добавлен тестовый проект **BankTests**
- Включена ссылка на **Bank**. ↑
- Создан тестовый класс **BankAccountTests**.

### 3. Разработка и запуск тестов
#### Тестирование метода `Debit`
1. **Debit_WithValidAmount_UpdatesBalance**
   - Проверяет корректное списание суммы при допустимом значении.
   - **Результат**: Тест не пройден (обнаружена ошибка в коде `Debit`).
2. **Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange**
   - Проверяет выброс исключения при отрицательной сумме.
   - **Результат**: Тест пройден.
3. **Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange**
   - Проверяет выброс исключения при списании суммы, превышающей баланс.
   - **Результат**: Тест пройден.

#### Рефакторинг метода `Debit`
- Добавлены константы ошибок.
- Исключения дополнены сообщениями.
- Модифицированы тесты с проверкой текста исключения.

#### Тестирование метода `Credit`
- Разработан тест `Credit_WithValidAmount_UpdatesBalance`.
- Разработан тест `Credit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange`.
- **Результат**: Тесты пройдены.

---

## Скриншоты
![image](https://github.com/user-attachments/assets/9bc43f3f-c2c3-4685-ac3e-b3ee660d1c75)
![image](https://github.com/user-attachments/assets/5455c2d3-a86e-4d37-9383-204718e7a538)
![image](https://github.com/user-attachments/assets/6ef1dfea-fa11-4f7b-a4ca-f266ef27af57)
![image](https://github.com/user-attachments/assets/91469edf-7285-4f3a-995b-74df9a22de22)
![image](https://github.com/user-attachments/assets/1cb320e5-a195-45d6-b82e-278d4cad0d06)



---

## Вывод
Модульное тестирование позволило выявить ошибку в методе `Debit`, которая была исправлена путём рефакторинга кода. Тесты подтверждают корректность работы методов `Debit` и `Credit` в различных сценариях. Все тесты успешно пройдены после внесения исправлений.
