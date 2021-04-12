---
description: 抓取與特定來源實例相關聯的所有實例。
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: 語句 ASSOCIATORS OF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320031"
---
# <a name="associators-of-statement"></a>語句 ASSOCIATORS OF

語句的 ASSOCIATORS OF 會抓取與特定來源實例相關聯的所有實例。 取出的實例稱為端點。 每個端點會以其與來源物件之間的關聯，多次傳回。 例如，假設有實例 A、B、X 和 Y。有兩個關聯實例存在，一個連結 A 和 X，另一個連結 B 和 Y。下列查詢會傳回單一端點 X：


```sql
ASSOCIATORS OF {A}
```



但是，如果有另一個關聯連結 A 和 X，則上述查詢會傳回兩個 X 端點。

ASSOCIATORS OF 語句的基本語法為：

``` syntax
ASSOCIATORS OF {ObjectPath}
```

請注意，大括弧是語法的一部分。 任何有效的物件路徑都可以用於 ObjectPath。 物件路徑內的標記不可包含任何空白字元。 例如，下列清單中的查詢會傳回與指定的邏輯磁片相關聯的實例：

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

如同 [select 語句](select-statement-for-data-queries.md)，語句的 associators of 可以包含 [WHERE 子句](where-clause.md)，但語句 associators of 的 WHERE 子句與 SELECT statementWHERE 子句非常不同。

語句 ASSOCIATORS OF 的 [WHERE 子句](where-clause.md) 可以包含下列一或多個預先定義的關鍵字和其值：


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



請注意，選擇性的子條款不會以逗號分隔。

**AssocClass** 關鍵字指出傳回的端點必須透過指定的類別或其衍生類別的其中一個來與來源產生關聯。 例如，下列清單中的查詢只會傳回透過 [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association 類別或其任何衍生類別與來源相關聯的端點：

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

**ClassDefsOnly** 關鍵字指出子句會傳回類別定義物件的結果集，而不是類別的實際實例。 這些物件是端點實例所屬類別的定義。 例如，下列清單中的查詢會傳回 [**win32 \_ 目錄**](/windows/desktop/CIMWin32Prov/win32-directory) 和 win32 執行程式類別 [**\_**](/windows/desktop/CIMWin32Prov/win32-computersystem) 的定義：

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

**ClassDefsOnly** 和 **ResultClass** 關鍵字是互斥的。 一起使用它們會導致不正確查詢錯誤。

**RequiredAssocQualifier** 關鍵字指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。 這種類型的篩選可用來消除範圍廣泛的端點，除非端點透過一組特定的標記關聯類別與目標相關聯。 例如，如果 association 類別包含稱為 **association** 的辨識符號，則下列清單中的查詢會傳回端點實例。

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

**RequiredQualifier** 關鍵字表示與來源物件相關聯的傳回端點必須包含指定的限定詞。 **RequiredQualifier** 關鍵字可以用來在結果集中包含特定類型的實例。 例如，下列清單中的查詢會傳回包含稱為 [**Locale**](swbemobjectpath-locale.md)的辨識符號的端點實例。

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

**ResultClass** 關鍵字表示與來源物件相關聯的傳回端點必須屬於或衍生自指定的類別。 例如，下列清單中的查詢會傳回衍生自 [**CIM \_ 目錄**](/windows/desktop/CIMWin32Prov/cim-directory) 類別的端點實例：

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

**ClassDefsOnly** 和 **ResultClass** 關鍵字是互斥的。 一起使用它們會導致不正確查詢錯誤。

**ResultRole** 關鍵字指出傳回的端點必須在其與來源物件的關聯中扮演特定的角色。 角色是由指定的屬性所定義，即 [ref](references.md)類型的參考屬性。例如，您可以使用 **ResultRole** 關鍵字，在其與來源物件的關聯中取得具有 **GroupComponent** 屬性的所有端點，如下列查詢所示。

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

**Role** 關鍵字表示傳回的端點會參與與來源物件（其來源物件扮演特定角色）的關聯。 角色是由指定的屬性所定義，即 **ref** 類型的參考屬性。例如， **Role** 關鍵字可用來取得與具有 **GroupComponent** 屬性之來源物件相關聯的所有端點，如下列查詢所示。

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> 複雜的查詢不能使用 "And" 或 "Or" 來分隔 ASSOCIATORS OF 和語句 [參考的](references-of-statement.md) 關鍵字。 此外，等號是唯一可用於這類查詢的有效運算子。 例如，以下是有效的查詢：

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> 接下來的範例是不正確。 第一個範例不會使用等號，而第二個範例會錯誤地嘗試使用 **和** 關鍵字。

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
