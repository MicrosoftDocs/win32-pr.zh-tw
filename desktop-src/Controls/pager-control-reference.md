---
title: 呼叫器
description: 本章節包含與分頁控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bf9860c9e1dd1d565b24c7bbfc02e46480198f5bdea03717288abc83591a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914768"
---
# <a name="pager"></a>呼叫器

本章節包含與分頁控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                | 目錄                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [呼機控制項](pager-controls.md) | *呼機控制項* 是一種視窗容器，它會與沒有足夠顯示區域的視窗一起顯示，以顯示其所有內容。<br/> |



 

### <a name="macros"></a>巨集



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**呼機 \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | 啟用或停用呼機控制項的滑鼠轉送。 啟用滑鼠轉寄時，分頁控制項會將 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息轉送至包含的視窗。 您可以使用此宏，或明確地傳送 [**PGM \_ FORWARDMOUSE**](pgm-forwardmouse.md) 訊息。 <br/>                                                                                                                     |
| [**呼機 \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | 抓取呼機控制項目前的背景色彩。 您可以使用此宏，或明確地傳送 [**PGM \_ GETBKCOLOR**](pgm-getbkcolor.md) 訊息。 <br/>                                                                                                                                                                                                                                                                 |
| [**呼機 \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | 抓取呼機控制項目前的框線大小。 您可以使用此宏，或明確地傳送 [**PGM \_ GETBORDER**](pgm-getborder.md) 訊息。 <br/>                                                                                                                                                                                                                                                                        |
| [**呼機 \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | 抓取頁面導航控制項目前的按鈕大小。 您可以使用此宏，或明確地傳送 [**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md) 訊息。 <br/>                                                                                                                                                                                                                                                                |
| [**呼機 \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | 抓取頁面導航控制項中指定之按鈕的狀態。 您可以使用此宏，或明確地傳送 [**PGM \_ GETBUTTONSTATE**](pgm-getbuttonstate.md) 訊息。 <br/>                                                                                                                                                                                                                                                       |
| [**呼機 \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | 抓取呼機控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 介面指標。 您可以使用此宏，或明確地傳送 [**PGM \_ GETDROPTARGET**](pgm-getdroptarget.md) 訊息。 <br/>                                                                                                                                                                                                                                       |
| [**呼機 \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | 抓取呼機控制項目前的滾動位置。 您可以使用此宏，或明確地傳送 [**PGM \_ GETPOS**](pgm-getpos.md) 訊息。 <br/>                                                                                                                                                                                                                                                                           |
| [**呼機 \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | 強制呼機控制項重新計算包含視窗的大小。 使用這個宏會導致傳送 [PGN 的 \_ CALCSIZE](pgn-calcsize.md) 通知。 您可以使用此宏，或明確地傳送 [**PGM \_ RECALCSIZE**](pgm-recalcsize.md) 訊息。 <br/>                                                                                                                                                        |
| [**呼機 \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | 設定呼機控制項目前的背景色彩。 您可以使用此宏，或明確地傳送 [**PGM \_ SETBKCOLOR**](pgm-setbkcolor.md) 訊息。 <br/>                                                                                                                                                                                                                                                                      |
| [**呼機 \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | 設定呼機控制項的目前框線大小。 您可以使用此宏，或明確地傳送 [**PGM \_ SETBORDER**](pgm-setborder.md) 訊息。 <br/>                                                                                                                                                                                                                                                                             |
| [**呼機 \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | 設定呼機控制項目前的按鈕大小。 您可以使用此宏，或明確地傳送 [**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md) 訊息。 <br/>                                                                                                                                                                                                                                                                     |
| [**呼機 \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | 設定呼機控制項的包含視窗。 這個宏不會變更包含視窗的父系;它只會將視窗控制碼指派給呼機控制項以供滾動。 在大部分的情況下，包含的視窗將會是子視窗。 如果是這種情況，則包含的視窗應該是呼機控制項的子系。 您可以使用此宏，或明確地傳送 [**PGM \_ SETCHILD**](pgm-setchild.md) 訊息。 <br/> |
| [**呼機 \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | 設定呼機控制項的滾動位置。 您可以使用此宏，或明確地傳送 [**PGM \_ SETPOS**](pgm-setpos.md) 訊息。 <br/>                                                                                                                                                                                                                                                                                       |
| [**呼機 \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **適用于內部用途;不建議在應用程式中使用。**<br/> 設定分頁控制項的滾動參數，包括超時值、每個超時的行數，以及每行的圖元。 您可以使用此宏，或明確地傳送 [**PGM \_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) 訊息。 <br/>                                                                                                  |



 

### <a name="messages"></a>訊息



| 主題                                              | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PGM \_ FORWARDMOUSE**](pgm-forwardmouse.md)      | 啟用或停用呼機控制項的滑鼠轉送。 啟用滑鼠轉寄時，分頁控制項會將 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息轉送至包含的視窗。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) 宏。 <br/>                                                                                                                       |
| [**PGM \_ GETBKCOLOR**](pgm-getbkcolor.md)          | 抓取呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) 宏。 <br/>                                                                                                                                                                                                                                                                   |
| [**PGM \_ GETBORDER**](pgm-getborder.md)            | 抓取呼機控制項目前的框線大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) 宏。 <br/>                                                                                                                                                                                                                                                                          |
| [**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)    | 抓取頁面導航控制項目前的按鈕大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) 宏。 <br/>                                                                                                                                                                                                                                                                  |
| [**PGM \_ GETBUTTONSTATE**](pgm-getbuttonstate.md)  | 抓取頁面導航控制項中指定之按鈕的狀態。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) 宏。 <br/>                                                                                                                                                                                                                                                         |
| [**PGM \_ GETDROPTARGET**](pgm-getdroptarget.md)    | 抓取呼機控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 介面指標。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) 宏。 <br/>                                                                                                                                                                                                                                         |
| [**PGM \_ GETPOS**](pgm-getpos.md)                  | 抓取呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) 宏。 <br/>                                                                                                                                                                                                                                                                             |
| [**PGM \_ RECALCSIZE**](pgm-recalcsize.md)          | 強制呼機控制項重新計算包含視窗的大小。 傳送此訊息將會產生 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) 宏。 <br/>                                                                                                                                                      |
| [**PGM \_ SETBKCOLOR**](pgm-setbkcolor.md)          | 設定呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) 宏。 <br/>                                                                                                                                                                                                                                                                        |
| [**PGM \_ SETBORDER**](pgm-setborder.md)            | 設定呼機控制項的目前框線大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) 宏。 <br/>                                                                                                                                                                                                                                                                               |
| [**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)    | 設定呼機控制項目前的按鈕大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) 宏。 <br/>                                                                                                                                                                                                                                                                       |
| [**PGM \_ SETCHILD**](pgm-setchild.md)              | 設定呼機控制項的包含視窗。 此訊息不會變更包含視窗的父系;它只會將視窗控制碼指派給呼機控制項以供滾動。 在大部分的情況下，包含的視窗將會是子視窗。 如果是這種情況，則包含的視窗應該是呼機控制項的子系。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) 宏。 <br/> |
| [**PGM \_ SETPOS**](pgm-setpos.md)                  | 設定呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) 宏。 <br/>                                                                                                                                                                                                                                                                                 |
| [**PGM \_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) | **適用于內部用途;不建議在應用程式中使用。**<br/> 設定分頁控制項的滾動參數，包括超時值、每個超時的行數，以及每行的圖元。 您可以明確地傳送此訊息，或使用 [ [**呼叫器 \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) 宏]。 <br/>                                                                                                  |



 

