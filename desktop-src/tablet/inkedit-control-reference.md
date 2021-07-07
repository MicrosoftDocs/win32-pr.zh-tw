---
description: InkEdit 控制項可讓您收集筆跡、辨識筆墨，以及將筆墨顯示為文字。
ms.assetid: 52761cb2-4433-4824-ba19-fe597de2faf0
title: InkEdit 控制項參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe2aad6b7d8b536f2ede35fd93bd19840e69fc
ms.sourcegitcommit: f8f06d7ad2ff6599e90b0493b355e0c1811d898f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113369310"
---
# <a name="inkedit-control-reference"></a>InkEdit 控制項參考

InkEdit 控制項可讓您收集筆跡、辨識筆墨，以及將筆墨顯示為文字。 此控制項可讓您啟用智慧型表單，以改善文字輸入的精確度。

此控制項是 [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) 控制項的超集合。 它會擴充 **RichEdit** 控制項，並具備可捕獲、辨識和顯示筆墨的能力。

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

在透明控制項背後建立 InkEdit 控制項 (例如，加上 WS \_ EX \_ 透明屬性集) 的分組會導致 InkEdit 無法收集筆跡。

## <a name="members"></a>成員



| 列舉型別                                            | 描述                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppearanceConstants**](/windows/desktop/api/inked/ne-inked-appearanceconstants)     | 定義值，這個值會指定控制項是否顯示為平面或立體。<br/>                                                                                            |
| [**BorderStyleConstants**](/windows/desktop/api/inked/ne-inked-borderstyleconstants)   | 定義指定控制項是否有框線的值。<br/>                                                                                                   |
| [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) | 定義值，這些值會在一組應用程式特定的手勢中設定感興趣的值。<br/>                                                                                 |
| [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode)               | 定義值，這個值會指定選取範圍是否顯示為筆墨或文字。<br/>                                                                                         |
| [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus)                 | 定義值，這個值會指定 InkEdit 控制項為閒置、收集筆墨或辨識筆跡。<br/>                                                            |
| [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode)                 | 定義值，這些值會指定如何將筆墨插入至 InkEdit 控制項。<br/>                                                                                       |
| [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode)                             | 定義值，這些值會指定繪圖筆墨的收集模式設定：是否停用筆墨收集、收集筆跡，或是收集筆跡和手勢。<br/> |
| [**InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)               | 定義指定按下滑鼠按鍵的值。<br/>                                                                                                     |
| [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer)             | 定義值，這些值會指定出現的滑鼠指標類型。<br/>                                                                                             |
| [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)                     | 定義指定按下滑鼠按鍵的值。<br/>                                                                                                     |
| [**ScrollBarsConstants**](/windows/desktop/api/inked/ne-inked-scrollbarsconstants)     | 定義值，這些值會指定 InkEdit 控制項捲軸如何顯示在螢幕上。<br/>                                                                     |
| [**SelAlignmentConstants**](/windows/desktop/api/inked/ne-inked-selalignmentconstants) | 定義值，這個值會指定相對於 InkEdit 控制項邊界的段落對齊。<br/>                                                      |



 



| 事件通知訊息                                   | Description                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [IECN \_ 筆觸](inkedit-messages--win32-only-.md)            | 當筆劃完成時，會透過 WM 通知訊息傳送此訊息 \_ (Win32) 。<br/>  |
| [IECN \_ 手勢](inkedit-messages--win32-only-.md)           | \_當手勢完成 (僅限 Win32) 時，會透過 WM 通知訊息傳送此訊息。<br/> |
| [IECN \_ RECOGNITIONRESULT](inkedit-messages--win32-only-.md) | 這則訊息會在進行辨識時，透過 WM \_ 通知訊息傳送 (僅限 Win32) 。<br/>     |



 



