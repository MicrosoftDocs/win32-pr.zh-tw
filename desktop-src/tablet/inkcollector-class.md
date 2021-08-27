---
description: 表示用來從可用的平板電腦裝置捕獲筆墨的物件。
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: 'InkCollector 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718174"
---
# <a name="inkcollector-class"></a>InkCollector 類別

表示用來從可用的平板電腦裝置捕獲筆墨的物件。

在透明控制項背後建立 **InkCollector** 控制項 (例如，加上 **WS \_ EX \_ 透明** 屬性集) 的分組會導致 **InkCollector** 無法收集筆跡。

**InkCollector** 具有下列類型的成員：

-   [事件](#events)
-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**InkCollector** 類別具有這些事件。



| 事件                                                     | 描述                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | 當 **InkCollector** 偵測到已關閉的資料指標按鈕時發生。<br/>                                                                                                                                                                             |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | 當 **InkCollector** 偵測到已啟動的資料指標按鈕時發生。<br/>                                                                                                                                                                               |
| [**CursorDown**](inkcollector-cursordown.md)             | 當游標提示接觸到數位化的 tablet 介面時發生。<br/>                                                                                                                                                                                 |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | 當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。<br/>                                                                                                                                                        |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | 當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時發生。<br/>                                                                                                                                                      |
| [**按兩下**](inkcollector-doubleclick.md)           | 當按兩下 **InkCollector** 物件時發生。<br/>                                                                                                                                                                                         |
| [**手勢**](inkcollector-gesture.md)                   | 在識別應用程式特定的手勢時發生。<br/>                                                                                                                                                                                         |
| [**MouseDown**](inkcollector-mousedown.md)               | 發生于滑鼠指標位於 **InkCollector** 物件上方且按下滑鼠按鍵時。<br/>                                                                                                                                                   |
| [**MouseMove**](inkcollector-mousemove.md)               | 發生于滑鼠指標移至 **InkCollector** 物件上方時。<br/>                                                                                                                                                                           |
| [**MouseUp**](inkcollector-mouseup.md)                   | 發生于滑鼠指標位於 **InkCollector** 物件上方且放開滑鼠按鍵時。<br/>                                                                                                                                                  |
| [**滑鼠滾輪**](inkcollector-mousewheel.md)             | 發生于 **InkCollector** 物件具有焦點時，滑鼠滾輪移動時。<br/>                                                                                                                                                                     |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | 發生于出現無線封包時，當使用者將畫筆移近 tablet，而游標位於 **InkCollector** 物件的視窗內，或使用者在 **InkCollector** 物件物件的相關視窗內移動滑鼠時，就會發生這種情況。<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | 當 **InkCollector** 物件接收封包時發生。<br/>                                                                                                                                                                                          |
| [**中風**](inkcollector-stroke.md)                     | 當使用者在任何平板電腦上完成繪製新筆劃時發生。<br/>                                                                                                                                                                                  |
| [**SystemGesture**](inkcollector-systemgesture.md)       | 在辨識系統手勢時發生。<br/>                                                                                                                                                                                                        |
| [**TabletAdded**](inkcollector-tabletadded.md)           | 當 [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 新增至系統時發生。<br/>                                                                                                                                                                                 |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | 從系統移除 [**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 電腦時發生。<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>介面

**InkCollector** 類別會定義這些介面。



| 介面         | 描述                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkCollector** | 這個物件會實 **IInkCollector** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkCollector** 類別有這些方法。



| 方法                                                                              | 描述                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | 抓取特定 **InkCollector** 物件事件的目前狀態，也就是是否正在聆聽或使用事件。<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | 抓取 **InkCollector** 物件是否對特定手勢感興趣。<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | 抓取用來繪製筆墨的視窗矩形（以圖元為單位）。<br/>                                                                               |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | 此模式可讓 **InkCollector** 物件從任何連接到 tablet PC 的平板電腦收集筆跡。<br/>                                              |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | 修改值，這個值會指出是否應聆聽或使用特定事件。<br/>                                                            |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | 修改已知手勢中 **InkCollector** 物件的感興趣。<br/>                                                                            |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | 此模式可讓 **InkCollector** 物件只從一個平板電腦收集筆跡。 **InkCollector** 物件會忽略其他平板電腦的筆墨。<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | 修改視窗矩形（以圖元為單位），用來將繪製的筆墨對應至視窗。<br/>                                                                    |



 

### <a name="properties"></a>屬性

**InkCollector** 類別具有這些屬性。



| 屬性                                                                             | 存取類型          | Description                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | 唯讀<br/> | 取得或設定值，這個值會指定當視窗無效時， **InkCollector** 是否會重新繪製筆墨。<br/>                                                                 |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | 唯讀<br/> | 取得值，這個值會指定是否目前正在 **InkCollector** 物件上繪製筆墨。<br/>                                                                                   |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | 唯讀<br/> | 取得或設定收集模式，這個模式會決定是否將筆墨、手勢或兩者辨識為使用者寫入。<br/>                                                                |
| [**資料指標**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | 唯讀<br/> | 取得可在筆跡區域中使用的資料 [**指標**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) 集合。<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | 唯讀<br/> | 取得或設定預設的 [**InkDrawingAttributes**](inkdrawingattributes-class.md) 物件，這個物件會指定繪製和顯示筆墨時使用的繪製屬性。<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | 唯讀<br/> | 取得或設定與 **InkCollector** 物件上繪製之筆跡相關聯的封包方面感興趣。<br/>                                                                          |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | 唯讀<br/> | 取得或設定值，這個值會指出是否在繪製時呈現筆墨。<br/>                                                                                                       |
| [**啟用**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | 唯讀<br/> | 取得或設定值，這個值會指定 **InkCollector** 物件是否會收集畫筆輸入。<br/>                                                                                       |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | 唯讀<br/> | 取得或設定要附加 **InkCollector** 物件的視窗控制碼。<br/>                                                                                           |
| [**筆跡**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | 唯讀<br/> | 取得或設定與 **InkCollector** 物件相關聯的 [**InkDisp**](inkdisp-class.md)物件。<br/>                                                                     |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | 唯讀<br/> | 取得或設定沿著 X 軸的邊界（以圖元為單位）。<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | 唯讀<br/> | 取得或設定沿著 y 軸的邊界（以圖元為單位）。<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | 唯讀<br/> | 取得或設定目前的自訂滑鼠圖示。<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | 唯讀<br/> | 取得或設定值，這個值表示當滑鼠停留在物件的特定部分時，所顯示的滑鼠指標類型。<br/>                                                |
| [**轉譯器**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | 唯讀<br/> | 取得或設定用來繪製筆墨的 [**InkRenderer**](inkrenderer-class.md) 物件。<br/>                                                                                        |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | 唯讀<br/> | 取得或設定值，這個值會指定當系統處於高對比模式時，是否只將筆墨轉譯為一種色彩。<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | 唯讀<br/> | 取得 **InkCollector** 物件目前用來收集輸入的平板電腦裝置。<br/>                                                                                      |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

**InkCollector** 物件只會收集在與其相關聯之特定視窗中輸入的筆墨和手勢。 **InkCollector** 的唯一目的是從硬體收集筆墨 (例如，透過 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)和 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)物件) ，然後將其傳遞至應用程式。 它基本上是做為將筆墨分配至一或多個不同 [**InkDisp**](inkdisp-class.md) 物件的來源，而這些物件會作為保存分散式筆墨的容器。

若要使用 **InkCollector**，您可以建立它，告訴它要收集繪製筆墨的視窗，然後加以啟用。 啟用之後，就可以將它設定為只收集三種模式的其中一種 (模式是在 [**InkCollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) 列舉) 中指定：

-   InkOnly，在其中建立 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件。
-   GestureOnly，在其中建立 [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) 物件。
-   InkAndGesture，其中會根據應用程式處理事件的方式，來建立筆觸、手勢或可能兩者。

這表示，對於位於平板電腦範圍內的每個資料指標的移動， **InkCollector** 一律會收集筆劃或手勢，有時兩者都是。 使用 Microsoft 手勢辨識器內建手勢支援。

**InkCollector** 會處理所有的平板電腦輸入。 您可以從所有連結的平板電腦收集筆跡 (包括) 同時進行。 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)和 [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)物件中的變更可能會導致 **InkCollector** 物件引發事件。

**InkCollector** 也會管理它在存在期間遇到的資料指標清單。 當 **InkCollector** 遇到新的資料指標時，就會引發 [**CursorInRange**](inkcollector-cursorinrange.md) 事件，並將 *newCursor* 參數設定為 **VARIANT \_ TRUE**。 應用程式會使用 **InkCollector** 來管理新的資料指標。

一個以上的 **InkCollector** 可以與特定的視窗控制碼相關聯，即使它們的集合區域（在函式中設定或使用 [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) 方法）也會重迭。 不過，此案例的唯一運作方式，是每個 **InkCollector** 都會呼叫 [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) 並使用唯一的平板電腦。 此行為可讓您輕鬆地將筆墨儲存在每個平板電腦的個別物件中。

如果一個啟用的 **InkCollectors** (設定為 [**已**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) 啟用的屬性) 與另一個已啟用之 **InkCollector** 的視窗輸入矩形重迭，就會發生錯誤。

> [!Note]  
> 只要在任何已知時間啟用了其中一個輸入矩形，就可能會發生重迭，而不會發生錯誤。

 

[**MouseDown**](inkcollector-mousedown.md)、 [**MouseMove**](inkcollector-mousemove.md)、 [**MouseUp**](inkcollector-mouseup.md)和 [**滑鼠滾輪**](inkcollector-mousewheel.md)事件會傳回 x 和 y 座標（以圖元為單位），而非與筆墨空間相關聯的 HIMETRIC 單位。 這是因為這些事件會取代不知道應用程式的滑鼠事件，而這些應用程式只會瞭解圖元。

> [!Note]  
> **InkCollector** 物件無法在非 UI 執行緒上安全地釋放。

 

若要改善應用程式的效能，請在不再需要時處置您的 **InkCollector** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkEdit 控制項參考](inkedit-control-reference.md)
</dt> <dt>

[**InkDisp 類別**](inkdisp-class.md)
</dt> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> <dt>

[InkPicture 控制項參考](inkpicture-control-reference.md)
</dt> </dl>

 

