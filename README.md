Файл: sergeant.py

class Sergeant:
    def __init__(self, name, unit, rank="Головний сержант"):
        self.name = name
        self.unit = unit
        self.rank = rank
        self.tasks = []

    def assign_task(self, task):
        """Додати завдання для виконання"""
        self.tasks.append(task)
        print(f"{self.rank} {self.name} доручив: {task}")

    def report_status(self):
        """Звіт про виконання завдань"""
        if not self.tasks:
            return f"{self.rank} {self.name} не має активних завдань."
        report = f"Звіт {self.rank} {self.name}:\n"
        for i, task in enumerate(self.tasks, 1):
            report += f"{i}. {task}\n"
        return report

    def lead_training(self, topic):
        """Проведення занять"""
        return f"{self.rank} {self.name} проводить тренування на тему: {topic}"


# Приклад використання
if __name__ == "__main__":
    sergeant = Sergeant("Іван Петренко", "1-ше відділення")
    sergeant.assign_task("Перевірити готовність особового складу")
    sergeant.assign_task("Організувати стройове заняття")
    print(sergeant.report_status())
    print(sergeant.lead_training("Тактика дій у бою"))