| 事件                                                  | 描述                                                                                                                                                                                 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**改變**](inkedit-change.md)                       | 發生于控制項的內容或屬性值變更時。<br/>                                                                                                              |
| [**按一下**](inkedit-click.md)                         | 發生於按下控制項時。<br/>                                                                                                                                              |
| [**DblClick**](inkedit-dblclick.md)                   | 發生於按兩下控制項時。<br/>                                                                                                                                       |
| [**手勢**](inkedit-gesture.md)                     | 當應用程式手勢被辨識時發生。<br/>                                                                                                                                |
| [**KeyDown**](inkedit-keydown.md)                     | 當使用者按下按鍵時，InkEdit 控制項有焦點時發生。<br/>                                                                                                          |
| [**KeyPress**](inkedit-keypress.md)                   | 發生于 InkEdit 控制項具有焦點時按下按鍵時。<br/>                                                                                                                |
| [**KeyUp**](inkedit-keyup.md)                         | 當 InkEdit 控制項具有焦點時，放開按鍵時發生。<br/>                                                                                                               |
| [**MouseDown**](inkedit-mousedown.md)                 | 發生于滑鼠指標位於 InkEdit 控制項上方且按下滑鼠按鍵時。<br/>                                                                                         |
| [**MouseMove**](inkedit-mousemove.md)                 | 發生于滑鼠指標移至 InkEdit 控制項時。<br/>                                                                                                                 |
| [**MouseUp**](inkedit-mouseup.md)                     | 發生于滑鼠指標位於 InkEdit 控制項上方並放開滑鼠按鍵時。<br/>                                                                                        |
| [**RecognitionResult**](inkedit-recognitionresult.md) | 當 InkEdit 控制項以手動方式從呼叫辨識方法或在 [**辨識**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) 超時之後自動取得結果時發生。<br/> |
| [**SelChange**](inkedit-selchange.md)                 | InkEdit 控制項中的筆跡選取範圍變更時發生。<br/>                                                                                                             |
| [**中風**](inkedit-stroke.md)                       | 當使用者在任何 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)物件上繪製新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件時發生。<br/>                                                 |



 



