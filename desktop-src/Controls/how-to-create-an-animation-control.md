---
title: 如何建立動畫控制項
description: 本主題將示範如何建立動畫控制項。
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8117d7c9393a828786532bd3d3fbfcf4f4eaaf6bb1bfdccdc5a2f97fa1c5cb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435818"
---
# <a name="how-to-create-an-animation-control"></a>如何建立動畫控制項

本主題將示範如何建立動畫控制項。 隨附的 c + + 程式碼範例會在對話方塊中建立動畫控制項。 它會將動畫控制項放在指定的控制項底下，並根據 Audio-Video 交錯 (AVI) 剪輯中的框架維度來設定動畫控制項的尺寸。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>先決條件

-   C/C++
-   Windows消費者介面程式設計
-   AVI 檔案

## <a name="instructions"></a>指示

### <a name="step-1-create-an-instance-of-the-animation-control"></a>步驟1：建立動畫控制項的實例。

使用「 [**\_ 建立**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 動畫」宏建立動畫控制項的實例。


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>步驟2：放置動畫控制項。

取得指定控制項按鈕的螢幕座標。


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



將左下角的座標轉換為工作區座標。


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



將動畫控制項放在指定的控制項按鈕下方。


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>步驟3：開啟 AVI 剪輯。

呼叫 [**動畫 \_ 開啟**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) 宏以開啟 AVI 剪輯，並顯示動畫控制項中的第一個畫面格。 呼叫 **ShowWindow** 函式，讓動畫控制項可見。


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>完整範例


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於動畫控制項](animation-control-overview.md)
</dt> <dt>

[動畫控制項參考](bumper-animation-animation-control-reference.md)
</dt> <dt>

[使用動畫控制項](using-animation-control.md)
</dt> <dt>

[動畫](animation-control-reference.md)
</dt> </dl>

 

 




