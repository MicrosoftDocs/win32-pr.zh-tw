---
title: 判斷屬性類型
description: AttributeSchema 物件的 systemFlags 屬性包含一組旗標，這些旗標表示屬性物件的各種特性，例如屬性是否為已建立或非複寫。
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- 判斷屬性類型 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023254"
---
# <a name="determining-an-attribute-type"></a>判斷屬性類型

[**AttributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags)屬性包含一組旗標，這些旗標表示屬性物件的各種特性，例如屬性是否為已建立或非複寫。 下表列出 **systemFlags** 屬性的旗標，其會影響屬性的儲存類型。 

| 旗標值 | Description                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | 如果 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) 屬性中有此旗標，則不會複寫屬性。 |
| 0x00000004 | 如果 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) 屬性中有此旗標，則會建立屬性。    |



 

您可以建立查詢字串，以用來查詢已建立或非複寫的屬性。 例如，下列查詢字串會尋找所有非複寫的 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 物件。 請注意，查詢字串需要值的十進位對等專案，而不是值的十六進位對等專案。 如需此查詢字串所使用之比對規則 OID 的詳細資訊，請參閱 [如何指定比較值](how-to-specify-comparison-values.md)。


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



每個屬性之 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags)屬性會定義屬性是否已編制索引;索引屬性的值為1，非索引屬性的值為0。 例如，下列查詢字串會尋找代表已編制索引之屬性的 **attributeSchema** 物件。


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



每個屬性之 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset)屬性會定義屬性是否要複寫至通用類別目錄。 如果屬性是通用類別目錄的成員，則這個屬性的值為 **TRUE** ，如果屬性不在通用類別目錄中，則為 **FALSE** 。 例如，下列查詢字串會搜尋已複寫至通用類別目錄的 **attributeSchema** 物件。


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 