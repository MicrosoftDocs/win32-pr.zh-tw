---
title: 如何執行多行工具提示
description: 多行工具提示允許文字顯示在一行以上。
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671975"
---
# <a name="how-to-implement-multiline-tooltips"></a>如何執行多行工具提示

多行工具提示允許文字顯示在一行以上。

[版本 4.70](common-control-versions.md)和更新版本的通用控制項都支援它們。 您的應用程式會藉由傳送 [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) 訊息（指定顯示矩形的寬度）來建立多行工具提示。 超過此寬度的文字會換行至下一行，而不是擴展顯示區域。 視需要增加矩形高度以容納額外的行。 工具提示控制項會自動包裝行，或者您可以使用換行字元組合（ \\ r \\ n）來強制在特定位置換行。

結果顯示如下圖所示。

![具有工具提示之對話方塊的螢幕擷取畫面，其中包含的文字相片順序類似多行段落](images/tt-multiline.png)

> [!Note]  
> [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的 **szText** 成員所指定的文字緩衝區只能容納80個字元。 如果您需要使用較長的字串，請將 **NMTTDISPINFO** 的 **lpszText** 成員指向包含所需文字的緩衝區。

 

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="implement-multiline-tooltips"></a>執行多行工具提示

下列程式碼片段是簡單 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知處理常式的範例。 它會將顯示矩形設定為150圖元，以啟用多行工具提示。 第一個單字後面會插入一個手動分行符號，以顯示分行符號可能很難和軟。


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

 




