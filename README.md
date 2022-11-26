# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #3 выполнил(а):
-Ахунзянов Денис Тимурович
- РИ210914
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | *| 60 |
| Задание 2 | # | 20 |
| Задание 3 | # | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## Задание 1

1.В созданный проект добавил ML Agent, добавив .json – файлы.
![Снимок экрана (258)](https://user-images.githubusercontent.com/114305035/204092825-da0a9f36-1724-4442-92db-e0879c325a72.png)

2.Далее написал серию команд для создания и активации нового ML-агента, а также для скачивания необходимых библиотек.
![Снимок экрана (260)](https://user-images.githubusercontent.com/114305035/204092992-4719dc90-0023-42b5-9990-98a4ecdf6015.png)

3.Создал на сцене плоскость, куб и сферу.Создал простой C# скрипт-файл и подключил его к сфере.
![Снимок экрана (261)](https://user-images.githubusercontent.com/114305035/204093036-80a8e287-5e7b-4039-b26d-557ec783ccac.png)

4.Объекту «сфера» добавил компоненты Rigidbody, Decision Requester, Behavior Parameters и настроил их.
![Снимок экрана (262)](https://user-images.githubusercontent.com/114305035/204093095-9060897b-7ee3-42a5-9505-d61410edbb5e.png)

5.В корень проекта добавил файл конфигурации нейронной сети.
![Снимок экрана (271)](https://user-images.githubusercontent.com/114305035/204093244-e49ac30c-da06-4599-9f9a-e7039e22082b.png)

6.Сделал 3, 9, 27 копий модели «Плоскость-Сфера-Куб», запустил симуляцию сцены.
![Снимок экрана (264)](https://user-images.githubusercontent.com/114305035/204093329-cbeb70fb-0646-4007-9ba2-8bb4daa4a4cc.png)
![Снимок экрана (265)](https://user-images.githubusercontent.com/114305035/204093336-7243cc84-0dee-42a2-9507-ff63e8937ca8.png)
![Снимок экрана (266)](https://user-images.githubusercontent.com/114305035/204093345-d5b34588-571e-4275-9cfb-43af5664c1af.png)
![Снимок экрана (267)](https://user-images.githubusercontent.com/114305035/204093356-4403e31b-d7be-4ccb-a0d8-ceef09e41d49.png)

7.После завершения обучения проверил работу модели.
![Снимок экрана (261)](https://user-images.githubusercontent.com/114305035/204093036-80a8e287-5e7b-4039-b26d-557ec783ccac.png)




## Задание 2
### Должна ли величина loss стремиться к нулю при изменении исходных данных? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ.

- Перечисленные в этом туториале действия могут быть выполнены запуском на исполнение скрипт-файла, доступного [в репозитории](https://github.com/Den1sovDm1triy/hfss-scripting/blob/main/ScreatingSphereInAEDT.py).
- Для запуска скрипт-файла откройте Ansys Electronics Desktop. Перейдите во вкладку [Automation] - [Run Script] - [Выберите файл с именем ScreatingSphereInAEDT.py из репозитория].

```py

import ScriptEnv
ScriptEnv.Initialize("Ansoft.ElectronicsDesktop")
oDesktop.RestoreWindow()
oProject = oDesktop.NewProject()
oProject.Rename("C:/Users/denisov.dv/Documents/Ansoft/SphereDIffraction.aedt", True)
oProject.InsertDesign("HFSS", "HFSSDesign1", "HFSS Terminal Network", "")
oDesign = oProject.SetActiveDesign("HFSSDesign1")
oEditor = oDesign.SetActiveEditor("3D Modeler")
oEditor.CreateSphere(
	[
		"NAME:SphereParameters",
		"XCenter:="		, "0mm",
		"YCenter:="		, "0mm",
		"ZCenter:="		, "0mm",
		"Radius:="		, "1.0770329614269mm"
	], 
)

```

## Задание 3
### Какова роль параметра Lr? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.

- Перечисленные в этом туториале действия могут быть выполнены запуском на исполнение скрипт-файла, доступного [в репозитории](https://github.com/Den1sovDm1triy/hfss-scripting/blob/main/ScreatingSphereInAEDT.py).
- Для запуска скрипт-файла откройте Ansys Electronics Desktop. Перейдите во вкладку [Automation] - [Run Script] - [Выберите файл с именем ScreatingSphereInAEDT.py из репозитория].

```py

import ScriptEnv
ScriptEnv.Initialize("Ansoft.ElectronicsDesktop")
oDesktop.RestoreWindow()
oProject = oDesktop.NewProject()
oProject.Rename("C:/Users/denisov.dv/Documents/Ansoft/SphereDIffraction.aedt", True)
oProject.InsertDesign("HFSS", "HFSSDesign1", "HFSS Terminal Network", "")
oDesign = oProject.SetActiveDesign("HFSSDesign1")
oEditor = oDesign.SetActiveEditor("3D Modeler")
oEditor.CreateSphere(
	[
		"NAME:SphereParameters",
		"XCenter:="		, "0mm",
		"YCenter:="		, "0mm",
		"ZCenter:="		, "0mm",
		"Radius:="		, "1.0770329614269mm"
	], 
)

```

## Выводы

В данной лабораторной работе я создал ML-агента и тренировал нейросеть, задача которой заключалась в управлении шаром. Задача шара заключалась в том, чтобы оставаясь на плоскости находить кубик, смещающийся в заданном случайном диапазоне координат.
В итоге я познакомился с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
