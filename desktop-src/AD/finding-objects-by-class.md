---
title: 依類別尋找物件
description: 特定物件類別的一般搜尋查詢。
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- 依類別 AD 尋找物件
- 依類別 Active Directory、使用、搜尋
- 物件廣告，依類別搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999570"
---
# <a name="finding-objects-by-class"></a>依類別尋找物件

特定物件類別的一般搜尋查詢。 下列程式碼範例會在組建7N 中搜尋具有位置的電腦。


```C++
(&(objectCategory=computer)(location=Building 7N))
```



考慮不使用 **objectClass** 的原因。 請勿使用 **objectClass** ，而不需要包含已編制索引之屬性的另一個比較。 索引屬性可以提高查詢的效率。 **ObjectClass** 屬性是多重值，且未建立索引。 若要指定物件的類型或類別，請使用 **objectCategory**。

效率較低：


```C++
(objectClass=computer)
```



更有效率：


```C++
(objectCategory=computer)
```



請注意，在某些情況下，必須使用 **objectClass** 和 **objectCategory** 的組合。 User 類別和 contact 類別應該依照下列方式指定。


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



請注意，您可以使用下列程式來搜尋使用者和連絡人。


```C++
(objectCategory=person)
```



 

 




