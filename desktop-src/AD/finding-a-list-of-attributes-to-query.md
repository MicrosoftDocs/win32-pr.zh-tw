---
title: 尋找要查詢的屬性清單
description: 搜尋特定類別的物件時，您的搜尋篩選中的比較應指定實際存在於該類別物件上的屬性。
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- 尋找要查詢 AD 的屬性清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0edfee59c42a8cf07be05ab31e58c0298f7285c8a02de659257e3b3cd14bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189188"
---
# <a name="finding-a-list-of-attributes-to-query"></a>尋找要查詢的屬性清單

搜尋特定類別的物件時，您的搜尋篩選中的比較應指定實際存在於該類別物件上的屬性。 若要取得特定類別之物件的清單屬性，請系結至抽象架構中的該類別，並取出 [**得到 iadsclass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) 和 **得到 iadsclass. OptionalProperties** 屬性。 如需詳細資訊，請參閱 [讀取抽象架構](reading-the-abstract-schema.md)。

此外，所有物件都是繼承自 top 抽象類別。 因此， **top** 中的任何屬性都可以存在，但可能不會在任何物件上設定。

如果要搜尋通用類別目錄，請務必在通用類別目錄中指定屬性。 包含在通用類別目錄中的屬性，其 **attributeSchema** 物件上的 **isMemberOfPartialAttributeSet** 會設定為 **TRUE** 。 請注意，此資料在抽象架構中無法使用。從架構容器中的 **attributeSchema** 物件讀取。

在通用類別目錄中，只有在符合下列兩個條件時，才可以查詢後置連結屬性：首先，屬性已標示為要包含在通用類別目錄中。 其次，對應的轉寄連結也會標示為要包含在通用類別目錄中。 這適用于查詢篩選和查詢結果。 如需詳細資訊，請參閱 [連結的屬性](linked-attributes.md)。

此外，也會建立一些大部分在使用者物件上的屬性。 查詢篩選不能包含已建立的屬性。 無法在查詢篩選中評估已建立的屬性;不過，它們可以在查詢結果中傳回。 這適用于所有命名內容和通用類別目錄。 所建立的屬性（attribute）會在 **attributeSchema** 物件的 **systemFlags** 屬性中， (0x00000004) 來 **\_ \_ \_ \_ 建造 SYSTEMFLAG ATTR** 的屬性。

> [!Note]  
> 如需系統隨附的預先定義類別和屬性的詳細資訊，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)。 這些頁面會列出每個物件類別的強制和選擇性屬性。 若為屬性，參考頁面會指出屬性是否已編制索引、已建立、連結或在通用類別目錄中。

 

 

 