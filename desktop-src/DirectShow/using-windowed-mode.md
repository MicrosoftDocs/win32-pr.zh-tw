---
description: 使用視窗模式
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: 使用視窗模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987665"
---
# <a name="using-windowed-mode"></a>使用視窗模式

> [!Note]  
> 舊版 [影片轉譯器篩選準則](video-renderer-filter.md) 一律使用視窗模式。 VMR-7 和 VMR-9 篩選器預設會使用視窗型模式，但也支援無視窗模式。

 

在視窗模式中，影片轉譯器會建立自己的視窗，以繪製影片畫面。 除非您另外指定，否則這個視窗會是具有自己的框線和標題列的最上層視窗。 不過大部分的時候，您會將影片視窗附加至應用程式視窗，讓影片整合到您的應用程式 UI 中。 此時，您需要進行下列步驟：

1.  **IVideoWindow** 的查詢。
2.  設定父視窗。
3.  設定新的視窗樣式。
4.  將影片視窗置於擁有者視窗內。
5.  通知 WM 移動訊息的影片視窗 \_ 。

**IVideoWindow 的查詢**

開始播放之前，請查詢 **IVideoWindow** 介面的篩選圖形管理員：


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**設定父視窗**

若要設定父視窗，請使用應用程式視窗的控制碼來呼叫 [**IVideoWindow：:p \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) 的使用者的擁有者方法。 這個方法會接受 [**OAHWND**](oahwnd.md)型別的變數，所以請將控制碼轉換成這個型別：


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**設定新的視窗樣式**

藉由呼叫 [**IVideoWindow：:p \_ system.windows.window.windowstyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) 方法來變更影片視窗的樣式：


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



WS \_ 子旗標會將視窗設定為子視窗，而 ws \_ CLIPSIBLINGS 旗標會防止視窗繪製在另一個子視窗的工作區中。

**放置影片視窗**

若要設定影片相對於應用程式視窗的工作區的位置，請呼叫 [**IVideoWindow：： SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) 方法。 這個方法會使用矩形來指定影片視窗的左邊緣、上邊緣、寬度和高度。 例如，下列程式碼會將影片視窗伸展，以符合父視窗的整個工作區：


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



若要取得影片的原生大小，請在篩選圖形管理員上呼叫 [**IBasicVideo：： GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) 方法。 您可以使用該資訊來調整影片，並保持正確的外觀比例。

**回應 WM \_ 移動訊息**

為了達到最佳效能，您應該在圖形暫停時，每次視窗移動時通知影片轉譯器。 呼叫 [**IVideoWindow：： NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) 方法以轉送 WM \_ 移動訊息：


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



如果轉譯器使用硬體重迭，此通知會導致轉譯器更新覆迭位置。  (VMR-9 不會使用覆迭，所以如果您使用 VMR-9，就不需要呼叫這個方法。 ) 

**清除**

在應用程式結束之前，停止圖形並將影片視窗的擁有者重設為 **Null**。 否則，可能會將視窗訊息傳送至錯誤的視窗，而這可能會造成錯誤。 此外，隱藏影片視窗，否則您可能會在螢幕上立即看到影片影像閃爍：


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> 如果影片視窗的父系是主應用程式視窗的子系 (換句話說，如果影片視窗是子) 的子系，您應該使用 **CoCreateInstance** 建立影片視窗並將它新增至圖形，而不是讓篩選圖形管理員在 [智慧型連接](intelligent-connect.md)期間新增影片轉譯器。 這可確保同時重新繪製影片視窗和子視窗。 否則，子視窗可能會在影片視窗中繪製。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片轉譯](video-rendering.md)
</dt> </dl>

 

 



