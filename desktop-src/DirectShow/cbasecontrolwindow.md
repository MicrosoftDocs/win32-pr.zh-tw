---
description: CBaseControlWindow 類別會執行 IVideoWindow 介面，並控制其相關聯篩選的外部存取。
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: CBaseControlWindow 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow
api_type:
- COM
api_location: ''
ms.openlocfilehash: c4b53cc5ce1b209cc7de9d68648b68096e5c4911
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187516"
---
# <a name="cbasecontrolwindow-class"></a>CBaseControlWindow 類別

![cbasecontrolwindow 類別階層](images/wctrl01.png)

**CBaseControlWindow** 類別會執行 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)介面，並控制其相關聯篩選的外部存取。 您必須將 **CBaseControlWindow** 物件的指標傳遞至重要區段同步處理物件的指標，以將其與篩選同步處理。 **CBaseControlWindow** 類別提供一些方法，這些方法會傳回屬性設定，而不需要處理此重要區段。 例如，呼叫 [**CBaseControlWindow：： get 會 \_**](cbasecontrolwindow-get-autoshow.md) 自動執行，以取得 **m \_ bAutoShow** 資料成員的值，以鎖定重要區段。 但是，篩選可能已經有鎖定的內部關鍵區段，這可能會違反篩選的鎖定階層。 相反地，呼叫 [**CBaseControlWindow：： IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) 成員函式會傳回所需的值，而不會影響重要區段。

所有 **CBaseControlWindow** 實 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 方法都需要使用其上游篩選正確連接篩選。 基於這個理由，類別物件需要同步處理 pin，您可以呼叫 [**CBaseControlWindow：： SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md) 方法來設定它。 每當您呼叫 **IVideoWindow** 方法時， **CBaseControlWindow** 物件都會檢查釘選是否仍在連線。



