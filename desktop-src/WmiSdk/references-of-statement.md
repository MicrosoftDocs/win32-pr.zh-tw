---
description: 語句的參考會捕獲參考特定來源實例的所有關聯實例。
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: 語句的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979762"
---
# <a name="references-of-statement"></a>語句的參考

語句的參考會捕獲參考特定來源實例的所有關聯實例。 語句的參考與語法中的語句 ASSOCIATORS OF 類似。 不過，它不會取出端點實例，而是會抓取中間的關聯實例。

WHERE 子句的參考可以包含下列一或多個預先定義的關鍵字和其值：


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



若要指定來源物件，請使用任何有效的物件路徑進行 SourceObject。 如同 SELECT 語句，WHERE 子句是選擇性的，並且用來進一步定義查詢。 也就是說，下列語句完全有效：


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



**ClassDefsOnly** 關鍵字表示語句會傳回類別定義物件的結果集，而非關聯類別的實際實例。 這些物件包含參考來源物件之實例所屬類別的定義。 例如，下列語句會傳回 **AdapterDriver** 和 **AdapterProtocol** 類別的定義：


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



**RequiredQualifier** 關鍵字指出傳回的關聯物件必須包含指定的限定詞。 **RequiredQualifier** 關鍵字可以用來在結果集中包含關聯的特定實例。 例如，下列語句會傳回關聯實例，其中包含名為 **AdapterTag** 的辨識符號：


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



**ResultClass** 關鍵字指出傳回的關聯物件必須屬於或衍生自指定的類別。 例如，下列語句會傳回 **AdapterDriver** 類別或 **AdapterDriver** 子類別的關聯：


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



**ClassDefsOnly** 和 **ResultClass** 關鍵字是互斥的。 一起使用它們會導致不正確查詢錯誤。

**Role** 關鍵字表示傳回的關聯只是來源物件扮演特定角色的關聯。 角色是由指定的屬性所定義，即 [ref](references.md)類型的參考屬性。 **Role** 關鍵字適用于在某些情況下，某些物件在某些情況下可扮演某個角色的關聯性，以及其他在階層式關聯中的角色。 例如， **role** 關鍵字可以用來抓取來源物件扮演父系角色的所有關聯。 下列語句說明用來抓取關聯的語法，此關聯具有將來源物件參考為父系的 **父** 屬性：


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> 複雜的查詢不能使用 "And" 或 "Or" 來分隔 ASSOCIATORS OF 和語句參考的關鍵字。 此外，等號是唯一可搭配這些查詢中的關鍵字使用的有效運算子。 例如，以下是有效的查詢：

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> 接下來的範例是不正確。 第一個範例不會使用等號，而第二個範例會錯誤地嘗試使用 **和** 關鍵字：

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



