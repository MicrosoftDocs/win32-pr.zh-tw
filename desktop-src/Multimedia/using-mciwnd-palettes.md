---
title: 使用 MCIWnd 調色板
description: 使用 MCIWnd 調色板
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette 宏
- MCIWndSetPalette 宏
- MCIWndRealize 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074dece2c1dac95e24a465413cae686acea5a8e9055913bfb832341efdb12c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801117"
---
# <a name="using-mciwnd-palettes"></a>使用 MCIWnd 調色板

使用8位色彩深度播放影片剪輯 (256-色彩容量) 需要有一個調色板來定義所要使用的色彩。 有時候，影片剪輯隨附的調色板不是播放期間最適合使用的調色板。 在此情況下，MCIWnd 提供三種方式來管理用來播放的調色板：

-   使用 [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) 宏，取出與 MCIWnd 視窗相關聯之調色板的控制碼。 選擇區不一定會與 [MCIWnd] 視窗建立關聯。 其他應用程式可以存取，甚至使調色板控制碼失效。 因此，您的應用程式應該預期會使用調色板的全域使用方式，而且在使用調色板完成時，不應該釋放它。
-   使用 [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) 宏，指定與 MCIWnd 視窗相關聯之影片剪輯要使用的新調色板。
-   使用 [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) 宏，藉此實現與 MCIWnd 視窗相關聯的元件至系統元件。 此宏會使用與 [MCIWnd] 視窗相關聯的調色板來呼叫 [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) 函數。 如果您的應用程式訊息處理常式適用于 [**wm \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**Wm \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 只呼叫 **RealizePalette** 或 **MCIWndRealize**，則必須將這些訊息轉送到 MCIWnd，如果您未自行處理它們。

> [!Note]  
> 當有8位色彩深度的影片剪輯載入至 MCIWnd 視窗時，該剪輯隨附的調色板會取代與 [MCIWnd] 視窗相關聯的調色板。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[播放增強功能](playback-enhancements.md)
</dt> </dl>

 

 