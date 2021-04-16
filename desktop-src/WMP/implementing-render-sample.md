---
title: 執行轉譯範例
description: 執行轉譯範例
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- 視覺效果、光暈範例
- 自訂視覺效果，發光範例
- 程式設計指南，視覺效果
- 範例，發光視覺效果
- 發光視覺效果範例
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函數，發光範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508276"
---
# <a name="implementing-render-sample"></a>執行轉譯範例

下列程式碼會用來執行轉譯 **函數：**


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



以下是程式碼的說明：

名為 *mycolor* 的變數會用於發光的色彩，並使用 **COLORREF** 來宣告。 所有色彩都應該使用 **COLORREF** 資料類型。

名為 *mylevel* 的變數會用於音訊波形層級快照集。 此值將取決於快照集當時的實際電源等級。

**Switch** 語句是由使用者在 Windows Media Player 上選擇的預設值所設定。 選擇會將 *mycolor* 設定為所需的色彩 (red、綠或 blue) 。 不過，確切的色彩會由音訊電源等級決定。 例如，如果選擇紅色的預設值，色彩會是紅色的紅色，但會根據快照集當時的音訊波形而變得較淺或較暗。 請務必使用 **RBG** 宏來建立您的色彩。

建立的筆刷稱為 *hNewBrush*，它是用來填滿 Windows Media Player 所提供的 *prc* 矩形。 繪圖介面是 Windows Media Player 所提供的 *hdc* 裝置內容。

**DeleteObject** 會刪除筆刷。 務必刪除您所建立的任何畫筆或筆刷。

轉譯程式 **代碼完成** 後，Windows Media Player 將會在所使用的面板所決定的視窗中顯示 *hdc* 圖形。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**發光範例**](the-glow-sample.md)
</dt> </dl>

 

 




