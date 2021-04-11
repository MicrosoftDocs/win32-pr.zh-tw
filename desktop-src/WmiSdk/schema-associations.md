---
description: 架構關聯查詢使用與資料關聯查詢中所使用的相同語句：的 ASSOCIATORS OF 和參考。
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: 架構關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194699"
---
# <a name="schema-associations"></a>架構關聯

架構關聯查詢使用與資料關聯查詢中所使用的相同語句：的 ASSOCIATORS OF 和參考。 不過，使用資料關聯查詢時，會傳回類別實例，並使用架構關聯查詢來傳回可參與關聯關聯性的類別名稱。 例如，使用架構查詢來尋找參考來源類別的架構中定義的所有關聯類別。

架構關聯查詢的 ASSOCIATORS OF 和語句參考的語法，與下列例外狀況的資料關聯查詢相同：

-   來源物件是類別，而不是實例。
-   還有一個額外的關鍵字 **SchemaOnly**，它會將查詢識別為套用至架構，而不是資料。
-   **ClassDefsOnly** 關鍵字無效。

下列範例顯示架構查詢的語句 ASSOCIATORS OF 完整語法。 如需詳細的語法，請參閱 [語句 associators of](associators-of-statement.md)。


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



下列範例顯示的查詢會傳回 **通訊協定** 和 **驅動程式** 類別，這是兩個參考來源類別的類別。


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



下列查詢只會傳回 **驅動程式** 類別，因為 **AssocClass** 關鍵字所放置的限制。


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



架構查詢語句參考的完整語法如下所示。 如需詳細的語法，請參閱 [語句的參考](references-of-statement.md)。


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> 架構關聯查詢可能會傳回重複的物件。

 

例如，下列查詢會在列舉 **根 \\ cimv2** 命名空間中的類別時，傳回 CIM 的「執行程式類型」多次。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem)


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
