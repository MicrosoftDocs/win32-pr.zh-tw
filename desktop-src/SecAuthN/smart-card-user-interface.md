---
description: 智慧卡使用者介面 (UI) 是單一的通用對話方塊，可讓使用者指定或搜尋智慧卡來開啟 (也就是在應用程式) 中連接和使用。
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: 智慧卡消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b94a82889d196b01f8a1d1ca6af7b4788398d9508accc2d5ca245f7929d9d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917328"
---
# <a name="smart-card-user-interface"></a>智慧卡消費者介面

智慧卡 [*使用者介面*](../secgloss/u-gly.md) (UI) 是單一的 [*通用對話方塊*](../secgloss/s-gly.md) ，可讓使用者指定或搜尋智慧卡來開啟 (也就是在應用程式) 中連接和使用。

以下是您可以使用 [一般] 對話方塊的兩種方式。 兩者都假設將顯示對話方塊 UI。 如需詳細資訊，請參閱 [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)。

**若要選取要開啟的智慧卡**

1.  宣告 **OPENCARDNAME** 型別的變數。
2.  在 [一般] 對話方塊中提供足夠的資訊，以縮小呼叫應用程式所要尋找之智慧卡的搜尋範圍。 這包括指定 **lpstrGroupNames**、 **lpstrCardNames** 和 **rgguidInterfaces**。 這也包括指定慣用的共用模式，以及當通用對話方塊使用 [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea)結構的 **dwShareMode** 和 **dwPreferredProtocols** 成員連接到卡片時所要使用的通訊協定。
3.  呼叫 [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) 函式，向使用者顯示通用對話方塊。 系統將會顯示簡單的說明資訊行，而且如果找到其中一個所要求的卡片，則會在顯示中反白顯示該卡片。 針對多個卡片名稱搜尋，會反白顯示包含其中一個慣用卡片的第一個讀取器。
4.  使用者接著選取卡片，然後按一下 **[確定]**，連接到智慧卡。

**搜尋特定卡片**

1.  宣告 **OPENCARDNAME** 型別的變數。
2.  在 [一般] 對話方塊中提供足夠的資訊，以縮小呼叫應用程式所要尋找之智慧卡的搜尋範圍。 這包括指定 **lpstrGroupNames**、 **lpstrCardNames** 和 **rgguidInterfaces**。
3.  建立 **連線**、**檢查** 和 **中斷連接** 回呼函數，並適當地設定 **lpfnConnect**、 **lpfnCheck** 和 **lpfnDisconnect** 資料成員。
    > [!Note]  
    > 以這種方式使用通用對話方塊時，所有三個函數和成員都必須可用。

     

4.  呼叫 [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) 通用對話方塊函數。
5.  [一般] 對話方塊接著會搜尋要求的卡片。 如果找到相符的卡片名稱或 [*ATR 字串*](../secgloss/a-gly.md)，就會依序呼叫 **連線**、**檢查** 和 **中斷連接** 回呼函數。 如果卡片通過 **檢查** 常式 (亦即， **檢查** 回呼會傳回 **TRUE**) ，則會在顯示中將此卡片反白顯示給使用者。
    > [!Note]  
    > 如果指定了多個卡片名稱，則第一個包含其中一個要求之卡片的讀取器，並通過 **檢查** 常式將會是選取的卡片。

     

6.  如果找不到相符專案，則會出現通用對話方塊。

 

 
