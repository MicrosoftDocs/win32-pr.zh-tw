---
description: 描述事件查詢之 SELECT 語句的基本語法。
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: 事件查詢的 SELECT 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e36eaa8f396f8dd7b7c0b0c013d1d6738fefeb7ed2ae565ee7114ebb524faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315837"
---
# <a name="select-statement-for-event-queries"></a>事件查詢的 SELECT 語句

您可以使用各種 SELECT 語句來查詢事件資訊。 語句可以是基本語句，也可以更嚴格地縮減查詢所傳回的結果集。

下列範例是用來查詢事件資訊的基本 SELECT 語句。


```sql
SELECT * FROM EventClass
```



當取用者提交查詢時，會要求收到 **EventClass** 所代表事件的所有出現次數。 此要求包含有關所有事件系統和非系統屬性的通知要求。 當事件提供者提交查詢時，它會在 **EventClass** 所代表的事件發生時，註冊產生通知的支援。

取用者可以在 SELECT 語句中指定個別屬性，而不是星號 (\*) 。

下列範例示範如何查詢特定屬性。


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



但是，即使查詢指定内嵌物件屬性，也會傳回内嵌物件的所有屬性。

下列範例顯示兩個傳回相同資料的查詢。


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



如果系統屬性與特定查詢無關，則會包含 **Null**。 例如，所有事件查詢的 **\_ \_ RELPATH** 系統屬性值都是 **Null** 。

下列系統屬性包含事件查詢的 **Null** ：

<dl> \_\_命名 空間  
\_\_路徑  
\_\_RelPath  
\_\_伺服器  
</dl>

如需詳細資訊，請參閱 [WMI 系統屬性參考](wmi-system-properties.md)。

所有事件查詢都可以包含選擇性 [的 WHERE 子句](where-clause.md)，但 where 子句主要是供取用者用來指定其他篩選。 強烈建議取用者一律指定 WHERE 子句。 相較于傳遞和處理不必要通知的成本，複雜查詢的成本很低。

下列範例顯示的查詢會要求所有會影響假想類別 **EmailEvent** 的實例修改事件的通知。


```sql
SELECT * FROM EmailEvent
```



如果經常發生與 **EmailEvent** 相關聯的事件，取用者會產生事件。 只有當特定條件使用指定之類別的屬性（例如重要性層級很高）時，更好的查詢才會要求事件。

下列範例顯示當 **EmailImportance** 是 **EmailEvent** 類別的屬性時，您可以使用的查詢。


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



請注意，WMI 可能會因為許多原因而拒絕查詢。 例如，查詢可能太複雜或需要大量資源才能進行評估。 發生這種情況時，WMI 會傳回特定的錯誤碼，例如 **WBEM \_ E \_ 無效 \_ 查詢**。

内嵌物件的屬性可以在 WHERE 子句中使用。

下列範例示範如何查詢物件，其中 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)系統類別的 **TargetInstance** 屬性是內嵌的 [**win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)物件，而可 **空間** 是 **Win32 \_ LogicalDisk** 的屬性。


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>範例

TechNet 上 [特定進程名稱 VBScript 範例的監視器建立事件](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) 會使用 SELECT 語句來監視 Win32 進程的 WMI 實例建立事件 \_ ，並篩選特定的進程名稱。

 

 