| 受保護的資料成員                                                     | Description                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | 當狀態變更時的結果。                                                                                                              |
| m \_ bCursorHidden                                                           | 判斷資料指標是否顯示或隱藏。                                                                                 |
| m \_ BorderColour                                                            | 目前視窗框線的色彩。                                                                                                         |
| m \_ hwndDrain                                                               | 張貼所接收之訊息的視窗控制碼。                                                                                        |
| m \_ hwndOwner                                                               | 擁有視窗。                                                                                                                              |
| m \_ pFilter                                                                 | 擁有媒體篩選器的指標。                                                                                                         |
| m \_ pInterfaceLock                                                          | 外部定義的重要區段。                                                                                                        |
| m \_ pPin                                                                    | 控制連接的媒體類型。                                                                                                  |
| 成員函數                                                           | Description                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | 結構 **CBaseControlWindow** 物件。                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | 抓取一般或延伸的視窗樣式。                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | 設定一般或延伸的視窗樣式。                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | 抓取目前的框線色彩。 這是 helper 成員函式。                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | 抓取擁有視窗。 這是 helper 成員函式。                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | 抓取當轉譯篩選暫停或執行時，是否會自動顯示影片視窗的相關資訊。                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | 抓取 **m \_ bCursorHidden** 資料成員的目前狀態，而不鎖定重要區段。 這是 helper 成員函式。 |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | 將訊息散發至父視窗。                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | 通知物件所套用的 pin。                                                                                         |
| IVideoWindow 方法                                                       | Description                                                                                                                                 |
| [**取得 \_ 自動完成**](cbasecontrolwindow-get-autoshow.md)                   | 抓取目前的自動按旗標設定。                                                                                                |
| [**取得 \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | 抓取背景旗標中的已實現調色板。                                                                                      |
| [**取得 \_ 邊框**](cbasecontrolwindow-get-bordercolor.md)             | 抓取目前的框線色彩。                                                                                                         |
| [**取得 \_ 標題**](cbasecontrolwindow-get-caption.md)                     | 抓取目前的視窗標題。                                                                                                       |
| [**取得 \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | 抓取目前全螢幕模式。                                                                                                     |
| [**取得 \_ 高度**](cbasecontrolwindow-get-height.md)                       | 抓取目前的視窗高度。                                                                                                        |
| [**取得 \_ 左方**](cbasecontrolwindow-get-left.md)                           | 抓取目前的左視窗座標。                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | 抓取理想影像的大小上限。                                                                                              |
| [**取得 \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | 抓取目前的訊息清空。                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | 抓取理想影像的大小下限。                                                                                              |
| [**取得 \_ 擁有者**](cbasecontrolwindow-get-owner.md)                         | 抓取父視窗控制碼。                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | 抓取視窗將在最大化或最小化時還原的位置。                                                    |
| [**取得 \_ 最上層**](cbasecontrolwindow-get-top.md)                             | 抓取視窗頂端的 y 座標。                                                                                       |
| [**取得 \_ 可見**](cbasecontrolwindow-get-visible.md)                     | 抓取視窗目前的可見度設定。                                                                                     |
| [**取得 \_ 寬度**](cbasecontrolwindow-get-width.md)                         | 抓取視窗的寬度。                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | 抓取目前的視窗座標。                                                                                                   |
| [**取得 \_ system.windows.window.windowstate**](cbasecontrolwindow-get-windowstate.md)             | 抓取視窗的目前狀態。                                                                                                  |
| [**取得 \_ system.windows.window.windowstyle**](cbasecontrolwindow-get-windowstyle.md)             | 抓取標準視窗樣式。                                                                                                       |
| [**取得 \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | 抓取擴充的視窗樣式。                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | 隱藏或顯示資料指標。                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | 抓取 **m \_ bCursorHidden** 資料成員的目前狀態。                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | 傳遞傳送給擁有視窗的訊息。                                                                                         |
| [**put \_ 自動放置**](cbasecontrolwindow-put-autoshow.md)                   | 設定自動後的屬性。                                                                                                                 |
| [**put \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | 設定旗標，以在背景中實現調色板。                                                                                       |
| [**put \_ 邊框存放**](cbasecontrolwindow-put-bordercolor.md)             | 設定目前的框線色彩。                                                                                                              |
| [**put \_ 標題**](cbasecontrolwindow-put-caption.md)                     | 設定目前的視窗標題。                                                                                                            |
| [**put \_ FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | 設定全螢幕模式。                                                                                                                  |
| [**put \_ Height**](cbasecontrolwindow-put-height.md)                       | 設定目前的視窗高度。                                                                                                             |
| [**放在 \_ 左方**](cbasecontrolwindow-put-left.md)                           | 設定視窗的左座標。                                                                                                    |
| [**put \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | 設定 [消息清空] 視窗。                                                                                                              |
| [**put \_ 擁有者**](cbasecontrolwindow-put-owner.md)                         | 設定 Microsoft Win32 父視窗控制碼。                                                                                              |
| [**放在 \_ 頂端**](cbasecontrolwindow-put-top.md)                             | 設定視窗頂端的位置。                                                                                                |
| [**put \_ Visible**](cbasecontrolwindow-put-visible.md)                     | 隱藏或顯示視窗。                                                                                                                  |
| [**put \_ 寬度**](cbasecontrolwindow-put-width.md)                         | 設定視窗的寬度。                                                                                                               |
| [**put \_ system.windows.window.windowstate**](cbasecontrolwindow-put-windowstate.md)             | 設定視窗的狀態。                                                                                                               |
| [**put \_ system.windows.window.windowstyle**](cbasecontrolwindow-put-windowstyle.md)             | 設定標準視窗樣式。                                                                                                            |
| [**put \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | 設定延伸視窗樣式。                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | 在前景中設定視窗。                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | 設定視窗的位置。                                                                                                                   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 基類](directshow-base-classes.md)
</dt> </dl>

 

 



