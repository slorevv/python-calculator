# python-calculator
#Бесконечный калькулятор: сложение, вычитание, умножение, деление. Защита от деления на ноль и выхода по 'q'
print("=== Бесконечный калькулятор ====")
print("(Чтобы выйти, введи 'q' вместо числа)")

while True:
    print("\n" + "="*30)
    
    # Ввод первого числа с проверкой на выход
    first = input("Введите первое число (или 'q' для выхода): ")
    if first == "q":
        print("До свидания!")
        break
    
    # Ввод второго числа
    second = input("Введите второе число: ")
    if second == "q":
        print("До свидания!")
        break
    
    # Превращаем в числа
    try:
        num1 = float(first)
        num2 = float(second)
    except ValueError:
        print("Ошибка! Нужно вводить числа или 'q'.")
        continue
    
    # Выбор действия
    print("\nДействия: + - * /")
    action = input("Выбери действие: ")
    
    # Считаем
    if action == "+":
        print(f"Результат: {num1} + {num2} = {num1 + num2}")
    elif action == "-":
        print(f"Результат: {num1} - {num2} = {num1 - num2}")
    elif action == "*":
        print(f"Результат: {num1} * {num2} = {num1 * num2}")
    elif action == "/":
        if num2 == 0:
            print("Ошибка! На ноль делить нельзя.")
        else:
            print(f"Результат: {num1} / {num2} = {num1 / num2}")
    else:
        print("Неизвестное действие!")
