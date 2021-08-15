---
title: 靜態連結的輔助類別
description: 靜態連結的輔助類別是一種，包含在架構中物件類別之 classSchema 定義的 auxiliaryClass 或 systemAuxiliaryClass 屬性中。
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- 靜態連結的輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce00592052b1b52f82e2758fdfd7241c6bd24233ce6db6c11389165eeaa5e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024716"
---
# <a name="statically-linked-auxiliary-classes"></a>靜態連結的輔助類別

靜態連結的輔助類別是一種，包含在架構中物件類別之 **classSchema** 定義的 **auxiliaryClass** 或 **systemAuxiliaryClass** 屬性中。 這表示輔助類別是與其相關聯之類別的每個實例的一部分。

在定義類別時，輔助類別可以靜態連結到物件類別，也就是將其 **classSchema** 物件加入至架構容器時。 這是唯一可以使用 **systemAuxiliaryClass** 的時間;建立 **classSchema** 物件之後，就無法修改其 **systemAuxiliaryClass** 屬性。 此時靜態連結的輔助類別可以具有強制 (**mustHave**) 和/或選擇性 (**mayHave**) 屬性。

具有延伸架構所需許可權的特殊許可權使用者，可以從現有 **classSchema** 物件的 **systemAuxiliaryClass** 屬性新增或移除輔助類別。 這樣做會從物件類別的每個現有實例加入或移除輔助類別。 此時靜態連結的輔助類別可以有選擇性屬性，但不能有必要的屬性。 這是因為可能有物件類別的現有實例，在這種情況下，加入新的強制屬性會造成問題。 具有特殊許可權的使用者之後可以從 **classSchema** 物件的 **auxiliaryClass** 屬性中移除輔助類別。

 

 




