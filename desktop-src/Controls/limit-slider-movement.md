---
title: 如何限制滑杆移動
description: 如關於敘述區控制項中所述，您可以將部分的部分部分的資料格範圍設定為選取範圍。 選取範圍的其中一個用途，就是限制滑杆的移動，讓部分的完整範圍超出限制。
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839591"
---
# <a name="how-to-limit-slider-movement"></a>如何限制滑杆移動

如關於敘述區 [控制項](trackbar-controls.md)中所述，您可以將部分的部分部分的資料格範圍設定為選取範圍。 選取範圍的其中一個用途，就是限制滑杆的移動，讓部分的完整範圍超出限制。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="limit-slider-movement"></a>限制滑杆移動

下列範例程式碼會在移動滑杆的位置超出選取範圍時，重設滑杆的位置，藉此限制滑杆的移動。


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>備註

此程式碼片段會是對話方塊視窗程式的一部分。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 [使用] 控制項](using-trackbar-controls.md)
</dt> </dl>

 

 




