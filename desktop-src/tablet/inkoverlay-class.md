---
description: 表示物件，這個物件適用于注釋案例，其中使用者不在意筆墨的執行辨識，而是對筆墨的大小、形狀、色彩和位置感興趣。
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: 'InkOverlay 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d1a818c1fef9006abad2dd31da5a41f43aeb3df9a9b75d348d8987938abfcea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967117"
---
# <a name="inkoverlay-class"></a>InkOverlay 類別

表示物件，這個物件適用于注釋案例，其中使用者不在意筆墨的執行辨識，而是對筆墨的大小、形狀、色彩和位置感興趣。

在透明控制項背後建立 **InkOverlay** 控制項 (例如，具有 WS \_ EX \_ 透明屬性集的群組方塊) 將會防止 **InkOverlay** 收集筆跡。

**InkOverlay** 有下列類型的成員：

-   [事件](#events)
-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**InkOverlay** 類別具有這些事件。



| 事件                                                     | 描述                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkcollector-cursorbuttondown.md) | 當 **InkOverlay** 偵測到已關閉的資料指標按鈕時發生。<br/>                                                                                                                                                                           |
| [**CursorButtonUp**](inkcollector-cursorbuttonup.md)     | 當 **InkOverlay** 偵測到已啟動的資料指標按鈕時發生。<br/>                                                                                                                                                                             |
| [**CursorDown**](inkcollector-cursordown.md)             | 當游標提示接觸到數位化的 tablet 介面時發生。<br/>                                                                                                                                                                             |
| [**CursorInRange**](inkcollector-cursorinrange.md)       | 當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。<br/>                                                                                                                                                    |
| [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) | 當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時發生。<br/>                                                                                                                                                  |
| [**按兩下**](inkcollector-doubleclick.md)           | 發生于按兩下 **InkOverlay** 物件時。<br/>                                                                                                                                                                                       |
| [**手勢**](inkcollector-gesture.md)                   | 在識別應用程式特定的手勢時發生。<br/>                                                                                                                                                                                     |
| [**MouseDown**](inkcollector-mousedown.md)               | 發生于滑鼠指標位於 **InkOverlay** 物件上方，且按下滑鼠按鍵時。<br/>                                                                                                                                                 |
| [**MouseMove**](inkcollector-mousemove.md)               | 發生于滑鼠指標移到 **InkOverlay** 物件上方時。<br/>                                                                                                                                                                         |
| [**MouseUp**](inkcollector-mouseup.md)                   | 發生于滑鼠指標位於 **InkOverlay** 物件上並放開滑鼠按鍵時。<br/>                                                                                                                                                |
| [**滑鼠滾輪**](inkcollector-mousewheel.md)             | 發生于當 **InkOverlay** 物件具有焦點時，滑鼠滾輪移動時。<br/>                                                                                                                                                                   |
| [**NewInAirPackets**](inkcollector-newinairpackets.md)   | 發生于出現無線封包時，當使用者將畫筆移近平板電腦，且游標位於 **inkoverlay** 物件的視窗內，或使用者在 **inkoverlay** 物件物件的相關聯視窗內移動滑鼠時，就會發生這種情況。<br/> |
| [**NewPackets**](inkcollector-newpackets.md)             | 當 **InkOverlay** 物件接收封包時發生。<br/>                                                                                                                                                                                        |
| [**畫**](inkoverlay-painted.md)                     | 當 **InkOverlay** 物件已完成重繪本身時發生。<br/>                                                                                                                                                                          |
| [**繪畫**](inkoverlay-painting.md)                   | 發生于 **InkOverlay** 物件自行重新繪製之前。<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | 發生于控制項內的筆墨選取變更時（例如，透過對使用者介面的變化、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。<br/>                                       |
| [**SelectionChanging**](inkoverlay-selectionchanging.md) | 發生于控制項內的筆墨選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式，或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。<br/>                                |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)       | 發生于目前選取範圍的位置變更時，例如透過對使用者介面的改變、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。<br/>                                         |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)     | 當目前選取範圍的位置即將變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性。<br/>                                  |
| [**SelectionResized**](inkoverlay-selectionresized.md)   | 發生于目前的選取範圍變更時（例如，透過對使用者介面的改變、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。<br/>                                             |
| [**SelectionResizing**](inkoverlay-selectionresizing.md) | 發生于目前的選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。<br/>                                      |
| [**中風**](inkcollector-stroke.md)                     | 當使用者在任何平板電腦上完成繪製新筆劃時發生。<br/>                                                                                                                                                                              |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)       | 從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) 屬性刪除筆劃之後發生。<br/>                                                                                                                                                      |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)     | 發生于從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) 屬性刪除筆劃之前。<br/>                                                                                                                                                           |
| [**SystemGesture**](inkcollector-systemgesture.md)       | 在辨識系統手勢時發生。<br/>                                                                                                                                                                                                    |
| [**TabletAdded**](inkcollector-tabletadded.md)           | [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)新增至系統時發生。<br/>                                                                                                                                                                        |
| [**TabletRemoved**](inkcollector-tabletremoved.md)       | 從系統移除 [**平板**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 電腦時發生。<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>介面

**InkOverlay** 類別會定義這些介面。



| 介面       | 描述                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkOverlay** | 這個物件會實 **IInkOverlay** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkOverlay** 類別具有這些方法。



| 方法                                                                              | 描述                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | 設定用來重繪 **InkOverlay** 物件內筆墨的矩形。<br/>                                                                   |
| [**GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | 傳回特定 **InkOverlay** 物件事件的目前狀態，也就是是否正在聆聽或使用事件。<br/>                |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | 傳回 **InkOverlay** 物件是否對特定手勢感興趣。<br/>                                                                |
| [**GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | 抓取用來繪製筆墨的視窗矩形（以圖元為單位）。<br/>                                                                           |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | 判中斷點擊測試期間，選取的部分。<br/>                                                                             |
| [**SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | 此模式可讓 **InkOverlay** 物件從任何連接到 tablet PC 的平板電腦收集筆跡。<br/>                                            |
| [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | 設定是否應聆聽或使用特定事件。<br/>                                                                                   |
| [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | 在已知的手勢中設定 **InkOverlay** 物件的興趣。<br/>                                                                              |
| [**SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | 此模式可讓 **InkOverlay** 物件只從一個平板電腦收集筆跡。 **InkOverlay** 物件會忽略其他平板電腦的筆墨。<br/> |
| [**SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | 設定視窗矩形（以圖元為單位），用來將繪製的筆墨對應至視窗。<br/>                                                                    |



 

### <a name="properties"></a>屬性

**InkOverlay** 類別具有這些屬性。



| 屬性                                                                                       | 存取類型           | 描述                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | 讀取/寫入<br/> | 取得或設定值，這個值會指定是否要將 **InkOverlay** 物件附加在已知視窗的後方或前面。<br/>                                                       |
| [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | 讀取/寫入<br/> | 取得或設定值，這個值會指定當視窗失效時， **InkOverlay** 是否重新繪製筆墨。<br/>                                                                   |
| [**CollectingInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | 唯讀<br/>  | 取得值，這個值會指定是否目前在 **InkOverlay** 物件上繪製筆墨。<br/>                                                                                     |
| [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | 讀取/寫入<br/> | 取得或設定收集模式，這個模式會決定是否將筆墨、手勢或兩者辨識為使用者寫入。<br/>                                                                |
| [**資料指標**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | 唯讀<br/>  | 取得可在筆跡區域中使用的資料 [**指標**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) 集合。<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | 讀取/寫入<br/> | 取得或設定預設的 [**InkDrawingAttributes**](inkdrawingattributes-class.md) 物件，這個物件會指定繪製和顯示筆墨時使用的繪製屬性。<br/> |
| [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | 讀取/寫入<br/> | 取得或設定與在 **InkOverlay** 物件上繪製的筆墨相關聯的封包方面感興趣的內容。<br/>                                                                            |
| [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | 讀取/寫入<br/> | 取得或設定值，這個值會指出是否在繪製時呈現筆墨。<br/>                                                                                                       |
| [**System.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | 讀取/寫入<br/> | 取得或設定值，這個值表示 **InkOverlay** 處於筆墨模式、刪除模式或選取/編輯模式。<br/>                                                          |
| [**啟用**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | 讀取/寫入<br/> | 取得或設定值，這個值會指定 **InkOverlay** 物件是否會收集畫筆輸入。<br/>                                                                                         |
| [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | 讀取/寫入<br/> | 取得或設定值，這個值會指出筆墨是否以筆劃或點清除。<br/>                                                                                                  |
| [**EraserWidth**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | 讀取/寫入<br/> | 取得或設定值，這個值會指定橡皮擦畫筆提示的寬度。<br/>                                                                                                              |
| [**Handle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | 讀取/寫入<br/> | 取得或設定要附加 **InkOverlay** 物件的視窗控制碼。<br/>                                                                                             |
| [**筆跡**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | 讀取/寫入<br/> | 取得或設定與 **InkOverlay** 物件相關聯的 [**InkDisp**](inkdisp-class.md)物件。<br/>                                                                       |
| [**MarginX**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | 讀取/寫入<br/> | 取得或設定沿著 X 軸的邊界（以圖元為單位）。<br/>                                                                                                                             |
| [**MarginY**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | 讀取/寫入<br/> | 取得或設定沿著 y 軸的邊界（以圖元為單位）。<br/>                                                                                                                             |
| [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | 讀取/寫入<br/> | 取得或設定目前的自訂滑鼠圖示。<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | 讀取/寫入<br/> | 取得或設定值，這個值表示當滑鼠停留在物件的特定部分時，所顯示的滑鼠指標類型。<br/>                                                |
| [**轉譯器**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | 讀取/寫入<br/> | 取得或設定用來繪製筆墨的 [**InkRenderer**](inkrenderer-class.md) 物件。<br/>                                                                                        |
| [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | 讀取/寫入<br/> | 取得或設定目前在 **InkOverlay** 控制項內選取的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。<br/>                                                 |
| [**SupportHighContrastInk**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | 讀取/寫入<br/> | 取得或設定值，這個值會指定當系統處於高對比模式時，是否只將筆墨轉譯為一種色彩。<br/>                                                           |
| [**SupportHighContrastSelectionUI**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | 讀取/寫入<br/> | 取得或設定值，這個值會指定當系統處於高對比模式時，是否要以高對比繪製所有選取的 UI。<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | 唯讀<br/>  | 取得 **InkOverlay** 物件目前用來收集輸入的平板電腦裝置。<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>MFC 執行注意事項

如果您將 InkOverlay 物件附加至 CView 物件，請釋放 InkOverlay 物件以回應 WM 終結訊息， \_ 如下列範例所示：


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

**InkOverlay** 物件非常適合用於拍攝和基本 scribbling。 這個物件的主要用途是將筆墨顯示為筆跡。

一般而言，此物件的執行時間使用者介面是透明的視窗，且筆墨不透明。

[**MouseDown**](inkcollector-mousedown.md)、 [**MouseMove**](inkcollector-mousemove.md)、 [**MouseUp**](inkcollector-mouseup.md)和 [**滑鼠滾輪**](inkcollector-mousewheel.md)事件會傳回 x 座標和 y 座標（以圖元為單位），而非與筆墨空間相關聯的 HIMETRIC 單位。 這是因為這些事件會取代不知道應用程式的滑鼠事件，而這些應用程式只會瞭解圖元。

> [!Caution]  
> 如果您要將 **inkoverlay** 物件的 [**AttachMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) 屬性設定為 InFront，請在執行該表單的執行緒中建立 **inkoverlay** 物件。 如果在不同的執行緒中建立了 **InkOverlay** 物件，且其 **AttachMode** 屬性設定為 InFront，則您的應用程式可能會停止回應。

 

> [!Note]  
> 在非 UI 執行緒上無法安全地釋放 **InkOverlay** 物件。

 

若要改善應用程式的效能，請在不再需要您的 **InkOverlay** 物件時進行處置。

如果您將 InkOverlay 物件附加至 CView 物件，請釋放 InkOverlay 物件以回應 WM 終結訊息， \_ 如下列範例所示：


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkCollector 類別**](inkcollector-class.md)
</dt> <dt>

[InkPicture 控制項參考](inkpicture-control-reference.md)
</dt> <dt>

[InkEdit 控制項參考](inkedit-control-reference.md)
</dt> </dl>

 

