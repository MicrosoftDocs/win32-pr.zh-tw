---
title: 日期和時間選擇器
description: 本章節包含與日期和時間選擇器控制項搭配使用之 API 元素的相關資訊。
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4e91b325b798ff465d8048cac2f0a9a72e5774
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842811"
---
# <a name="date-and-time-picker"></a>日期和時間選擇器

本章節包含與日期和時間選擇器控制項搭配使用之 API 元素的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                                                    | 目錄                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於日期和時間選擇器控制項](date-and-time-picker-controls.md) | *日期和時間選擇器 (DTP) 控制項* 提供簡單且直覺的介面，可讓您用來與使用者交換日期和時間資訊。<br/> |
| [使用日期時間選擇器控制項](using-date-and-time-picker.md)    | 本節提供用來執行日期和時間選擇器控制項的資訊和範例程式碼。 <br/>                                                |



 

### <a name="macros"></a>巨集



| 主題                                                                     | 目錄                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | 關閉 (DTP) 控制項的日期和時間選擇器。 使用這個宏或明確地傳送 [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md) 訊息。<br/>                                                                                                                     |
| [**DateTime \_ GetDateTimePickerInfo**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | 取得指定日期和時間選擇器 (DTP) 控制項的資訊。<br/>                                                                                                                                                                                              |
| [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | 取得在不剪切的情況下顯示控制項所需的大小。 使用這個宏或明確地傳送 [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md) 訊息。<br/>                                                                                                        |
| [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | 取得日期和時間選擇器的 (DTP) 子月曆控制項的控制碼。 您可以使用此宏，或明確地傳送 [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) 訊息。 <br/>                                                                               |
| [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | 取得日期和時間選擇器中的月曆指定部分的色彩， (DTP) 控制項。 您可以使用此宏，或明確地傳送 [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md) 訊息。 <br/>                                                           |
| [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | 取得日期和時間選擇器 (DTP) 控制項的子月曆控制項目前使用的字型。 您可以使用此宏，或明確地傳送 [**DTM \_ GETMCFONT**](dtm-getmcfont.md) 訊息。 <br/>                                                      |
| [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | 取得指定之 DTP 控制項的樣式。 使用這個宏或明確地傳送 [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md) 訊息。<br/>                                                                                                                               |
| [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | 取得日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以使用這個宏，或明確地傳送 [**DTM \_ GETRANGE**](dtm-getrange.md) 訊息。 <br/>                                                              |
| [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | 從日期和時間選擇器取得目前選取的時間 (DTP) 控制項，並將它放在指定的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構中。 您可以使用這個宏，或明確地傳送 [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md) 訊息。 <br/> |
| [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | 根據指定的格式字串，設定日期和時間選擇器的顯示 (DTP) 控制項。 您可以使用此宏，或明確地傳送 [**DTM \_ SETFORMAT**](dtm-setformat.md) 訊息。 <br/>                                                                          |
| [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | 在日期和時間選擇器中，設定日曆指定部分的色彩， (DTP) 控制項。 您可以使用此宏，或明確地傳送 [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md) 訊息。 <br/>                                                           |
| [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | 設定日期和時間選擇器 (DTP) 控制項的子月曆控制項所使用的字型。 您可以使用此宏或明確地傳送 [**DTM \_ SETMCFONT**](dtm-setmcfont.md) 訊息。 <br/>                                                                |
| [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | 設定指定之 DTP 控制項的樣式。 使用這個宏或明確地傳送 [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md) 訊息。<br/>                                                                                                                              |
| [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | 設定日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以使用這個宏，或明確地傳送 [**DTM \_ SETRANGE**](dtm-setrange.md) 訊息。 <br/>                                                                       |
| [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | 設定日期和時間選擇器 (DTP) 控制項設定為指定的日期和時間。 您可以使用此宏，或明確地傳送 [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息。 <br/>                                                                                       |



 

### <a name="messages"></a>訊息



| 主題                                                           | 目錄                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md)                 | 關閉 DTP 控制項。 請明確地傳送此訊息，或使用 [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) 宏。<br/>                                                                                                                                        |
| [**DTM \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | 取得 (DTP) 控制項之日期和時間選擇器的資訊。<br/>                                                                                                                                                                                                                  |
| [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | 取得在不剪切的情況下顯示控制項所需的大小。 請明確地傳送此訊息，或使用 [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) 宏。<br/>                                                                                                  |
| [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md)                       | 取得日期和時間選擇器中的月曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) 宏。 <br/>                                              |
| [**DTM \_ GETMCFONT**](dtm-getmcfont.md)                         | 取得日期和時間選擇器 (DTP) 控制項的子月曆控制項目前使用的字型。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) 宏。 <br/>                                         |
| [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | 取得 DTP 控制項的樣式。 請明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) 宏。<br/>                                                                                                                       |
| [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | 取得日期和時間選擇器的 (DTP) 子月曆控制項的控制碼。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) 宏。 <br/>                                                                              |
| [**DTM \_ GETRANGE**](dtm-getrange.md)                           | 取得日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) 宏。 <br/>                                                              |
| [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md)                 | 從日期和時間選擇器取得目前選取的時間 (DTP) 控制項，並將它放在指定的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構中。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) 宏。 <br/> |
| [**DTM \_ SETFORMAT**](dtm-setformat.md)                         | 根據指定的格式字串，設定日期和時間選擇器的顯示 (DTP) 控制項。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) 宏。 <br/>                                                                         |
| [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md)                       | 在日期和時間選擇器中，設定日曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) 宏。 <br/>                                              |
| [**DTM \_ SETMCFONT**](dtm-setmcfont.md)                         | 設定日期和時間選擇器 (DTP) 控制項的子月曆控制項所使用的字型。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) 宏。<br/>                                                    |
| [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md)                       | 設定 DTP 控制項的樣式。 請明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) 宏。<br/>                                                                                                                       |
| [**DTM \_ SETRANGE**](dtm-setrange.md)                           | 設定日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) 宏。 <br/>                                                                      |
| [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | 設定日期和時間選擇器 (DTP) 控制項的時間。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) 宏。 <br/>                                                                                                   |



 

### <a name="notifications"></a>通知



| 主題                                                   | 目錄                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ 特寫](dtn-closeup.md)                         | 由日期和時間選擇器所傳送 (DTP) 控制使用者何時關閉下拉式月曆。 當使用者選擇月曆中的日期，或在行事曆開啟時按一下下拉箭號時，就會關閉月曆。 <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | 每次發生變更時，日期和時間選擇器都會傳送 (的 DTP) 控制。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                                                  |
| [DTN \_ 下拉式清單](dtn-dropdown.md)                       | 當使用者啟動下拉式月曆時，日期和時間選擇器會傳送 (DTP) 控制。 <br/>                                                                                                                                                                                                                                               |
| [DTN \_ 格式](dtn-format.md)                           | 由日期和時間選擇器所傳送 (DTP) 控制項，要求在回呼欄位中顯示文字。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | 由日期和時間選擇器所傳送 (DTP) 控制項，以取得將顯示在回呼欄位中之字串的允許大小上限。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | 當使用者完成編輯控制項中的字串時，日期和時間選擇器會傳送 (DTP) 控制項。 只有設定為 [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) 樣式的 DTP 控制項才會傳送此通知碼。 這則訊息會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)                     | 當使用者在回呼欄位中輸入時，日期和時間選擇器會傳送 (DTP) 控制項。 這則訊息會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (日期時間) ](nm-killfocus-date-time.md) | 通知日期和時間選擇器控制項的父視窗，表示控制項已遺失輸入焦點。 [**NM \_KILLFOCUS (日期時間)**](nm-killfocus-date-time.md) 會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                 |
| [NM \_ SETFOCUS (日期時間) ](nm-setfocus-date-time-.md)  | 通知日期和時間選擇器控制項的父視窗，控制項已收到輸入焦點。 [NM \_SETFOCUS (日期時間)](nm-setfocus-date-time-.md) 會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                  |



 

### <a name="structures"></a>結構



| 主題                                                  | 目錄                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | 包含有關 DTP 控制項的資訊。 <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | 包含在日期和時間選擇器中發生之變更的相關資訊 (DTP) 控制項。 此結構會與 [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) 通知程式碼搭配使用。 <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | 包含部分格式字串的相關資訊，此字串會定義日期和時間選擇器中的回呼欄位， (DTP) 控制項。 它會攜帶定義回呼欄位的子字串，並包含緩衝區來接收將顯示在回呼欄位中的字串。 此結構會搭配 [DTN \_ 格式](dtn-format.md) 通知碼使用。 <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | 包含日期和時間選擇器 (DTP) 控制項回呼欄位的相關資訊。 它包含的子字串 (取自訂回呼欄位的控制項格式字串) 。 結構會接收將在回呼欄位中顯示之文字的允許大小上限。 此結構會與 [DTN \_ FORMATQUERY](dtn-formatquery.md) 通知程式碼搭配使用。 <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | 包含在日期和時間選擇器中進行的編輯作業的特定資訊 (DTP) 控制項。 此訊息可搭配 [DTN \_ USERSTRING](dtn-userstring.md) 通知碼使用。 <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | 攜帶用來描述和處理 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知碼的資訊。 <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>常數



| 主題                                                                          | 目錄                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [日期和時間選擇器控制項樣式](date-and-time-picker-control-styles.md) | 此處所列的視窗樣式是日期和時間選擇器控制項特有的樣式。<br/> |



 

 

