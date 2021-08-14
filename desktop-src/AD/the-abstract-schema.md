---
title: 抽象架構
description: 架構容器包含所有的 classSchema 和 attributeSchema 物件，這些物件會定義可存在於目錄樹系中的類別和屬性。
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- 抽象架構 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b46e4fefd52e786829e051a14714d2fec118b2ad42cdd95afcaa78b098b0f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182779"
---
# <a name="the-abstract-schema"></a>抽象架構

架構容器包含所有的 **classSchema** 和 **attributeSchema** 物件，這些物件會定義可存在於目錄樹系中的類別和屬性。 架構容器也包含名為 Aggregate of 類別 **ubschema** 的物件。 這個 **ubschema** 物件稱為抽象架構。

抽象架構包含 **classSchema** 和 **attributeSchema** 物件中所儲存之資料的子集。 其目的是要提供簡單且有效率的機制，以供您用來抓取類別和屬性定義的常用元素。 例如，若要抓取物件類別的選擇性和強制屬性，請系結至多個物件，以從類別及其所有的超類收集 **mayContain**、 **mustContain**、 **systemMayContain** 和 **systemMustContain** 值，以及從類別的任何輔助類別和其超類收集。 抽象架構可方便地收集單一物件中的所有資料。

如同 Active Directory Domain Services 中的任何物件，您可以系結至 **ubschema** 物件並讀取其屬性，以剖析字串值以取得所需的資料。 不過，ADSI 會提供一組介面，讓您更輕鬆地讀取抽象架構。 如需詳細資訊，請參閱 [讀取抽象架構](reading-the-abstract-schema.md)。

下表列出 **ubschema** 物件的索引鍵屬性。



| 屬性                 | 描述                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | 包含字串的多重值屬性，這些字串代表架構中的每個屬性。 每個值都包含 **attributeID**、 **lDAPDisplayName**、 **attributeSyntax**、 **rangeLower**、 **rangeUpper**，以及指出屬性是否可以有多個值的專案。 |
| **extendedAttributeInfo** | 多值屬性，其中包含代表每個屬性之其他資料的字串。 每個值都包含 **attributeID**、 **lDAPDisplayName**、 **schemaIDGUID** 和 **attributeSecurityGUID**。                                                                          |
| **extendedClassInfo**     | 多值屬性，其中包含代表每個類別之其他資料的字串。 每個值都包含類別的 **governsID**、 **lDAPDisplayName** 和 **schemaIDGUID** 。                                                                                              |
| **objectClasses**         | 多值屬性，其中包含表示架構中每個類別的字串。 每個值都包含 **governsID**、 **lDAPDisplayName**、 **mustContain**、 **mayContain** 等等。                                                                                           |



 

 

 




