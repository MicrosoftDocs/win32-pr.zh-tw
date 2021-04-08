---
title: 依名稱尋找物件
description: Active Directory Domain Services 中的大部分物件都會使用 cn 屬性作為其命名屬性。
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- 依名稱 Active Directory、使用、搜尋
- 物件廣告，依名稱搜尋
- 依名稱尋找物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671279"
---
# <a name="finding-objects-by-name"></a>依名稱尋找物件

Active Directory Domain Services 中的大部分物件都會使用 **cn** 屬性作為其命名屬性。 不過，某些物件會使用 **cn** 以外的命名屬性。 例如，網域控制站會使用命名屬性的 **domainDNS** 屬性，而組織單位會使用 **organizationalUnit** 屬性作為命名屬性。 為了避免必須針對不同的物件類型使用不同的命名屬性，必須使用 **name** 屬性（包含物件的相對辨別名稱）來依名稱搜尋物件。

## <a name="examples"></a>範例

下列程式碼範例會顯示不同的查詢字串，可用來依名稱尋找物件。

下列查詢字串會尋找名稱開頭為 "Jeff" 的所有物件。


```C++
(name=Jeff*)
```



下列查詢字串會尋找名稱開頭為 "租借" 或 "corp" 的所有電腦物件。


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



下列查詢字串會尋找所有使用者，以及名稱開頭為 "張穎" 或 "Jeff" 的使用者。


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




