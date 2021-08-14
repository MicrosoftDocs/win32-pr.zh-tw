---
description: 在資料查詢的 WHERE 子句中，使用 ISA 運算子來要求類別階層中的内嵌物件。
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: 資料查詢的 ISA 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33c0bc4b78101a4b1e6a38997518fec543b9eb49e42b28cbb2500c321f56ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318300"
---
# <a name="isa-operator-for-data-queries"></a>資料查詢的 ISA 運算子

在資料查詢的 WHERE 子句中，使用 ISA 運算子來要求類別階層中的内嵌物件。

下列範例顯示在類別階層中要求内嵌物件的語法。


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



結果包含類別的實例，該 **類別** 具有在 **EmbeddedProp** 屬性中衍生自 **ParentClass** 的内嵌物件。 並非 **類別** 物件的每個實例都是衍生自 **ParentClass**，但結果會傳回衍生自 **ParentClass** 的内嵌物件。

例如，在下列查詢中， **ClassA** 會包含弱類型的 **EmbeddedObj** 屬性。 **ClassA** 類別有10個實例。 其中五個實例的内嵌物件具有衍生自 **ClassZ** 的類型。 其他五個具有其他類型的内嵌物件。

下列範例顯示的查詢會傳回五個實例，其中包含衍生自 **ClassZ** 的物件。


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



