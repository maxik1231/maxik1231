class Tvarina:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        
class Sobaka(Tvarina):
    def sound(self):
        return "Гав-гав!"

class Kit(Tvarina):
    def sound(self):
        return "Мяу-мяу!"

sobaka = Sobaka("Рекс", 5)
kit = Kit("Мурчик", 3)


print(sobaka.info())
print(sobaka.sound())

print(kit.info())
print(kit.sound())

