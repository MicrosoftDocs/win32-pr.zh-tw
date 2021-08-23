---
description: 針對 Tablet PC 使用客戶控制項的說明。
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: 使用自訂控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70699a141f0319f917953e25363db0e0cd38eb21ecc06345c581b55526ad6bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551878"
---
# <a name="using-custom-controls"></a>使用自訂控制項

您可以自訂標準控制項，方法是使用主控描繪來變更控制項的外觀，並建立超類別或子類別來變更控制項的行為。 在每個案例中，標準控制項類型的基礎系統程式碼會處理基本的控制函數。 如果您正確地使用這些控制項，就可以存取這些控制項。

以標準控制項為基礎的主控描繪控制項，會顯示為輔助功能輔助的標準控制項，並支援 Microsoft Active Accessibility;不過，它有自訂的外觀。 有些應用程式會使用自訂控制項來變更控制項的外觀，但主控描繪的控制項是更容易存取的方案。 如需如何定義主控描繪功能表和公開主控描繪控制項的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md)。

建立超級類別或子類別是自訂現有控制項行為的技巧。 視控制項的新行為而定，可能需要補充其公開的協助工具資訊。 例如，應用程式可以使用主控描繪的控制項，在選取的核取方塊中顯示 X，而不是以圖片（而非單字）標示命令按鈕。

使用屬於超類別或子類別的擁有者繪製控制項時：

-   提供所有控制項的標籤，即使在畫面上看不到標籤。 如果您自訂控制項，使標準標題無法顯示 (例如，具有圖形面的按鈕) ，並將標題保留為空白字串，協助工具輔助程式就無法取得標題並使用它來識別控制項。
-   確定支援 [**WM \_ GETTEXT**](../winmsg/wm-gettext.md) 。
-   確定支援所有類別特定的訊息。 更重要的是，支援如 [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) 和 [**LB \_ GETTEXT**](../controls/lb-gettext.md)等文字抓取訊息。 設定適當的樣式位，例如 **CBS \_ HASSTRINGS** 和 **磅 \_ HASSTRINGS**，以指出控制項支援這些訊息。

 

 
