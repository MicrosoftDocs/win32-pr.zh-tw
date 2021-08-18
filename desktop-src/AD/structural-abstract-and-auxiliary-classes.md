---
title: 結構化、抽象類別和輔助類別
description: ClassSchema 物件的 objectClassCategory 屬性可以有值（如下表所示），指出類別是結構化、抽象或輔助。
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- 結構化、抽象類別和輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393c08f5c26690d5b08b76dfea8ab4ff2833c94851a10ddcea2a69209279fbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024706"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>結構化、抽象類別和輔助類別

**ClassSchema** 物件的 **objectClassCategory** 屬性可以有值（如下表所示），指出類別是結構化、抽象或輔助。



| 值 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 結構化類別，這是唯一可在 Active Directory Domain Services 中具有實例的類別類型。 結構化類別可以是抽象或結構化類別的子類別。 結構化類別可在其定義中包含任意數目的輔助類別。                                                                                                                                                                                                                                           |
| 2     | 抽象類別，此類別是用來衍生新的抽象、輔助和結構化類別的範本。 抽象類別只能是抽象類別的子類別。 抽象類別無法在 Active Directory Domain Services 中具現化。 抽象類別可在其定義中包含任意數目的輔助類別。                                                                                                                                                                                   |
| 3     | 輔助類別可包含在結構化、抽象或輔助類別的定義中，在此情況下，會將輔助類別的 **mustContain**、 **systemMustContain**、 **mayContain** 和 **systemMayContain** 值加入至類別的定義中。 輔助類別可以是抽象或輔助類別的子類別。 輔助類別無法在 Active Directory Domain Services 中具現化。 輔助類別可在其定義中包含任意數目的輔助類別。 |



 

請勿將 **objectClassCategory** 與 [物件類別](object-class-and-object-category.md)混淆。

 

 




