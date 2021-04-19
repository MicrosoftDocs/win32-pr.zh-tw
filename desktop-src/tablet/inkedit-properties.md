---
description: 此區段包含屬於 InkEdit 控制項的屬性。
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: InkEdit 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985188"
---
# <a name="inkedit-properties"></a>InkEdit 屬性

此區段包含屬於 InkEdit 控制項的屬性。



| 屬性                                                 | 描述                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**外觀**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | 取得或設定值，這個值會判斷 [InkEdit](inkedit-control-reference.md) 控制項是否顯示為平面或立體。<br/>                                                                      |
| [**顏色**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項的背景色彩。<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | 取得或設定值，這個值會決定 [InkEdit](inkedit-control-reference.md) 控制項是否有框線。<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | 取得或設定值，這個值會決定是否停用 [InkEdit](inkedit-control-reference.md) 控制項中的捲軸。<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | 取得或設定尚未在 [InkEdit](inkedit-control-reference.md) 控制項上繪製之筆墨的繪圖屬性。<br/>                                                                |
| [**啟用**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | 取得或設定值，這個值會決定 [InkEdit](inkedit-control-reference.md) 控制項是否可以回應使用者產生的事件。<br/>                                                     |
| [**標記**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | 取得或設定 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件用來限制其搜尋辨識結果的 [模擬](factoid-constants.md)條件常數。<br/>                  |
| [**字型**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項顯示之文字的字型。<br/>                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | 取得 [**InkDisp**](inkdisp-class.md) 控制項所系結的視窗控制碼。<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | 取得或設定值，這個值會指定如何將筆墨插入至 [InkEdit](inkedit-control-reference.md) 控制項（以文字或筆墨的形式）。<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | 取得或設定值，這個值會指定是否停用筆墨收集、收集筆跡，或是收集筆跡和手勢。<br/>                                                                |
| [**鎖定**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | 取得或設定值，這個值會指定 [InkEdit](inkedit-control-reference.md) 控制項是否為唯讀。<br/>                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | 取得或設定值，指出 [InkEdit](inkedit-control-reference.md) 控制項是否可以保留最大字元數，如果是，則指定最大字元數。<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | 取得或設定目前的自訂滑鼠圖示。<br/>                                                                                                                                                 |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | 取得或設定值，這個值表示當滑鼠停留在 [InkEdit](inkedit-control-reference.md) 控制項的特定部分時，所顯示的滑鼠指標類型。<br/>                |
| [**適用**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | 取得或設定值，這個值會指出這是否為多行 [InkEdit](inkedit-control-reference.md) 控制項。<br/>                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | 取得或設定上次收集 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件與文字辨識開頭之間的時間長度（以毫秒為單位）。<br/>                         |
| [**辨識器**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | 取得或設定要用於辨識的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件。<br/>                                                                                                    |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | 取得或設定顯示在 [InkEdit](inkedit-control-reference.md) 控制項中的捲軸類型。<br/>                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | 取得或設定要套用至目前選取範圍或插入點的對齊， (執行時間僅) 。<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | 取得或設定值，這個值會指定 [InkEdit](inkedit-control-reference.md) 控制項中目前所選取文字的字型樣式是否僅)  (執行時間。<br/>                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項中的文字是否顯示在基準上（以上標表示），或僅) 的 (執行時間。<br/>                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | 取得或設定目前文字選取範圍或插入點的文字色彩 (執行時間) 。<br/>                                                                                               |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項中所選取文字的字型名稱， (執行時間僅) 。<br/>                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項中所選取文字的字型大小， (僅限執行時間) 。<br/>                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | 取得或設定內嵌 [**InkDisp**](inkdisp-class.md) 物件的陣列 (如果顯示為目前選取範圍所包含的筆墨) 。<br/>                                                      |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | 取得或設定值，這個值允許切換筆跡和文字之間選取的外觀。<br/>                                                                                             |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | 取得或設定值，這個值會指定 [InkEdit](inkedit-control-reference.md) 控制項中目前所選取文字的字型樣式是否為斜體 (執行時間僅) 。<br/>                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項中選取的字元數 (執行時間) 。<br/>                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | 取得或設定目前選取的 Rtf 格式 (RTF) [InkEdit](inkedit-control-reference.md) 控制項中格式化的文字 (執行時間只) 。<br/>                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | 取得或設定文字方塊中所選取文字的起始點， (執行時間僅) 。<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項中選取的文字 (執行時間) 。<br/>                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | 取得或設定值，這個值會指定 [InkEdit](inkedit-control-reference.md) 控制項中目前所選取文字的字型樣式是否只 (執行時間) 加上底線。<br/>            |
| [**狀態**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | 取得值，這個值會指定 [InkEdit](inkedit-control-reference.md) 控制項為閒置、收集筆墨或辨識筆墨 (執行時間) 。<br/>                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | 取得或設定文字方塊中目前的文字。<br/>                                                                                                                                              |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | 取得或設定 [InkEdit](inkedit-control-reference.md) 控制項的文字，包括所有 RTF 程式碼。<br/>                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | 取得或設定值，這個值表示是否可以使用滑鼠做為輸入裝置。<br/>                                                                                                       |



 

 

 




