---
description: 描述資料查詢的 SELECT 語句。
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: 資料查詢的 SELECT 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fec0526c5e5d47a74d6e165726222f9e521bd7102072e5a4b79e960f8dae19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315946"
---
# <a name="select-statement-for-data-queries"></a>資料查詢的 SELECT 語句

您可以使用各種 SELECT 語句來查詢資訊。 語句可以是基本語句，也可以更嚴格地縮減查詢所傳回的結果集。

下列範例是用來查詢資料的基本 SELECT 語句。


```sql
SELECT * FROM Class
```



這個語句會傳回指定之類別及其任何子類別的實例。 系統會包含類別的所有系統和使用者定義屬性。 如果系統屬性與特定查詢無關，則會包含 **Null**。

您可以使用數種技術來減少取出結果集所需的頻寬，如果查詢的執行結果太多，而且使用者只對屬性子集感興趣。 首先，查詢可以將星號取代為所需的屬性。

下列範例示範如何查詢特定屬性。


```sql
SELECT property_1, property_2, property_3 FROM class
```



結果集會包含所有系統屬性和指定的非系統屬性。

縮小查詢結果集範圍的另一個方法是使用 [**\_ \_ 類別**](wmi-system-properties.md)系統屬性。 依預設，查詢會傳回指定之類別及其子類別的所有實例。 您可以使用 **\_ \_ 類別** 系統屬性，只要求指定類別的實例，但不包括其子類別。

下列範例示範如何在 WHERE 子句中使用 [**\_ \_ 類別**](wmi-system-properties.md)系統屬性。


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



您也可以使用 [**\_ \_ 類別**](wmi-system-properties.md)系統屬性，將結果集限制為特定子類別的實例。

下列範例顯示如何將結果集限制為特定子類別的實例。


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> 如果您使用不正確內嵌物件路徑來建立查詢，則您的查詢不會傳回錯誤或任何結果。

 

下列範例會傳回 **MainClass** 的實例，假設 **MainClass** 的實例存在，其包含屬性 **P \_ Uint32** 等於 "70011" 的内嵌物件 **EmbedObj** 。


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



下列範例不會傳回任何結果，也不會傳回錯誤，假設 **MainClass** 實例中 **EmbedObj** 的内嵌物件沒有 **無效** 的屬性。


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



