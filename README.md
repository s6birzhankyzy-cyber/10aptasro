# 10aptasro
def save_txt(tasks):
    with open("tasks.txt", "w", encoding="utf-8") as f:
        for d, t, tm in tasks:
            f.write(f"{d},{t},{tm}\n")
def load_txt():
    try:
        with open("tasks.txt", "r", encoding="utf-8") as f:
            for line in f:
                day, task, time = line.strip().split(",")
                print(f"{day} — {task} ({time})")
    except FileNotFoundError:
        print(" File not found.")
tasks = []
n = int(input("Number of today's tasks: "))
for i in range(n):
    day = input("Day: ")
    task = input("Task: ")
    time = input("Time: ")
    tasks.append((day, task, time))

save_txt(tasks)
print("\n Tasks were saved to file (tasks.txt)\n")
print(" Info read from file:")
load_txt()
Бұл жұмыста Python бағдарламалау тілін пайдалана отырып күнделікті тапсырмаларды файлға сақтау, файлдан оқу және оларды экранға шығару тапсырмалары орындалды.
Уақытты дұрыс жоспарлау үшін пайдаланушы енгізген тапсырмаларды арнайы файлда сақтау өте маңызды. Бұл болашақта тапсырмаларды тексеруге, өңдеуге және талдауға мүмкіндік береді.
Мәліметтерді сақтау үшін tasks.txt деп аталатын файл таңдалды.
Файлда әр тапсырма бір жолмен сақталады. Әр жолда үш бөлік болады:
Күн,Тапсырма,Уақыты
Пайдаланушы енгізген мәліметтер алдымен тізімде уақытша сақталады:
tasks = []
Пайдаланушы өзі күн, тапсырма атауы және уақыты туралы мәлімет енгізеді.
Бұл деректер автоматты түрде файлға қосылады және программа жабылғаннан кейін де сақталады.
