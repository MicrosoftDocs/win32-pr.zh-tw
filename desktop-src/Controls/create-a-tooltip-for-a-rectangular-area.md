---
title: 如何建立矩形區域的工具提示
description: 下列範例示範如何建立視窗整個工作區的標準工具提示控制項。
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671968"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>如何建立矩形區域的工具提示

下列範例示範如何建立視窗整個工作區的標準工具提示控制項。

下圖顯示當滑鼠指標位於對話方塊的用戶端視窗內時，所顯示的工具提示。 對話方塊的控制碼已傳遞至上述範例中所示的函式。

![對話方塊的螢幕擷取畫面;滑鼠指標位於用戶端視窗內，並顯示工具提示](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="create-a-tooltip-for-a-rectangular-area"></a>建立矩形區域的工具提示

下列範例示範如何建立視窗整個工作區的標準工具提示控制項。


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

 




