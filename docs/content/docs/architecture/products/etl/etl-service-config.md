---
title: Конфигурации
weight: 13
draft: false
---


## Конфигурационный файл Service `config.json` {id=etl-service-config}

Этот файл содержит настройки для интеграционного сервиса **Service**, включая маппинг сущностей, связей и атрибутов.

---

## **Структура файла**
```json {filename=ServiceConfig,linenos=table}
{
  "SilaService": {
    "ModelCodeAttributeId": "e1f78293-a5ea-489a-824e-7e809ec50365",
    "EntityMapConfig": {  },
    "LinkMapConfig": {  },
    "AttributeMapConfig": {  }
  }
}
```

### **`ModelCodeAttributeId`**
- Уникальный идентификатор атрибута, связанного с кодом модели.
- Используется для идентификации модели в системе.

---

### **`EntityMapConfig` — Маппинг сущностей**
Определяет соответствие идентификаторов сущностей их названиям.

```json {filename=EntityMapConfig,linenos=table}
{
  "EntityMapConfig": {
    "EntityMap": {
      "1": "Person"
    }
  }
}
```
- `1` → **"Person"** (Человек)

🔹 **Пример использования:** если сервис получает объект с ID `1`, он будет интерпретирован как `Person`.

---

### **`LinkMapConfig` — Маппинг связей**
Определяет соответствие между ID связей и их наименованиями.

```json {filename=LinkMapConfig,linenos=table}
{
  "LinkMapConfig": {
    "LinkMap": {
      "c_idef_input": "Rel",
      "2c9280876870fd2801689455a7060032": "BiRel"
    }
  }
}
```
- `"c_idef_input"` → **"Rel"** (Обычная связь)
- `"2c9280876870fd2801689455a7060032"` → **"BiRel"** (Двусторонняя связь)

**Пример использования:** если встречается связь с ID `"c_idef_input"`, она будет обозначаться как `Rel`.

---

### **`AttributeMapConfig` — Маппинг атрибутов**
Определяет соответствие ID атрибутов их названиям.

```json {filename=AttributeMapConfig,linenos=table}
{
  "AttributeMapConfig": {
    "AttributeMap": {
      "49acc949-c25f-4d0a-bbdb-0c9832bfb98c": "Code"
    }
  }
}
```
**Пример использования:** если встречается атрибут с ID `49acc949-c25f-4d0a-bbdb-0c9832bfb98c`, он будет обозначаться как `Code`.

---

### Код модели **`ModelCodeAttributeId`**

- `49acc949-c25f-4d0a-bbdb-0c9832bfb98c` → **"Code"** (Код модели)

**Пример использования:** если объект содержит атрибут с этим ID, он будет интерпретироваться как `Code`.

---

## **Заключение**
Этот конфигурационный файл управляет маппингом сущностей, связей и атрибутов в системе **Service**, упрощая их обработку и интеграцию.
