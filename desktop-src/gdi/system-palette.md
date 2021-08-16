---
description: 系統會為每個使用調色板的裝置維護一個系統元件。
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: 系統元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e540bd4068989a3c457568c2451dbc91f77755065f3bc70af03f9577fcebee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698130"
---
# <a name="system-palette"></a>系統元件

系統會為每個使用調色板的裝置維護一個 *系統元件* 。 系統選擇區包含目前可由裝置顯示或繪製的所有色彩的色彩值。 除了查看系統元件的內容之外，應用程式無法直接存取系統調色板。 相反地，系統會完全掌控系統元件，並只允許透過使用邏輯調色板來存取。

應用程式可以使用 [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) 函數來查看系統元件的內容。 此函式會抓取一或多個專案的內容，最多可達系統選擇區中的總專案數。 Total 永遠等於 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式針對 SIZEPALETTE 值傳回的數位，與任何指定之邏輯調色板的大小上限相同。

雖然應用程式無法直接變更系統調色板中的色彩，但它們可能會在實現邏輯調色板時造成變更。 為了實現調色板，系統會檢查每個要求的色彩，並嘗試在包含完全相符專案的系統元件中尋找專案。 如果系統找到相符的色彩，則會將邏輯調色板索引對應至對應的系統元件索引。 如果系統找不到完全相符的專案，它會在對應索引之前將要求的色彩複製到未使用的系統元件專案。 如果所有的系統調色板專案都在使用中，系統會將邏輯調色板索引對應到最符合所要求色彩的系統調色板專案。 設定此對應之後，應用程式就無法覆寫它。 例如，應用程式無法使用系統調色板索引來指定色彩;只允許邏輯調色板索引。

應用程式可以藉由將 [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85))結構的 **peFlags** 成員設定為建立邏輯選擇區時選取的值，來修改對應的索引方式。 例如，電腦 \_ NOCOLLAPSE 旗標會指示系統立即將要求的色彩複製到未使用的系統調色板專案，不論系統調色板專案是否已包含該色彩。 此外，電腦 \_ 明確旗標會指示系統將邏輯調色板索引對應至明確指定的系統調色板索引。  (應用程式會在 **PALETTEENTRY** 結構的低序位字組中提供系統調色板索引。 ) 

您可以分別針對 [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette)函式中的 *BForceBackground* 參數指定 **TRUE** 或 **FALSE** ，以將調色板視為背景調色板或前景調色板。 系統中一次只能有一個前景調色板。 如果視窗是目前使用中視窗或目前使用中視窗的子系，則可以實現前景調色板。 否則，不論 *bForceBackground* 參數的值為何，都能將調色板視為背景調色板。 前景調色板的重要屬性是，在實現時，它可以覆寫所有專案 (除了系統元件中) 的靜態專案以外。 系統會將系統選擇區中非靜態的所有專案標示為在前景調色板的實現之前未使用，藉此完成此工作，藉此排除所有使用的專案。 系統調色板上不會發生前置處理，以提供背景調色板。 前景調色板會設定所有可能的非靜態色彩。 背景調色板只能設定保持開啟狀態，並以先進先出的方式設定優先順序。 一般而言，應用程式會使用適用于子視窗的背景調色板，以實現自己的個別調色板。 這有助於將系統調色板所發生的變更數目降至最低。

未使用的系統調色板專案是指任何未保留且不含靜態色彩的專案。 保留的專案會明確標示電腦 \_ 保留值。 當應用程式發現適用于調色板動畫的邏輯元件時，就會建立這些專案。 靜態色彩專案是由系統建立，並且對應至預設調色板中的色彩。 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)函式可用來取得 NUMRESERVED 值，此值會指定保留給靜態色彩的系統調色板專案數目。

由於系統選擇區的專案數目有限，因此選取並實現指定裝置的邏輯調色板可能會影響與相同裝置的其他邏輯調色板相關聯的色彩。 這些色彩變更在顯示器上出現時特別明顯。 應用程式可以在每次使用時重設調色板，以確保其目前選取的邏輯調色板使用合理的色彩。 應用程式會藉由呼叫 [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) 和 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 函式重設調色板。 使用這些函式會導致系統將邏輯調色板中的色彩重新對應到系統調色板中合理的色彩。

 

 
