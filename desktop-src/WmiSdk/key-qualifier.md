---
description: 金鑰辨識符號會指出屬性是否為命名空間控制碼的一部分。
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: 金鑰辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae5525aa85ab744e7e6824bb6079511a3611643d53594503e70c8e587f363cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555887"
---
# <a name="key-qualifier"></a>金鑰辨識符號

**金鑰** 辨識符號會指出屬性是否為命名空間控制碼的一部分。 如果有一個以上的屬性具有索引 **鍵** 限定詞，則所有這類屬性統稱 (複合索引鍵) 。 在一起時，索引鍵屬性必須提供每個類別實例的唯一參考。 如果將這個限定詞放置在屬性上，則只允許值 **TRUE** 。

除了下列以外，您可以使用任何屬性類型：

-   陣列
-   實數和浮點數
-   內嵌物件
-   低於 ASCII 32 的字元 (也就是空白字元) 
-   **Char16** 類型的字元字串或定義為索引鍵的字元字串，必須包含大於 U + 0020 的值。 這是因為 WMI 會在物件路徑中使用索引鍵值，而您無法在物件路徑中使用非列印字元。

當父類別指定索引鍵時，衍生自父類別的所有類別都會繼承該索引鍵。 衍生的類別無法改變繼承的索引鍵，或定義任何新的索引鍵屬性。 但是，當您從沒有索引鍵的抽象類別衍生子類別時，您可以在子類別中引入一個索引鍵。

定義一個以上實例的所有類別都必須指定索引鍵。 因為抽象類別不會定義任何實例，所以不需要指定索引鍵。 因為 singleton 類別只會定義一個實例，所以無法指定索引鍵。

在物件具現化時，金鑰會寫入一次，且稍後不得修改。 將預設值套用至索引鍵限定屬性並不合理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

 




