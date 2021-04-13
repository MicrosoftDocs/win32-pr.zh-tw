---
title: 查詢類別1或2個架構物件
description: AttributeSchema 和 classSchema 物件的 systemFlags 屬性是一個整數位遮罩，其中包含的旗標會指出屬性或類別的其他系統品質。
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- 查詢類別1或2個架構物件 AD
- 物件 AD，查詢類別1或2個架構物件
- 架構 AD，查詢類別1或2個架構物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314620"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>查詢類別1或2個架構物件

**AttributeSchema** 和 **ClassSchema** 物件的 **systemFlags** 屬性是一個整數位遮罩，其中包含的旗標會指出屬性或類別的其他系統品質。 [**ADS \_ SYSTEMFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)列舉包含的值，會對應至您可以在 **systemFlags** 屬性中設定的位。 您還無法設定額外的 **systemFlags** 位，例如，表示屬性或類別為類別1或類別2的0x10 位。 0x10 位是針對類別1物件所設定，也就是包含在系統所包含的基底架構中的類別和屬性。 未針對類別2屬性和類別設定位，這是架構的延伸。 如果 **attributeSchema** 或 **classSchema** 物件上沒有 **systemFlags** 屬性，則為類別2。

您可以使用 **LDAP \_ 比對 \_ 規則 \_ 位 \_ 和比** 對規則來搜尋在 **systemFlags** 屬性中設定了0x10 旗標的物件。 如需詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。

## <a name="querying-for-category-1"></a>查詢類別1

下列查詢字串會搜尋類別1屬性 (**attributeSchema** 物件，並在 **systemFlags** 屬性) 中設定0x10 位。


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



請注意，在上述範例中，LDAP 查詢語法需要十進位值;因此，旗標的十六進位值必須轉換成 decimal。 在此情況下，類別1位為0x10，因此篩選值必須指定為16。

## <a name="querying-for-category-2"></a>查詢類別2

下列查詢字串會在 [ **systemFlags** ] 屬性) 中， (**attributeSchema** 未設定0x10 位的物件來搜尋類別2屬性。


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



請注意，此查詢也會傳回沒有 **systemFlags** 屬性的 **attributeSchema** 物件，因此，隱含地不會設定指定的旗標。

 

 