### <a name="notifications"></a>通知



| 主題                                                        | 目錄                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (的呼叫器) ](nm-releasedcapture-pager-.md) | 通知頁面控制項的父視窗，控制項已放開滑鼠捕捉。 NM \_ RELEASEDCAPTURE 是以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | 由分頁控制項傳送的通知，可取得所包含視窗的可滾動維度。 這些維度是由分頁控制項用來判斷所包含視窗的可滾動大小。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | 當熱 (反白顯示) 專案變更時，由呼機控制項傳送。 <br/>                                                                                                                                                                                                                               |
| [PGN \_ 捲軸](pgn-scroll.md)                                | 在要滾動包含的視窗之前，由呼機控制項所傳送的通知。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                         |



 

### <a name="structures"></a>結構



| 主題                                | 目錄                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | 包含和接收頁面控制用來計算內含視窗之可捲動區域的資訊。 它會搭配 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知一起使用。 <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | 包含 [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md) 通知所使用的資訊。 <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | 包含和接收分頁控制項在滾動包含的視窗時所使用的資訊。 它會搭配 [PGN \_ 滾動](pgn-scroll.md) 通知一起使用。 <br/>                          |



 

### <a name="constants"></a>常數



| 主題                                            | 目錄                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [呼機控制項樣式](pager-control-styles.md) | 此區段會列出建立呼機控制項時使用的視窗樣式。 <br/> |



 

 

