---
title: 改善 Single-Finger 的移動體驗
description: 如果您建立以 Windows Touch 為目標的應用程式，它會自動提供基本的移動流覽支援。 不過，您可以使用 WM \_ 手勢訊息來為單一手指移動提供增強的支援。
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Touch 的單指移動
- Windows Touch，移動流覽
- Windows Touch、捲軸
- Windows Touch，筆觸
- Windows Touch，軌跡平移訊息
- Windows Touch，界限意見反應
- 單一手指移動
- 單向移動
- 移動流覽、界限意見反應
- 捲軸、單鍵移動
- 筆觸，單一手指移動
- 捲軸，停用
- 筆觸，停用
- 手勢，軌跡平移訊息
- 移動流覽、軌跡平移訊息
- 界限意見反應，單一手指移動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682537"
---
# <a name="improving-the-single-finger-panning-experience"></a>改善 Single-Finger 的移動體驗

如果您建立以 Windows Touch 為目標的應用程式，它會自動提供基本的移動流覽支援。 不過，您可以使用 [**WM \_ 手勢**](wm-gesture.md) 訊息來為單一手指移動提供增強的支援。

## <a name="overview"></a>概觀

若要改善單指的移動體驗，請使用下列步驟，如本主題的後續章節所述：

-   建立具有捲軸的應用程式，並停用筆觸。
-   新增對軌跡平移訊息的支援。
-   啟用彈跳。

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>建立具有捲軸的應用程式並停用筆觸

開始之前，您必須建立具有捲軸的應用程式。 [使用捲軸來移動流覽的舊版支援](legacy-support-for-panning-with-scrollbars.md)會說明此流程。 如果您想要從範例內容開始，請移至該區段，並建立具有捲軸的應用程式，然後停用筆觸。 如果您已經有具有正常運作捲軸的應用程式，請停用筆觸，如該章節所述。

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>新增軌跡平移訊息的自訂移動流覽支援

若要支援軌跡平移訊息，您必須在 **WndProc** 方法中處理這些訊息。 手勢訊息是用來判斷移動流覽訊息的水準和垂直差異。 差異是用來更新捲軸物件，此物件會更新使用者介面。

首先，更新 targetver.h .h 檔案中的 Windows 版本設定，以啟用 Windows Touch。 下列程式碼顯示各種 Windows 版本設定，這些設定應該取代 targetver.h 中的設定。


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



接下來，將 UXTheme 檔案新增至您的專案，並將 UXTheme 程式庫新增至專案的其他相依性。


```C++
#include <uxtheme.h>
```



接下來，將下列變數新增至 **WndProc** 函式的頂端。 這些將用於移動用的計算。


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



接下來，新增 [**WM \_ 手勢**](wm-gesture.md) 訊息的處理常式，以便根據移動流覽手勢以差異更新捲軸。 這可讓您更精細地控制移動。

下列程式碼會從 *lParam* 取得 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)結構、儲存結構的最後一個 y 座標，以及決定要更新捲軸物件的位置變更。 下列程式碼應該放在您的 **WndProc** switch 語句中。


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



現在，當您在視窗上執行平移手勢時，您會看到具有慣性的文字捲軸。 至此，您可能會想要將文字變更為具有更多行，讓您可以探索移動大型文字區段的位置。

## <a name="boundary-feedback-in-wndproc"></a>WndProc 中的界限意見反應

界限意見反應是在使用者到達 pannable 區域結尾時提供給使用者的一種視覺效果意見反應。 當到達界限時，應用程式會觸發此程式。 在先前的 [**wm \_ 手勢**](wm-gesture.md) 訊息範例中， `(si.nPos == si.yPos)` 會使用來自 **wm \_ 手勢** 案例的結束條件來測試您已達到 pannable 區域的結尾。 下列變數用來追蹤值和測試錯誤。


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



平移手勢案例會更新以觸發界限意見反應。 下列程式碼說明來自 [**WM \_ 手勢**](wm-gesture.md)訊息處理常式的 **GID \_ 平移** 案例。


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



現在，當使用者移動超過捲軸區域底部時，您的應用程式視窗應該會有界限的意見反應。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Touch 手勢](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 