---
description: 邏輯調色板是應用程式建立並與指定的裝置內容產生關聯的色調色板。
ms.assetid: 7cc86771-237d-4539-8f48-2474edb764a4
title: 邏輯調色板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597e049c4320ff3ac30099e767c35a3438237904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972656"
---
# <a name="logical-palette"></a>邏輯調色板

*邏輯調色板* 是應用程式建立並與指定的裝置內容產生關聯的色調色板。 邏輯調色板可讓應用程式定義和使用符合其特定需求的色彩。 應用程式可以建立任意數目的邏輯調色板，將它們用於不同的裝置內容，或在它們之間切換以取得單一裝置內容。 應用程式可以建立的最大調色板數目取決於系統的資源。

應用程式會使用 [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) 函數來建立邏輯調色板。 應用程式會填滿 [**LOGPALETTE**](/windows/win32/api/wingdi/ns-wingdi-logpalette) 結構，此結構會指定專案數和每個專案的色彩值，然後應用程式會將結構傳遞至 **CreatePalette**。 此函式會傳回應用程式在所有後續作業中用來識別調色板的調色板控制碼。 若要在邏輯調色板中使用色彩，應用程式會使用 [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) 函式將選擇區選取到裝置內容中，然後使用 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 函式來瞭解該調色板。 當邏輯調色板可供使用時，就可以使用調色板中的色彩。

應用程式應該將其邏輯調色板的大小限制為只有足夠的專案，才能代表所需的色彩。 應用程式無法建立大於最大調色板大小的邏輯調色板，也就是與裝置相關的值。 應用程式可以使用 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函數來取得 SIZEPALETTE 值，以取得大小上限。

雖然應用程式可以為邏輯調色板中的指定專案指定任何色彩值，但並非所有色彩都能由指定的裝置產生。 系統不會提供方法來找出支援的色彩，但應用程式可以藉由抓取裝置的色彩解析度，來探索這些色彩的總數目。 色彩解析度（以每圖元的色彩位指定）等於 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函數所傳回的 COLORRES 值。 具有18色解析度的裝置具有262144可能的色彩。 如果應用程式要求不支援的色彩，系統會選擇適當的近似值。

建立邏輯調色板之後，應用程式就可以使用 [**SetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries) 函式來變更調色板中的色彩。 如果已選取並實現邏輯調色板，變更調色板不會立即影響所顯示的色彩。 應用程式必須使用 [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) 和 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 函數來更新色彩。 在某些情況下，應用程式可能需要取消選取、unrealize、選取並實現邏輯調色板，以確保色彩會依照要求的方式更新。 如果應用程式在一個以上的裝置內容中選取一個邏輯調色板，則對邏輯元件的變更將會影響所選取的所有裝置內容。

應用程式可以使用 [**ResizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette) 函數來變更邏輯調色板中的專案數。 如果應用程式縮減大小，其餘的專案就不會變更。 如果應用程式擴充大小，系統會將每個新專案的色彩設定為黑色 (0、0、0) ，並將旗標設定為零。

應用程式可以使用 [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries) 函式，以取得指定邏輯調色板中專案的色彩和旗標值。 應用程式可以使用 [**GetNearestPaletteIndex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex) 函式，以取得最接近指定之色彩值的指定邏輯調色板中專案的索引。

當應用程式不再需要邏輯元件時，可以使用 [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) 函數將它刪除。 在刪除調色板之前，應用程式必須確定邏輯調色板不再被選取到裝置內容中。

 

 



