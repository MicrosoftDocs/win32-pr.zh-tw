---
description: 使用 WHERE 子句來縮小資料、事件或架構查詢的範圍。
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: 'WHERE 子句 (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386717"
---
# <a name="where-clause-wmi"></a>WHERE 子句 (WMI) 

使用 WHERE 子句來縮小資料、事件或架構查詢的範圍。 如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。 WHERE 子句是由屬性或關鍵字、運算子和常數所組成。 所有 WHERE 子句都必須指定其中一個預先定義的運算子，其中包含在 Windows Management Instrumentation (WMI) 查詢語言 (WQL) 中。 您可以使用下列其中一種形式，將 WHERE 子句附加至 SELECT 語句：


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



其中 \* 是查詢的專案，類別是要查詢的類別，而常數、運算子和屬性則是要使用的常數、運算子和屬性或關鍵字。 如需 SELECT 語句的詳細資訊，請參閱 [資料查詢的 Select 語句](select-statement-for-data-queries.md)、 [事件查詢的 select](select-statement-for-event-queries.md)語句，或 [架構查詢的 select 語句](select-statement-for-schema-queries.md)。

常數的值必須是屬性的正確類型。 此外，運算子必須在有效的 [WQL 運算子](wql-operators.md)清單中。 屬性名稱或常數必須出現在 WHERE 子句中運算子的任一邊。

在 WHERE 子句中，您可以使用字串常值（例如 "NTFS"）。 如果您想要在字串中包含下列特殊字元，您必須先在字元前面加上反斜線 () ，以將字元轉義 \\ ：

-   反斜線 (\\ \\) 
-   雙引號 (\\ ") 
-   單引號 (\\ ' ) 

不能使用任意算術運算式。 例如，下列查詢只會傳回代表 NTFS 磁片磁碟機之 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的實例：


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



屬性名稱不能出現在運算子的兩邊。 下列查詢是無效查詢的範例：


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



針對 WHERE 子句中類別描述項的大部分用法，WMI 會將查詢標示為無效，並傳回錯誤。 不過，請針對 WMI 中 **object** 類型的屬性使用點 (. ) 運算子。 例如，如果屬性是 MyClass 的有效屬性且為型別 **物件**，則下列查詢會是有效的：

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

比較測試一律不區分大小寫。 也就是說，下列三個語句全都評估為 **TRUE**：


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



您可以建立包含布林資料類型的查詢，但唯一有效的布林運算元類型為 =、！ = 和 <> 類型。 **TRUE** 值等於數位1，而 **FALSE** 值等於數位0。 下列範例是比較布林值與 **TRUE** 或 **FALSE** 值的查詢。


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



下列範例是嘗試使用無效運算元的無效查詢。


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



您可以使用邏輯運算子和括弧子運算式，在 WHERE 子句中結合多個屬性、運算子和常數群組。 每個群組都必須與 AND、OR 或 NOT [運算子](wql-operators.md) 聯結，如下列查詢所示。 第一個查詢會使用設定為 C 或 D 的 **Name** 屬性，來抓取 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)類別的所有實例：


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



第二個查詢只有在有特定數量的可用空間，且具有 NTFS 檔案系統時，才會取得名為 "C：" 或 "D：" 的磁片：


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



此範例顯示使用 WHERE 子句的架構查詢。


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



類別中繼類別會將 \_ 此識別為架構查詢，呼叫此屬性的屬性會 \_ \_ 識別查詢的目標類別，而[ISA 運算子](isa-operator-for-schema-queries.md)會要求目標類別之子類別的定義。 因此，上述查詢會傳回 myClassName 類別的定義和其所有子類別的定義。

下列範例是使用 [語句 associators of](associators-of-statement.md) 搭配 WHERE 的資料查詢：


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



下一個範例顯示使用 ASSOCIATORS OF 和 WHERE 的架構查詢：


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



下列範例是使用 [語句參考](references-of-statement.md) 和 WHERE 的資料查詢：


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



最後一個範例是使用的參考和位置的架構查詢：


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



除了 WMI [DATETIME](date-and-time-format.md) 格式之外，WQL WHERE 子句還支援數個其他的日期和時間格式：

-   [WQL-支援的日期格式](wql-supported-date-formats.md)
-   [WQL-支援的時間格式](wql-supported-time-formats.md)

 

 
