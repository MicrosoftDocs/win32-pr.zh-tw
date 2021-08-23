---
description: 對顯示裝置的系統選擇區進行變更，可能會對桌面上的 windows 所使用的色彩有很大的影響，有時也會造成不良的影響。
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: 選用區訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a82c5ae2727e9f687f5f7fb628279b7832e896991f703225beec075a6630133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558438"
---
# <a name="palette-messages"></a>選用區訊息

對顯示裝置的系統選擇區進行變更，可能會對桌面上的 windows 所使用的色彩有很大的影響，有時也會造成不良的影響。 為了將這些變更的影響降到最低，系統會提供一組訊息來協助應用程式管理其邏輯調色板，同時確保使用中視窗中的色彩盡可能接近所需的色彩。

系統會在啟用視窗之前，將 [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) 訊息傳送至最上層或重迭的視窗。 此訊息讓應用程式有機會選取並實現其邏輯調色板，讓它能獲得其邏輯調色板最可能的色彩對應。 當應用程式收到訊息時，它應該使用 [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette)、 [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)和 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 函式來選取並實現邏輯調色板。 這麼做會指示系統更新系統元件中的色彩，使其色彩盡可能符合邏輯調色板中的多個色彩。

當應用程式因為實現其邏輯調色板而導致系統元件的變更時，系統會將 [**WM \_ PALETTECHANGED**](wm-palettechanged.md) 訊息傳送至所有最上層和重迭的視窗。 此訊息讓應用程式有機會更新其視窗的用戶端區域中的色彩，並以更接近預期色彩的色彩來取代已變更的色彩。 接收 **WM \_ PALETTECHANGED** 訊息的應用程式應該使用 [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) 和 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 來重設與所有非作用中視窗相關聯的邏輯調色板，然後使用 [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) 函式，針對每個非使用中的視窗更新工作區中的色彩。 這項技術並不保證會有最大的精確色彩相符專案;不過，它確實會確保邏輯調色板中的色彩會對應到系統調色板中合理的色彩。

> [!Note]  
> 若要避免建立無限迴圈，應用程式永遠不應該知道控制碼符合在 [**WM \_ PALETTECHANGED**](wm-palettechanged.md)訊息的 *wParam* 參數中所傳遞之控制碼的視窗的調色板。

 

[**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors)函式通常會比重繪區域更快地更新非作用中視窗的工作區。 不過，由於 **UpdateColors** 會根據系統元件的每個圖元色彩來執行色彩轉譯，因此對此函式的每個呼叫都會導致某些色彩精確度遺失。 這表示當視窗變成使用中狀態時， **UpdateColors** 無法用來更新色彩。 在這種情況下，應用程式應該重新繪製工作區。

當對邏輯元件進行變更時，系統可能會傳送 [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) 訊息。 此外，系統可能會在系統調色板即將變更時，將 [**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md) 訊息傳送至所有最上層和重迭的視窗。

 

 



