# Анализ данных в разработке игр
Отчет по лабораторной работе #5 выполнил(а):
- Иванова Анастасия Евгеньевна
- РИ-230911

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

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
- Задание 1. Найдите внутри C# скрипта “коэффициент корреляции” и сделать выводы о том, как он влияет на обучение модели.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2. Изменить параметры файла yaml-агента и определить какие параметры и как влияют на обучение модели. Привести описание не менее трех параметров.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3. Приведите примеры, для каких игровых задачи и ситуаций могут использоваться примеры 1 и 2 с ML-Agent’ом. В каких случаях проще использовать ML-агент, а не писать программную реализацию решения? 
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## Задание 1
### Найдите внутри C# скрипта “коэффициент корреляции ” и сделать выводы о том, как он влияет на обучение модели.
Я нашла в скрипте RollerAgent.cs - число 1.42.

Я думаю что в данном случае это число, находящееся в условии называется коэффициентом корреляции, т.к. награда агенту начисляется только если он достиг цели, обозначенной этим числом.

Данный коэффициент корреляции влияет на обучение модели прямо, а именно, если:
* Коэффициент велик -- модель обучается быстрее, но допускает много ошибок. 
* Коэффициент маленький -- модель обучается медленно, но допускает меньше ошибок.

![image](https://github.com/user-attachments/assets/5c9e7136-ab63-494e-be7f-da9b4afc7ac3)


## Задание 2
### Изменить параметры файла yaml-агента и определить какие параметры и как влияют на обучение модели. Привести описание не менее трех параметров.
Изучив параметры yaml, я разобралась в некоторых параметрах:

trainer_type - это тип "тренера", или метод обучения. В данном примере используется тренер "ppo", существуют так же следующие методы "sac", "ddpg" и другие. Выбор между ними стоит делать учитывая необходимую для реализации задачу.

learning_rate - скорость обучения модели

num_epoch - количество итераций (эпох) при обучении модели

max_steps - максимальное количество шагов для завершения обучения

summary_freq - частота указываемая в шагах до создания отчета о текущем состоянии обучения

checkpoint_interval - интервал указываемых в шагах до создания агентом контрольных точек во время обучения

Так же я узнала, что в разделе "network_settings" указываются слои нейронной сети и количество нейронов в одном слое 

## Задание 3
### Приведите примеры, для каких игровых задачи и ситуаций могут использоваться примеры 1 и 2 с ML-Agent’ом. В каких случаях проще использовать ML-агент, а не писать программную реализацию решения? 

ML-агент проще использовать в случаях, когда внешние игровые условия могут меняться динамически и когда данные для программной реализации будет внести затруднительно.

Если корректно обучить ML-агент, то он сможет при любых условиях достичь поставленной цели.

Из примеров к л.р. можно привести пару примеров игр, в которых может использоваться схожий алгоритм:

В игре Friday the 13th : The Game, с ML-агентом, можно вместо маньяка-джейсона управляемого реальным игроком сделать бота либо PVE-контент.

В игре, Sea of Thieves, с ML-агентом, можно на локациях с островом размещать интересные ивенты, где каждый ход и решение могут привести к разному результату.

Так же ML-агент можно использовать для состязаний с игроками в различных гонках, платформерах.

## Выводы
Я разобралась в структуре конфигурационного файла для ML-агента.Познакомилась с программными средствами для создания системы машинного обучения и ее интеграции в Unity. Самостоятельно обучила модель достигать цели на простом примере.

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
