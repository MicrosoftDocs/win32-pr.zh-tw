---
title: 如何執行氣球工具提示
description: 氣球工具提示類似于標準工具提示，但會顯示在卡通樣式 \ 0034; balloon \ 0034;以指向工具的主幹。
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671979"
---
# <a name="how-to-implement-balloon-tooltips"></a>如何執行氣球工具提示

氣球工具提示類似于標準工具提示，但會顯示在卡通樣式的「球標」中，並以主幹指向工具。 氣球工具提示可以是單行或多行。 它們的建立和處理方式與標準工具提示的方式大致相同。

下圖顯示詞幹和矩形的預設位置。 如果工具太接近畫面頂端，工具提示會出現在工具矩形的下方和右邊。 如果工具太接近畫面右側，則適用類似的原則，但工具提示會出現在工具矩形的左邊。

![對話方塊的螢幕擷取畫面;具有一行文字的氣球工具提示會出現在目標的上方和右邊](images/tt-balloon.png)

您可以藉由在工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定 **TTF \_ CENTERTIP** 旗標，來變更預設位置。 在這種情況下，詞幹通常會指向工具矩形的下邊緣中央，而文字矩形則會直接顯示在工具的正下方。 此詞幹會附加至上方邊緣的文字矩形。 如果工具太接近畫面底部，則文字矩形的中心會在工具的上方，而莖會附加至下邊緣的中央。

下圖顯示以工具為中心的工具提示。

![對話方塊的螢幕擷取畫面;具有一行文字的氣球工具提示會出現在目標底下的中央](images/tt-ballooncenter.png)

如果您想要指定莖的位置，請在工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定 **TTF \_ TRACK** 旗標。 然後，您可以使用 *lParam* 值中的 x 和 y 座標來傳送 [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)訊息，以指定座標。 如果同時設定了 **TTF \_ CENTERTIP** ，則詞幹仍會指向 **TTM \_ TRACKPOSITION** 訊息所指定的位置。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="implement-balloon-tooltips"></a>執行氣球工具提示

下列範例程式碼示範如何使用 **TTS \_ 氣球** 工具提示控制項樣式來執行置中的氣球工具提示。


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> <dt>

[**工具提示樣式**](tooltip-styles.md)
</dt> </dl>

 

 




