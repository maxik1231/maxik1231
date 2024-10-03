ef error_handling_decorator(func):
    def wrapper(expression):
        try:
            result = func(expression)
            return result
        except ZeroDivisionError:
            return "Ошибка: Деление на ноль"
        except SyntaxError:
            return "Ошибка: Неверное выражение"
        except Exception as e:
            return f"Ошибка: {str(e)}"
    return wrapper

@error_handling_decorator
def calculate(expression):
    return eval(expression)

print(calculate("10 + 5"))
print(calculate("10 / 0"))     
print(calculate("10 +"))      
print(calculate("10 + 'test'"))