| 取得/設定訊息                                               | Description                                                                                                                                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EM \_ GETINKMODE](inkedit-messages--win32-only-.md)           | 取得控制項 (僅限 Win32) 的筆墨模式。<br/>                                                                                                                       |
| [EM \_ SETINKMODE](inkedit-messages--win32-only-.md)           | 將控制項的筆墨模式設定 (僅限 Win32) 。<br/>                                                                                                                       |
| [EM \_ GETINKINSERTMODE](inkedit-messages--win32-only-.md)     | 取得控制項 (僅限 Win32) 的筆墨插入模式。<br/>                                                                                                             |
| [EM \_ SETINKINSERTMODE](inkedit-messages--win32-only-.md)     | 將控制項的筆墨插入模式設定 (僅限 Win32) 。<br/>                                                                                                             |
| [EM \_ GETDRAWATTR](inkedit-messages--win32-only-.md)          | 取得控制項的目前繪圖屬性 (Win32) 。<br/>                                                                                                     |
| [EM \_ SETDRAWATTR](inkedit-messages--win32-only-.md)          | 設定要用於未來筆跡集合的繪製屬性， (僅限 Win32) 。<br/>                                                                                           |
| [EM \_ GETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | 取得控制項的辨識超時 (僅限 Win32) 。<br/>                                                                                                           |
| [EM \_ SETRECOTIMEOUT](inkedit-messages--win32-only-.md)       | 將控制項的辨識超時設定 (僅限 Win32) 。<br/>                                                                                                           |
| [EM \_ GETGESTURESTATUS](inkedit-messages--win32-only-.md)     | 取得控制項 (僅限 Win32) 的筆勢狀態。<br/>                                                                                                                |
| [EM \_ SETGESTURESTATUS](inkedit-messages--win32-only-.md)     | 將控制項的手勢狀態設定 (僅限 Win32) 。<br/>                                                                                                                |
| [EM \_ GETRECOGNIZER](inkedit-messages--win32-only-.md)        | 取得控制項使用 (Win32) 的辨識器。<br/>                                                                                                              |
| [EM \_ SETRECOGNIZER](inkedit-messages--win32-only-.md)        | 設定控制項使用 (Win32) 的辨識器。<br/>                                                                                                              |
| [EM \_ GETFACTOID](inkedit-messages--win32-only-.md)           | 取得要用於辨識 (僅限 Win32) 的模擬程式。<br/>                                                                                                                |
| [EM \_ SETFACTIOD](inkedit-messages--win32-only-.md)           | 設定要用於辨識 (僅限 Win32) 的模擬程式。<br/>                                                                                                                |
| [EM \_ GETSELINK](inkedit-messages--win32-only-.md)            | 取得選取範圍中的筆墨 (僅限 Win32) 。<br/>                                                                                                                          |
| [EM \_ SETSELINK](inkedit-messages--win32-only-.md)            | 將選取範圍中的筆墨設定 (僅限 Win32) 。<br/>                                                                                                                          |
| [EM \_ GETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | 使用 [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) 列舉的其中一個值 (僅限 Win32) ，傳回所選範圍中筆墨的目前外觀。<br/> |
| [EM \_ SETSELINKDISPLAYMODE](inkedit-messages--win32-only-.md) | 使用 [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) 列舉的其中一個值 (僅限 Win32) ，以設定所選範圍中筆墨的外觀。<br/>            |
| [EM \_ GETSTATUS](inkedit-messages--win32-only-.md)            | 取得僅限 (Win32) 的控制項狀態。<br/>                                                                                                                         |
| [EM \_ 辨識](inkedit-messages--win32-only-.md)            | 強制辨識 (僅限 Win32) 。<br/>                                                                                                                                     |
| [EM \_ GETMOUSEICON](inkedit-messages--win32-only-.md)         | 取得滑鼠圖示 (僅限 Win32) 。<br/>                                                                                                                                    |
| [EM \_ SETMOUSEICON](inkedit-messages--win32-only-.md)         | 將滑鼠圖示設定 (僅限 Win32) 。<br/>                                                                                                                                    |
| [EM \_ GETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | 取得滑鼠指標 (僅限 Win32) 。<br/>                                                                                                                                 |
| [EM \_ SETMOUSEPOINTER](inkedit-messages--win32-only-.md)      | 將滑鼠指標的 Win32 設定) 。<br/>                                                                                                                                  |
| [EM \_ GETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | 取得滑鼠輸入是否視為畫筆輸入的狀態， (僅限 Win32) 。<br/>                                                                                        |
| [EM \_ SETUSEMOUSEFORINPUT](inkedit-messages--win32-only-.md)  | 設定是否要將滑鼠輸入視為畫筆輸入，例如 (Win32) 。<br/>                                                                                        |



 



| 方法                                               | 描述                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------|
| [**GetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus) | 以一組已知的手勢取得 InkEdit 控制項的興趣。<br/> |
| [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)               | 指定應進行辨識。<br/>                             |
| [**重新整理**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)             | 使控制項重新繪製。<br/>                                        |
| [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) | 以一組已知的手勢設定 InkEdit 控制項的興趣。<br/> |



 



| 屬性                                                 | 描述                                                                                                                                                                           |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**外觀**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | 取得或設定值，這個值會判斷 InkEdit 控制項是否顯示為平面或立體。<br/>                                                                                      |
| [**顏色**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | 取得或設定 InkEdit 控制項的背景色彩。<br/>                                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | 取得或設定值，這個值會決定 InkEdit 控制項是否有框線。<br/>                                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | 取得或設定值，這個值會決定是否停用 InkEdit 控制項中的捲軸。<br/>                                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | 取得或設定尚未在 InkEdit 控制項上繪製之筆墨的繪圖屬性。<br/>                                                                                |
| [**啟用**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | 取得或設定值，這個值會決定 InkEdit 控制項是否可以回應使用者產生的事件。<br/>                                                                     |
| [**標記**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | 取得或設定 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件用來限制其搜尋辨識結果的 [模擬](factoid-constants.md)條件常數。<br/> |
| [**字型**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | 取得或設定 InkEdit 控制項顯示之文字的字型。<br/>                                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | 取得 [**InkDisp**](inkdisp-class.md) 控制項所系結的視窗控制碼。<br/>                                                                                     |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | 取得或設定值，這個值會指定如何將筆墨插入至 InkEdit 控制項（以文字或筆墨的形式）。<br/>                                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | 取得或設定值，這個值會指定是否停用筆墨收集、收集筆跡，或是收集筆跡和手勢。<br/>                                               |
| [**已鎖定**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | 取得或設定值，這個值會指定 InkEdit 控制項是否為唯讀。<br/>                                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | 取得或設定值，指出 InkEdit 控制項是否可以保留最大字元數，如果是，則指定最大字元數。<br/>                 |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | 取得或設定目前的自訂滑鼠圖示。<br/>                                                                                                                                |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | 取得或設定值，這個值表示當滑鼠停留在 InkEdit 控制項的特定部分時，所顯示的滑鼠指標類型。<br/>                                |
| [**適用**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | 取得或設定值，這個值會指出這是否為多行 InkEdit 控制項。<br/>                                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | 取得或設定上次收集 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件與文字辨識開頭之間的時間長度（以毫秒為單位）。<br/>        |
| [**識別**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | 取得或設定要用於辨識的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件。<br/>                                                                                   |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | 取得或設定顯示在 InkEdit 控制項中的捲軸類型。<br/>                                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | 取得或設定要套用至目前選取範圍或插入點的對齊， (執行時間僅) 。<br/>                                                                           |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | 取得或設定值，這個值會指定 InkEdit 控制項中目前所選取文字的字型樣式是否僅)  (執行時間。<br/>                                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | 取得或設定 InkEdit 控制項中的文字是否顯示在基準上（以上標表示），或僅) 的 (執行時間。<br/>                                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | 取得或設定目前文字選取範圍或插入點的文字色彩 (執行時間) 。<br/>                                                                              |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | 取得或設定 InkEdit 控制項中所選取文字的字型名稱， (執行時間僅) 。<br/>                                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | 取得或設定 InkEdit 控制項中所選取文字的字型大小， (僅限執行時間) 。<br/>                                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | 取得或設定內嵌 [**InkDisp**](inkdisp-class.md) 物件的陣列 (如果顯示為目前選取範圍所包含的筆墨) 。<br/>                                     |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | 取得或設定值，這個值允許切換筆跡和文字之間選取的外觀。<br/>                                                                            |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | 取得或設定值，這個值會指定 InkEdit 控制項中目前所選取文字的字型樣式是否為斜體 (執行時間僅) 。<br/>                                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | 取得或設定 InkEdit 控制項中選取的字元數 (執行時間) 。<br/>                                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | 取得或設定目前選取的 Rtf 格式 (RTF) InkEdit 控制項中格式化的文字 (執行時間只) 。<br/>                                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | 取得或設定文字方塊中所選取文字的起始點， (執行時間僅) 。<br/>                                                                              |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | 取得或設定 InkEdit 控制項中選取的文字 (執行時間) 。<br/>                                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | 取得或設定值，這個值會指定 InkEdit 控制項中目前所選取文字的字型樣式是否只 (執行時間) 加上底線。<br/>                            |
| [**狀態**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | 取得值，這個值會指定 InkEdit 控制項為閒置、收集筆墨或辨識筆墨 (執行時間) 。<br/>                                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | 取得或設定文字方塊中目前的文字。<br/>                                                                                                                             |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | 取得或設定 InkEdit 控制項的文字，包括所有 RTF 程式碼。<br/>                                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | 取得或設定值，這個值表示是否可以使用滑鼠做為輸入裝置。<br/>                                                                                      |

| 結構                                                                    | Description                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)                       | 包含 [**筆劃**](inkedit-stroke.md) 事件 (僅限 Win32) 的相關資訊。<br/> |
| [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)                     | 包含特定手勢 (僅限 Win32) 的相關資訊。<br/>                       |
| [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) | 包含 (Win32) 的辨識結果相關資訊。<br/>                     |

## <a name="com-implementation"></a>COM 執行

這個物件會實 [IInkEdit](/windows/win32/api/inked/nn-inked-iinkedit) COM 介面。

## <a name="related-topics"></a>相關主題

- [**InkOverlay 類別**](inkoverlay-class.md)， 
- [InkPicture 控制項參考](inkpicture-control-reference.md)
- [**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)
