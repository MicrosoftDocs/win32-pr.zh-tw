---
description: 指定包含排序屬性或排序屬性清單的元素，以指定排序別名或排序別名的清單。
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: System.management.automation.aliasinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974608"
---
# <a name="aliasinfo"></a>System.management.automation.aliasinfo

指定包含排序屬性或排序屬性清單的元素，以指定排序別名或排序別名的清單。 每個[propertyDescription](./propdesc-schema-propertydescription.md)專案都只能有一個[system.management.automation.aliasinfo]()元素。 針對設定 canGroupBy = true 的屬性，除非指定了次要 sort 屬性 (aliasInfo/@additionalSortByAliases =： example) ，否則使用者可能會在依屬性分組的視圖中變更排序次序時遇到非預期的行為。 具體來說，群組的順序將會變更，但群組內的專案順序則不會變更。

## <a name="syntax"></a>Syntax


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>項目資訊



| Parent 項目                                                   | 子元素 |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | 無           |



 

## <a name="attributes"></a>屬性



| 屬性               | 描述                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | 公用。 選擇性。 應該用來排序的屬性的標準名稱。 這個字串的型別是標準型別。                                            |
| additionalSortByAliases | 公用。 選擇性。 要在排序時使用的其他屬性清單（以分號分隔）。 這些屬性會套用到其指定順序中的排序。 |



 

 

 
