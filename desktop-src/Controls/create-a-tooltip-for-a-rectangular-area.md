---
title: 如何建立矩形區域的工具提示
description: 下列範例示範如何建立視窗整個工作區的標準工具提示控制項。
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9be19be187e8c09b3aeb618e1c3518c7c15ca66816cbbb751abe43aa0b9172a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920690"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>如何建立矩形區域的工具提示

下列範例示範如何建立視窗整個工作區的標準工具提示控制項。

下圖顯示當滑鼠指標位於對話方塊的用戶端視窗內時，所顯示的工具提示。 對話方塊的控制碼已傳遞至上述範例中所示的函式。

![對話方塊的螢幕擷取畫面;滑鼠指標位於用戶端視窗內，並顯示工具提示](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

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

 

 




