---
description: 用來控制物件屬性存取權的 Ace
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: 用來控制物件屬性存取權的 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fddd5d78ff5b02bbbe4b9b7a7ce0b77d7be263f9fd3926f44411469af2bb3c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785247"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>用來控制物件屬性存取權的 Ace

目錄服務的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL)  (DS) 物件可以包含 (ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 階層，如下所示：

1.  保護物件本身的 Ace
2.  保護物件上指定之屬性集的[特定物件 ace](object-specific-aces.md)
3.  保護物件上指定之屬性的物件特定 Ace

在此階層中，在較高層級授與或拒絕的許可權也適用于較低層級。 例如，如果屬性集上的特定物件 ACE 允許信任者的 ADS \_ right \_ DS \_ 讀取配置 \_ ，則信任者對該屬性集的所有屬性具有隱含的讀取存取權。 同樣地，物件本身上的 ACE （可讓 ADS 使用 \_ 正確的 \_ DS \_ 讀取 \_ 屬性存取）可讓受信任者讀取所有物件的屬性。

下圖顯示假設 DS 物件及其屬性集和屬性的樹狀結構。

![目錄服務物件階層](images/accctrl2.png)

假設您想要允許下列存取此 DS 物件的屬性：

-   允許群組所有物件屬性的讀取/寫入權限
-   允許其他人讀取/寫入所有屬性（屬性 D 除外）的許可權

若要這樣做，請在物件的 DACL 中設定 Ace，如下表所示。



| 受託 人  | 物件 GUID    | ACE 類型                  | 存取權限                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| 群組 A  | 無           | 存取-允許的 ACE        | ADS \_ 正確 \_ 的 \_ DS \_ 讀取 \| \_ 目錄廣告正確的 \_ DS \_ 寫入 \_ |
| 所有人 | 屬性集1 | 存取-允許的物件 ACE | ADS \_ 正確 \_ 的 \_ DS \_ 讀取 \| \_ 目錄廣告正確的 \_ DS \_ 寫入 \_ |
| 所有人 | 屬性 C     | 存取-允許的物件 ACE | ADS \_ 正確 \_ 的 \_ DS \_ 讀取 \| \_ 目錄廣告正確的 \_ DS \_ 寫入 \_ |



 

群組 A 的 ACE 沒有物件 GUID，這表示它允許存取所有物件的屬性。 屬性集1的物件特定 ACE 可讓每個人都能存取屬性 A 和 B。其他特定物件 ACE 可讓每個人都能存取屬性 C。請注意，雖然這個 DACL 沒有任何拒絕存取的 Ace，但是它會隱含地拒絕屬性 D 存取群組 A 以外的所有人。

當使用者嘗試存取物件的屬性時，系統會依序檢查 Ace，直到明確授與、拒絕要求的存取權，或沒有其他 Ace 為止（在這種情況下，會隱含拒絕存取）。

系統會評估：

-   套用至物件本身的 Ace
-   套用至屬性集的物件特定 Ace，其中包含正在存取的屬性
-   套用至所存取屬性的特定物件 Ace

系統會忽略適用于其他屬性集或屬性的物件特定 Ace。

 

 
