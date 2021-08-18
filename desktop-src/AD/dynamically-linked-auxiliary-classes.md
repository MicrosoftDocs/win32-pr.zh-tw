---
title: 動態連結的輔助類別
description: 動態連結的輔助類別是附加至個別物件的類別，而不是附加至物件類別的類別。
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- 動態連結的輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5fc73ef64e1ed4af0dd73879dc1cd7ed8b2d82ac1d397db001c1487680b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695371"
---
# <a name="dynamically-linked-auxiliary-classes"></a>動態連結的輔助類別

動態連結的輔助類別是附加至個別物件的類別，而不是附加至物件類別的類別。 動態連結可讓您以個別物件儲存其他屬性，而不會對整個類別的架構定義進行延伸整個樹系的影響。 例如，企業可以使用動態連結，將銷售特定的輔助類別附加至其銷售人員的使用者物件，以及其他部門專屬的輔助類別附加至其他部門中員工的使用者物件。

動態連結不復雜：將輔助類別的名稱加入至物件的 **objectClass** 屬性值。 如果輔助類別具有任何必要屬性 (**mustHave** 或 **SystemMustHave**) ，您必須同時設定它們。 如需詳細資訊和程式碼範例，請參閱 [將輔助類別加入至物件實例](adding-an-auxiliary-class-to-an-object-instance.md)。

若要移除動態連結的輔助類別，請清除輔助類別中所有屬性的值，然後從物件的 **objectClass** 屬性中移除輔助類別的名稱。

如果您動態加入的輔助類別是另一個輔助類別的子類別，則會將這兩個輔助類別新增至目標物件。 不過，移除子輔助類別並不會移除其父系;每個類別都必須明確移除。

 

 




