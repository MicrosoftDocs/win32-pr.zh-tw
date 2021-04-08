---
title: 'Windows Touch 手勢範例 (MTGestures) '
description: 本節說明 Windows Touch 手勢範例。
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch，程式碼範例
- Windows Touch，範例程式碼
- Windows Touch，手勢
- Windows Touch、手勢範例
- 手勢範例
- 手勢，範例程式碼
- 手勢，程式碼範例
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681395"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Touch 手勢範例 (MTGestures) 

本節說明 Windows Touch 手勢範例。

Windows Touch 手勢範例示範如何使用筆勢訊息來轉譯、旋轉和調整由圖形裝置介面 (GDI) 轉譯的方塊，方法是處理 [**WM_GESTURE**](wm-gesture.md) 訊息。 下列螢幕擷取畫面顯示範例在執行時的外觀。

![螢幕擷取畫面，顯示正在執行的 windows 觸控手勢範例，並在螢幕上使用旋轉的黑色空心矩形](images/mtgestures.png)

在此範例中，會將手勢訊息傳遞至手勢引擎，然後呼叫繪圖物件上的方法，以轉譯、旋轉和縮放具有處理這些命令之方法的物件。 若要協助示範範例的運作方式，請考慮使用兩個點一下命令來啟用或停用轉譯方塊中的對角線線的步驟。 使用者執行雙向點一下手勢，以產生程式所處理的訊息。 當處理訊息時，它會切換布林值，以便在繪圖物件上轉譯對角線，然後物件將會轉譯對角線線。

下列程式碼示範如何從 WndProc 方法將手勢訊息傳遞至手勢引擎。

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

下列程式碼顯示手勢引擎如何處理雙向的點一下命令。

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

下列程式碼顯示繪圖物件如何切換對角線。

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

下列程式碼顯示物件如何在其 draw 方法中轉譯對角線線。

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a>相關主題

[多點觸控手勢應用程式 (c # ) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)、 [多點觸控手勢應用程式 (c + +) ](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp)、 [Windows Touch 範例](windows-touch-samples.md)
