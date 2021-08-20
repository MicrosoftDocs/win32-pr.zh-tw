---
title: 高對比參數
description: 高對比參數表示使用者是否希望前景和背景視覺效果所使用的色彩之間有高對比。
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c268acbf95981e70e8e0d36843cfd9abfe9c1b459e1193dc2176032dec5a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929639"
---
# <a name="high-contrast-parameter"></a>高對比參數

高對比參數表示使用者是否希望前景和背景視覺效果所使用的色彩之間有高對比。

使用者可以使用主控台中的輕鬆存取中心來控制高對比參數的設定，或使用其他應用程式來自訂環境。 應用程式會使用 **spi \_ GETHIGHCONTRAST** 和 **spi \_ SETHIGHCONTRAST** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定高對比參數。

在初始化期間，以及處理 [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) 訊息時，應用程式應該判斷高對比參數的狀態。 為了進行這項判斷，應用程式應該使用 **SPI \_ GETHIGHCONTRAST** 旗標來呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) ，以取得 [**systeminformation.highcontrast**](/windows/win32/api/winuser/ns-winuser-highcontrasta)結構。 如果 **systeminformation.highcontrast** 結構的 **dwFlags** 成員已設定 **HCF \_ HIGHCONTRASTON** 位，則會啟用高對比功能，應用程式應該執行下列作業：

-   將所有色彩對應到一對前景和背景色彩。 您可以使用 [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) 函式來決定適當的前景和背景色彩，方法是使用 **色彩 \_ WINDOWTEXT** 和 **色彩 \_ 視窗** 的組合，或 **色彩 \_ BTNTEXT** 和 **色彩 \_ BTNFACE** 的組合。 **GetSysColor** 函式會透過主控台傳回使用者所選取的色彩。
-   略過通常會顯示在文字後方的任何點陣圖影像。 這類影像會以視覺方式分散到需要高對比的使用者。
-   通常會以多個色彩繪製的影像，應使用針對文字選取的前景和背景色彩來繪製。

此外，應用程式也會使用 **spi \_ GETDISABLEOVERLAPPEDCONTENT** 和 **spi \_ SETDISABLEOVERLAPPEDCONTENT** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定重迭的內容參數。 顯示功能（例如背景影像、紋理材質、檔上的水位線、Alpha 混色和透明度）可以降低前景與背景的對比，讓視力較低的使用者更難看到畫面上的物件。 這個旗標可讓應用程式判斷是否已停用這類重迭的內容

 

 