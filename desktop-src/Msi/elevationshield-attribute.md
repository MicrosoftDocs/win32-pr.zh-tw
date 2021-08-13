---
description: 這個屬性會將 [使用者帳戶控制] (UAC) 提高許可權圖示 (盾牌圖示) 新增至按鈕控制項。
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: ElevationShield 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4c5da7133a7216386be56328c0e21e2e365129caa185e045984cb5e89b7d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637488"
---
# <a name="elevationshield-attribute"></a>ElevationShield 屬性

這個屬性會將 [ [*使用者帳戶控制*](u-gly.md) ] (UAC) 提高許可權圖示 (盾牌圖示) 新增至 [按鈕控制項](pushbutton-control.md)。

如果設定此位，且安裝尚未以較 [*高*](e-gly.md) 的許可權執行，則會使用 [ [*使用者帳戶控制*](u-gly.md) ] (UAC) 提高許可權圖示 (盾牌圖示) 建立按鈕控制項。

如果設定此位，而且安裝已經以較 [*高*](e-gly.md) 的許可權執行，則會使用其他圖示屬性來建立按鈕控制項。

如果未設定此位，則會使用其他圖示屬性來建立按鈕控制項。

## <a name="valid-controls"></a>有效的控制項

[按鈕](pushbutton-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



