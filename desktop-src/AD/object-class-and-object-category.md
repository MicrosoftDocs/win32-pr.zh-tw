---
title: 物件類別和物件類別
description: 物件類別的每個實例都有一個多重值的 objectClass 屬性，它會識別物件為其實例的類別，以及衍生該類別的所有結構化或抽象的超類。
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74941b4f32cc197d3dbbf3aa0dc3179b4098ee8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933051"
---
# <a name="object-class-and-object-category"></a>物件類別和物件類別

物件類別的每個實例都有一個多重值的 [**objectClass**](/windows/desktop/ADSchema/a-objectclass) 屬性，它會識別物件為其實例的類別，以及衍生該類別的所有結構化或抽象的超類。 因此，使用者物件的 **objectClass** 屬性會識別 [**top**](/windows/desktop/ADSchema/c-top)、 [**person**](/windows/desktop/ADSchema/c-person)、 [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)和 [**user**](/windows/desktop/ADSchema/c-user) 類別。 **ObjectClass** 屬性不包含清單中的輔助類別。 系統會在建立物件實例時設定 **objectClass** 值，而且無法變更。

物件類別的每個實例也都有一個 [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) 屬性，這是單一值屬性，其中包含物件是實例或其一個超類的類別的分辨名稱。 當建立物件時，系統會將其 **objectCategory** 屬性設定為其物件類別的 [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) 屬性所指定的值。 無法變更物件的 **objectCategory** 屬性。

如需詳細資訊，以及抓取物件之 [**objectclass**](/windows/desktop/ADSchema/a-objectclass) 屬性的程式碼範例，請參閱抓取 [objectClass 屬性](retrieving-the-objectclass-property.md)。

> [!IMPORTANT]
> 在 Windows Server 2008 之前， [**objectClass**](/windows/desktop/ADSchema/a-objectclass) 屬性尚未編制索引。 這是因為它有多個值，且高度不是唯一的。也就是說， **objectClass** 屬性的每個實例都包含 [**最上層**](/windows/desktop/ADSchema/c-top) 類別。 這表示索引會很大且無效。 若要找出指定類別的物件，請使用 [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) 屬性，此屬性是單一值和索引。 如需在搜尋篩選中使用這些屬性的詳細資訊，請參閱 [決定要尋找的內容](deciding-what-to-find.md)。

 

對於大部分的類別而言， [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) 是類別的 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 物件的分辨名稱。 例如， [**organizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit)類別的 **DEFAULTOBJECTCATEGORY** 是 "CN = 組織單位，CN = Schema，cn = Configuration，<DC = forestroot>"。 不過，有些類別會將另一個類別稱為 **defaultObjectCategory**。 這可讓查詢輕鬆地尋找相關物件的群組，即使它們是不同的類別也一樣。 例如，[**使用者**](/windows/desktop/ADSchema/c-user)、 [**person**](/windows/desktop/ADSchema/c-person)、 [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)和 [**contact**](/windows/desktop/ADSchema/c-contact)類別都會在其 **defaultObjectCategory** 屬性中識別 **person** 類別。 這可讓 (objectCategory = person) 之類的搜尋篩選，以單一查詢找出所有這些類別的實例。 人們的查詢非常常見，因此這是簡單的優化。

如果您從結構化類別建立子類別，最佳作法是將新類別的 [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) 值設定為相同的超類別分辨名稱。 這可讓標準 UI 「尋找」子類別。

 

 