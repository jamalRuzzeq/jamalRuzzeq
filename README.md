from abc import ABC, abstractmethod

# تعريف الواجهة (كلاس مجرد)
class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        pass

    @abstractmethod
    def move(self):
        pass

# كلاس يطبق الواجهة Animal
class Dog(Animal):
    def make_sound(self):
        print("The dog barks: Woof Woof!")

    def move(self):
        print("The dog runs.")

# كلاس يطبق الواجهة Animal
class Cat(Animal):
    def make_sound(self):
        print("The cat meows: Meow Meow!")

    def move(self):
        print("The cat jumps.")

# الكود الرئيسي
if __name__ == "__main__":
    dog = Dog()
    cat = Cat()

    # استدعاء الدوال لكل من الكائنات
    dog.make_sound()
    dog.move()

    cat.make_sound()
    cat.move()
