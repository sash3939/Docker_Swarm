# Домашнее задание к занятию 6. «Оркестрация кластером Docker контейнеров на примере Docker Swarm»

#### Это задание для самостоятельной отработки навыков и не предполагает обратной связи от преподавателя. Его выполнение не влияет на завершение модуля. Но мы рекомендуем его выполнить, чтобы закрепить полученные знания. Все вопросы, возникающие в процессе выполнения заданий, пишите в учебный чат или в раздел "Вопросы по заданиям" в личном кабинете.

---

## Важно

**Перед началом работы над заданием изучите [Инструкцию по экономии облачных ресурсов](https://github.com/netology-code/devops-materials/blob/master/cloudwork.MD).**
Перед отправкой работы на проверку удаляйте неиспользуемые ресурсы.
Это нужно, чтобы не расходовать средства, полученные в результате использования промокода.
Подробные рекомендации [здесь](https://github.com/netology-code/virt-homeworks/blob/virt-11/r/README.md).

[Ссылки для установки открытого ПО](https://github.com/netology-code/devops-materials/blob/master/README.md).

---

## Задача 1

Создайте ваш первый Docker Swarm-кластер в Яндекс Облаке.
Документация swarm: https://docs.docker.com/engine/reference/commandline/swarm_init/
1. Создайте 3 облачные виртуальные машины в одной сети.

   Созданы 6 нод, 1 из которых является master (node1), еще 2 active и standby, и 3 manager ноды.

![VM](https://github.com/user-attachments/assets/c9682f01-6ec5-4264-a5b5-5028ff7290be)
---
   
2. Установите docker на каждую ВМ.

Docker установлен на всех нодах. Выборочно пример 3 нод

![docker_node1](https://github.com/user-attachments/assets/a85b4219-b38e-48e0-b0d0-7d9714d1afee)
---

![docker_node2](https://github.com/user-attachments/assets/dad235d2-e717-4cde-a651-891f2c29b84c)
---

![docker_node3](https://github.com/user-attachments/assets/4d0d6830-03a7-40b1-8b32-f6db7d497c69)
---

 
3. Создайте swarm-кластер из 1 мастера и 2-х рабочих нод.

Кластер создан.

4. Проверьте список нод командой:
```
docker node ls
```

![docker node ls swarm](https://github.com/user-attachments/assets/3c5e1623-0b86-4cd5-9b5c-54b6af1e45af)
---


## Задача 2 (*) (необязательное задание *).
1.  Задеплойте ваш python-fork из предыдущего ДЗ(05-virt-04-docker-in-practice) в получившийся кластер.

![deploy my repo into VM](https://github.com/user-attachments/assets/768f84cd-c1b4-48fc-895b-d0f2fa1e070b)
---

3. Удалите стенд.

Стэнд удален.


## Задача 3 (*)

Если вы уже знакомы с terraform и ansible  - повторите практику по примеру лекции "Развертывание стека микросервисов в Docker Swarm кластере". Попробуйте улучшить пайплайн, запустив ansible через terraform синамическим инвентарем.

Проверьте доступность grafana.

![Grafana](https://github.com/user-attachments/assets/1847311a-ced9-4a8e-bda6-93894c342df8)
---

Иначе вернитесь к выполнению задания после прохождения модулей "terraform" и "ansible".
