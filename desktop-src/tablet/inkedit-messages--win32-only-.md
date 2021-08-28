---
description: InkEdit 控制項是 RichEdit 控制項的超級類別。
ms.assetid: 26023012-9ab1-4bd9-beff-41587bc74f5e
title: 'InkEdit 訊息 (僅限 Win32) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cb1d390bf8e37d6affbbd96c34c53ea889b268
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475034"
---
# <a name="inkedit-messages-win32-only"></a>InkEdit 訊息 (僅限 Win32) 

[InkEdit](inkedit-control-reference.md)控制項是 [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole)控制項的超級類別。 在大部分的情況下，會直接傳入每個 **RichEdit** 訊息，且其效果與 **RichEdit** 完全相同。 這也適用于事件通知訊息。

若要傳送這些訊息，請使用下列參數呼叫 SendMessage 函數：




| C++ | 
|-----|
| <pre data-space="preserve"><code>LRESULT SendMessage(  HWND hWnd,      // handle to destination window  UINT Msg,       // message  WPARAM wParam,  // first message parameter  LPARAM lParam   // second message parameter);</code></pre> | 




 

## <a name="message"></a>訊息

[InkEdit](inkedit-control-reference.md)控制項的父視窗會透過 WM 通知訊息接收事件通知訊息 \_ ：


```C++
LRESULT CALLBACK WindowProc(
    HWND hWnd,                // handle to window
    UINT uMsg,                // WM_NOTIFY
    WPARAM wParam,        // InkEdit control identifier
    LPARAM lParam            // see documentation for notification messages
);
```





| 取得/設定訊息                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EM \_ GETINKMODE<br/>           | 取得 [InkEdit](inkedit-control-reference.md) 控制項的筆墨模式。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 此訊息會傳回 [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) 列舉中所定義的其中一個值，這個值會指定是否停用筆墨收集、是否要收集筆跡，或是否要收集筆跡和手勢。<br/>                                                                                                                                                                                                                                                         |
| EM \_ SETINKMODE<br/>           | 設定 [InkEdit](inkedit-control-reference.md) 控制項的筆墨模式。<br/> 參數：<br/>*wParam* 指定 [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) 列舉的其中一個值，這個值會指定是否停用筆墨收集、是否要收集筆跡，或是否要收集筆跡和手勢。<br/>*lParam* 未使用此參數;它必須是0。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/> 備註：<br/> 只有當 EM GETSTATUS 傳回的是閒置時，才應該使用這種情況 \_ \_ 。<br/>                                                                                                               |
| EM \_ GETINKINSERTMODE<br/>     | 取得 [InkEdit](inkedit-control-reference.md) 控制項的筆墨插入模式。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 此訊息會傳回 [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) 列舉的其中一個值，這個值會指定是否要將筆墨插入控制項中做為文字或筆跡。<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETINKINSERTMODE<br/>     | 設定 [InkEdit](inkedit-control-reference.md) 控制項的筆墨插入模式。 如果與 Microsoft Windows XP Tablet PC Edition 以外安裝的任何作業系統搭配使用，則傳送此訊息不會有任何作用。<br/> 參數：<br/>*wParam* 指定 [**InkInsertMode**](/windows/desktop/api/inked/ne-inked-inkinsertmode) 列舉的其中一個值，指定是否要將筆墨插入控制項中做為文字或筆跡。<br/>*lParam* 未使用此參數;它必須是0。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                       |
| EM \_ GETDRAWATTR<br/>          | 取得 [InkEdit](inkedit-control-reference.md) 控制項的目前繪圖屬性。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定指標 (IInkDrawingAttributes \* \* pDrawAttr) ，以接收目前的 [**InkDrawingAttributes**](inkdrawingattributes-class.md)物件。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                |
| EM \_ SETDRAWATTR<br/>          | 設定要用於未來筆墨收集的繪製屬性。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定指向 \* [**InkDrawingAttributes**](inkdrawingattributes-class.md) 物件之 IInkDrawingAttributes pDrawAttr) 的指標 (。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                                                                  |
| EM \_ GETRECOTIMEOUT<br/>       | 取得 [InkEdit](inkedit-control-reference.md) 控制項的辨識超時（以毫秒為單位）。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 此訊息會傳回辨識超時（以毫秒為單位）。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ SETRECOTIMEOUT<br/>       | 設定 [InkEdit](inkedit-control-reference.md) 控制項的辨識超時（以毫秒為單位）。<br/> 參數：<br/>*wParam* 指定辨識超時（以毫秒為單位）。<br/>*lParam* 未使用此參數;它必須是0。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                                                                                                    |
| EM \_ GETGESTURESTATUS<br/>     | 取得 [InkEdit](inkedit-control-reference.md) 控制項的手勢狀態。<br/> 參數：<br/>*wParam* 指定筆勢的類型，如 [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉中所定義。<br/>*lParam* 未使用此參數;它必須是0。<br/> 傳回值：<br/> 如果 [InkEdit](inkedit-control-reference.md)控制項訂閱手勢，此訊息會傳回 **TRUE** ，如果 InkEdit 控制項未訂閱筆勢，則會傳回 **FALSE** 。<br/>                                                                                                                                                                       |
| EM \_ SETGESTURESTATUS<br/>     | 設定 [InkEdit](inkedit-control-reference.md) 控制項的筆勢狀態。<br/> 參數：<br/>*wParam* 指定筆勢的類型，如 [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉中所定義。<br/>*lParam* 如果已啟用手勢的訂閱，則指定 **為 TRUE** ，如果未啟用接聽手勢，則指定 **為 FALSE** 。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/> 備註：<br/> 只有當 EM GETSTATUS 傳回的是閒置時，才應該使用這種情況 \_ \_ 。<br/>                                                                                                               |
| EM \_ GETRECOGNIZER<br/>        | 取得 [InkEdit](inkedit-control-reference.md) 控制項使用的辨識器。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定 IInkRecognizer 的指標， \* 以接收 [InkEdit](inkedit-control-reference.md)控制項所使用的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                   |
| EM \_ SETRECOGNIZER<br/>        | 設定 [InkEdit](inkedit-control-reference.md) 控制項使用的辨識器。 如果 InkEdit 控制項使用了 [模擬](factoid-constants.md) 程式，則必須在傳送此訊息之後重新套用。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定 IInkRecognizer 的指標， \* 以設定 [InkEdit](inkedit-control-reference.md)控制項用來在稍後使用的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/> 備註：<br/> 只有當 EM GETSTATUS 傳回的是閒置時，才應該使用這種情況 \_ \_ 。<br/> |
| EM \_ GETFACTOID<br/>           | 取得要用於辨識的 [智慧](factoid-constants.md) 標記。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定要接收模擬型字串之 BSTR 的指標。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETFACTOID<br/>           | 設定要用於辨識的 [模擬](factoid-constants.md) 程式。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定包含模擬字串的 BSTR。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/> 備註：<br/> 只有當 EM GETSTATUS 傳回的是閒置時，才應該使用這種情況 \_ \_ 。<br/>                                                                                                                                                                                                                                                                          |
| EM \_ GETSELINK<br/>            | 取得選取範圍內的筆墨。 必須先辨識筆墨，才能透過此訊息進行存取。 如果無法先辨識，EM \_ GETSELINK 一律會傳回零個 [**InkDisp**](inkdisp-class.md) 物件。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定 VARIANT 的指標，以接收安全陣列以接收目前選取範圍內的 [**InkDisp**](inkdisp-class.md) 物件。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                     |
| EM \_ SETSELINK<br/>            | 設定選取範圍內的筆墨。 如果與安裝 Windows XP Tablet PC Edition 以外的任何作業系統搭配使用，則傳送此訊息不會有任何作用。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定具有 [**InkDisp**](inkdisp-class.md) 物件之安全陣列的變異指標，以取代目前的選取範圍。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                     |
| EM \_ GETSELINKDISPLAYMODE<br/> | 使用 [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) 列舉的其中一個值，傳回所選範圍中筆墨目前的外觀。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 此訊息會傳回 [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) 列舉的其中一個值 (idm \_ Text 或 IDM \_ 筆墨) ，以指定如何在控制項上顯示選取範圍。<br/>                                                                                                                                                                                                                           |
| EM \_ SETSELINKDISPLAYMODE<br/> | 使用 [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) 列舉的其中一個值，設定所選範圍中筆墨的外觀。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定如何在選取的範圍中顯示筆墨，如 [**InkDisplayMode**](/windows/desktop/api/inked/ne-inked-inkdisplaymode) 列舉中所定義。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。 如果與安裝 Windows XP Tablet PC Edition 以外的任何作業系統搭配使用，則傳送此訊息不會有任何作用。<br/>                                                                                                   |
| EM \_ GETSTATUS<br/>            | 取得 [InkEdit](inkedit-control-reference.md) 控制項的狀態。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 此訊息會傳回 [**InkEditStatus**](/windows/desktop/api/inked/ne-inked-inkeditstatus) 列舉的其中一個值，這個值會指定控制項為閒置、收集筆墨或辨識筆跡。<br/>                                                                                                                                                                                                                                                                                                           |
| EM \_ 辨識<br/>            | 強制辨識。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| EM \_ GETMOUSEICON<br/>         | 取得滑鼠圖示。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 指定以 \* 目前的 [**MouseIcon**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon) HICON 填入的 HICON 指標。 這個 HICON 可以是 HICON 或 **Null** 值。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                                                                    |
| EM \_ SETMOUSEICON<br/>         | 設定滑鼠圖示。<br/> 參數：<br/>*wParam* 指定布林值，如果 [InkEdit](inkedit-control-reference.md)控制項應該擁有 HICON 控制碼，則設定為 **TRUE** ，如果 InkEdit 控制項不應擁有 HICON 控制碼，則為 **FALSE** 。 如果 InkEdit 控制項擁有 HICON，則會負責並適當地終結 HICON。 否則，呼叫端會擁有 HICON，並負責刪除它。<br/>*lParam* 指定新的 HICON 值。 使用 **Null** 來清除此值。 預設值是 **NULL**。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                |
| EM \_ GETMOUSEPOINTER<br/>      | 取得滑鼠指標。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 包含以 \* 目前的 [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) 值填入的 InkMousePointer 指標。 其行為與 **InkCollector：： get \_ MousePointer** 屬性相同。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                                            |
| EM \_ SETMOUSEPOINTER<br/>      | 設定滑鼠指標。<br/> 參數：<br/>*wParam* 未使用此參數;它必須是0。<br/>*lParam* 包含新的 [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer) 值，此值定義于 [**InkMousePointer**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer) 列舉中。 其行為與 **InkCollector：:p 的 \_ MousePointer** 屬性相同。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/>                                                                                                                                                                                                                                    |
| EM \_ GETUSEMOUSEFORINPUT<br/>  | 取得是否將滑鼠輸入視為畫筆輸入的狀態。<br/> 參數：<br/> 此訊息沒有參數; *wParam* 和 *lParam* 必須是0。<br/> 傳回值：<br/> 如果為 **FALSE** ，則此訊息會傳回 0; 如果 **為 TRUE**，則傳回1。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| EM \_ SETUSEMOUSEFORINPUT<br/>  | 設定滑鼠輸入是否視為畫筆輸入的狀態。<br/> 參數：<br/>*wParam* 指定布林值，決定是否要將滑鼠輸入視為畫筆輸入。<br/>*lParam* 未使用此參數;它必須是0。<br/> 傳回值：<br/> 如果成功，則此訊息會傳回0，如果發生錯誤則傳回非零值。<br/> 備註：<br/> 只有當 EM GETSTATUS 傳回的是閒置時，才應該使用這種情況 \_ \_ 。<br/>                                                                                                                                                                                                                                             |



 



| 事件通知訊息         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IECN \_ 筆觸<br/>            | 通知 [InkEdit](inkedit-control-reference.md) 控制項的父視窗，指出已建立 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 。 這會 \_ 使用下列參數在 WM 通知訊息中傳送。<br/> 參數：<br/>*wParam* 指定傳送訊息之控制項的識別碼。<br/>*lParam* 指定 [**IEC \_ STROKEINFO**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo) 結構的指標。<br/> 傳回值：<br/> 用戶端會傳回0以接受筆劃，1則會取消筆劃。<br/> |
| IECN \_ 手勢<br/>           | 通知 [InkEdit](inkedit-control-reference.md) 控制項的父視窗，表示已辨識手勢。 這會 \_ 使用下列參數在 WM 通知訊息中傳送。<br/> 參數：<br/>*wParam* 指定傳送訊息之控制項的識別碼。<br/>*lParam* 指定 [**IEC \_ GESTUREINFO**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo) 結構的指標。<br/> 傳回值：<br/> 用戶端會傳回0以接受手勢，1則會取消手勢。<br/>                           |
| IECN \_ RECOGNITIONRESULT<br/> | 通知 [InkEdit](inkedit-control-reference.md) 控制項的父視窗，確認已發生。 這會 \_ 使用下列參數在 WM 通知訊息中傳送。<br/> 參數：<br/>*wParam* 指定傳送訊息之控制項的識別碼。<br/>*lParam* 指定 [**IEC \_ RECOGNITIONRESULTINFO**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo) 結構的指標。<br/> 傳回值：<br/> 用戶端會在處理訊息時傳回0。<br/>                                  |



 

## <a name="applies-to"></a>套用至

-   [InkEdit](inkedit-control-reference.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IEC \_ GESTUREINFO 結構 (僅限 Win32)**](/windows/desktop/api/inked/ns-inked-iec_gestureinfo)
</dt> <dt>

[**IEC \_ STROKEINFO 結構 (僅限 Win32)**](/windows/desktop/api/inked/ns-inked-iec_strokeinfo)
</dt> <dt>

[**IEC \_ RECOGNITIONRESULTINFO 結構 (僅限 Win32)**](/windows/desktop/api/inked/ns-inked-iec_recognitionresultinfo)
</dt> <dt>

[**MousePointer 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)
</dt> <dt>

[**InkEditStatus 列舉**](/windows/desktop/api/inked/ne-inked-inkeditstatus)
</dt> <dt>

[**InkInsertMode 列舉**](/windows/desktop/api/inked/ne-inked-inkinsertmode)
</dt> <dt>

[**InkMode 列舉**](/windows/desktop/api/inked/ne-inked-inkmode)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDrawingAttributes 類別**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkRecognitionResult 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> <dt>

[**IInkRecognizer 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkDisp 類別**](inkdisp-class.md)
</dt> <dt>

[**IInkGesture 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)
</dt> </dl>

 

