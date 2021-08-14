---
title: 如何控制 AVI 剪輯
description: 本主題將示範如何使用動畫控制項宏來播放、停止及關閉相關聯的 Audio-Video 交錯 (AVI) 剪輯。
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbabd3ea6e0694448e4bd8c01e53161333b2df3904cf1578252bdbe150d3d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170759"
---
# <a name="how-to-control-the-avi-clip"></a>如何控制 AVI 剪輯

本主題將示範如何使用動畫控制項宏來播放、停止及關閉相關聯的 Audio-Video 交錯 (AVI) 剪輯。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計
-   AVI 檔案

## <a name="instructions"></a>指示


建立函式，此函式會將動畫控制項的控制碼作為參數，並使用旗標來指出要在相關聯的 AVI 剪輯上執行的動作。

下列 c + + 範例中的函式會呼叫三個動畫控制項宏的其中一個 ([**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)、[**動畫 \_ 停止**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)、根據 *nAction* 參數的值來建立 [**\_ 關閉**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) 的動畫。 與 AVI 剪輯相關聯之動畫控制項的控制碼，會透過 *hwndAnim* 參數傳遞。


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於動畫控制項](animation-control-overview.md)
</dt> <dt>

[動畫控制項參考](bumper-animation-animation-control-reference.md)
</dt> <dt>

[使用動畫控制項](using-animation-control.md)
</dt> <dt>

[動畫控制項](animation-control-reference.md)
</dt> </dl>

 

 




