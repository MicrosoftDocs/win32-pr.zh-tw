---
title: 月曆控制項
description: 本章節包含與月曆控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\monthcal\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ba999b48e99e75c7137064a1e8cd563235ac54
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945951"
---
# <a name="month-calendar-control"></a>月曆控制項

本章節包含與月曆控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                                              | 目錄                                                                                |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [關於 Month Calendar 控制項](month-calendar-controls.md)       | 月曆控制項會實行類似行事曆的使用者介面。<br/>          |
| [使用月曆控制項](using-month-calendar-controls.md) | 本節提供有關程式設計月曆控制項的資訊。<br/> |



 

### <a name="macros"></a>巨集



| 主題                                                                 | 目錄                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MonthCal \_ GetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarborder)     | 取得月曆控制項的框線大小（以圖元為單位）。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETCALENDARBORDER**](mcm-getcalendarborder.md) 訊息。<br/>                                                                                                                           |
| [**MonthCal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount)       | 取得目前在行事曆控制項中顯示的行事歷數目。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETCALENDARCOUNT**](mcm-getcalendarcount.md) 訊息。<br/>                                                                                                                 |
| [**MonthCal \_ GetCalendarGridInfo**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendargridinfo) | 取得行事曆方格的相關資訊。<br/>                                                                                                                                                                                                                                                                |
| [**MonthCal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid)                       | 取得指定月曆控制項的目前行事曆識別碼。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETCALID**](mcm-getcalid.md) 訊息。<br/>                                                                                                                                              |
| [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor)                       | 抓取月曆控制項指定部分的色彩。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETCOLOR**](mcm-getcolor.md) 訊息。 <br/>                                                                                                                                     |
| [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview)           | 取得月曆控制項的視圖。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETCURRENTVIEW**](mcm-getcurrentview.md) 訊息。<br/>                                                                                                                                                   |
| [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel)                     | 抓取目前選取的日期。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETCURSEL**](mcm-getcursel.md) 訊息。 <br/>                                                                                                                                                                 |
| [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek)     | 抓取月曆控制項的每週第一天。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETFIRSTDAYOFWEEK**](mcm-getfirstdayofweek.md) 訊息。 <br/>                                                                                                                      |
| [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount)           | 抓取月曆控制項中可選取的最大日期範圍。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETMAXSELCOUNT**](mcm-getmaxselcount.md) 訊息。 <br/>                                                                                                           |
| [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth)       | 抓取月曆控制項中 "today" 字串的最大寬度。 這包括標籤文字和日期文字。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) 訊息。 <br/>                                                           |
| [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect)             | 抓取在月曆控制項中顯示全月所需的最小大小。 大小資訊會以 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構的形式呈現。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETMINREQRECT**](mcm-getminreqrect.md) 訊息。 <br/>                        |
| [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta)             | 抓取月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETMONTHDELTA**](mcm-getmonthdelta.md) 訊息。 <br/>                       |
| [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange)             | 使用代表月曆控制項顯示之最高和最低限制的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構) ，抓取日期資訊 (。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETMONTHRANGE**](mcm-getmonthrange.md) 訊息。 <br/>                             |
| [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange)                       | 抓取月曆控制項設定的最小和最大允許日期。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETRANGE**](mcm-getrange.md) 訊息。 <br/>                                                                                                                      |
| [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange)                 | 抓取代表使用者目前所選取日期範圍上限和下限的日期資訊。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETSELRANGE**](mcm-getselrange.md) 訊息。 <br/>                                                                            |
| [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday)                       | 針對月曆控制項的日期，抓取指定為 "today" 的日期資訊。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETTODAY**](mcm-gettoday.md) 訊息。 <br/>                                                                                                           |
| [**MonthCal \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat)       | 抓取控制項的 Unicode 字元格式旗標。 您可以使用這個宏，或明確地傳送 [**MCM \_ GETUNICODEFORMAT**](mcm-getunicodeformat.md) 訊息。 <br/>                                                                                                                             |
| [**MonthCal \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest)                         | 判斷月曆控制項的哪個部分位於螢幕上的指定點。 您可以使用這個宏，或明確地傳送 [**MCM \_ system.windows.media.visualtreehelper.hittest**](mcm-hittest.md) 訊息。 <br/>                                                                                                                    |
| [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder)     | 設定月曆控制項的框線大小（以圖元為單位）。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETCALENDARBORDER**](mcm-setcalendarborder.md) 訊息。<br/>                                                                                                                           |
| [**MonthCal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid)                       | 設定給定行事曆控制項的行事曆識別碼。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETCALID**](mcm-setcalid.md) 訊息。<br/>                                                                                                                                                      |
| [**MonthCal \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor)                       | 設定月曆控制項指定部分的色彩。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETCOLOR**](mcm-setcolor.md) 訊息。 <br/>                                                                                                                                          |
| [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview)           | 設定月曆控制項的視圖。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETCURRENTVIEW**](mcm-setcurrentview.md) 訊息。<br/>                                                                                                                                                   |
| [**MonthCal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel)                     | 針對月曆控制項設定目前選取的日期。 如果指定的日期不在 view 中，控制項會更新顯示，使其變成可供觀看。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETCURSEL**](mcm-setcursel.md) 訊息。 <br/>                                            |
| [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate)                 | 設定當月月曆控制項中目前可見的所有月份的日期狀態。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) 訊息。 <br/>                                                                                                     |
| [**MonthCal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek)     | 設定月曆控制項的每週第一天。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETFIRSTDAYOFWEEK**](mcm-setfirstdayofweek.md) 訊息。 <br/>                                                                                                                           |
| [**MonthCal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount)           | 設定可在月曆控制項中選取的最大天數。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) 訊息。 <br/>                                                                                                            |
| [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta)             | 設定月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) 訊息。 <br/>                            |
| [**MonthCal \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange)                       | 設定月曆控制項的最小和最大允許日期。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETRANGE**](mcm-setrange.md) 訊息。 <br/>                                                                                                                               |
| [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange)                 | 將月曆控制項的選取範圍設定為指定的日期範圍。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETSELRANGE**](mcm-setselrange.md) 訊息。 <br/>                                                                                                                             |
| [**MonthCal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday)                       | 設定月曆控制項的 "today" 選項。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETTODAY**](mcm-settoday.md) 訊息。 <br/>                                                                                                                                                 |
| [**MonthCal \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat)       | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以使用這個宏，或明確地傳送 [**MCM \_ SETUNICODEFORMAT**](mcm-setunicodeformat.md) 訊息。 <br/> |
| [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin)             | 計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。 您可以使用這個宏，或明確地傳送 [**MCM \_ SIZERECTTOMIN**](mcm-sizerecttomin.md) 訊息。<br/>                                  |



 

### <a name="messages"></a>訊息



| 主題                                                       | 目錄                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ GETCALENDARBORDER**](mcm-getcalendarborder.md)     | 取得框線的大小（以圖元為單位）。 您可以使用 [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) 宏明確地傳送此訊息。<br/>                                                                                                                                                  |
| [**MCM \_ GETCALENDARCOUNT**](mcm-getcalendarcount.md)       | 取得目前在行事曆控制項中顯示的行事歷數目。 您可以使用 [**MonthCal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) 宏明確地傳送此訊息。<br/>                                                                                                            |
| [**MCM \_ GETCALENDARGRIDINFO**](mcm-getcalendargridinfo.md) | 取得行事曆方格的相關資訊。<br/>                                                                                                                                                                                                                                                                          |
| [**MCM \_ GETCALID**](mcm-getcalid.md)                       | 取得指定月曆控制項的行事曆識別碼。 您可以使用 [**MonthCal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) 宏明確地傳送此訊息。<br/>                                                                                                                                                 |
| [**MCM \_ GETCOLOR**](mcm-getcolor.md)                       | 抓取月曆控制項指定部分的色彩。 您可以使用 [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) 宏明確地傳送此訊息。 <br/>                                                                                                                                |
| [**MCM \_ GETCURRENTVIEW**](mcm-getcurrentview.md)           | 取得行事曆的目前視圖。 您可以使用 [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) 宏明確地傳送此訊息。<br/>                                                                                                                                                   |
| [**MCM \_ GETCURSEL**](mcm-getcursel.md)                     | 抓取目前選取的日期。 您可以使用 [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) 宏明確地傳送此訊息。 <br/>                                                                                                                                                            |
| [**MCM \_ GETFIRSTDAYOFWEEK**](mcm-getfirstdayofweek.md)     | 抓取月曆控制項的每週第一天。 您可以使用 [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) 宏明確地傳送此訊息。 <br/>                                                                                                                 |
| [**MCM \_ GETMAXSELCOUNT**](mcm-getmaxselcount.md)           | 抓取月曆控制項中可選取的最大日期範圍。 您可以使用 [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) 宏明確地傳送此訊息。 <br/>                                                                                                      |
| [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md)       | 抓取月曆控制項中 "today" 字串的最大寬度。 這包括標籤文字和日期文字。 您可以使用 [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) 宏明確地傳送此訊息。 <br/>                                                      |
| [**MCM \_ GETMINREQRECT**](mcm-getminreqrect.md)             | 抓取在月曆控制項中顯示全月所需的最小大小。 您可以使用 [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) 宏明確地傳送此訊息。 <br/>                                                                                                  |
| [**MCM \_ GETMONTHDELTA**](mcm-getmonthdelta.md)             | 抓取月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) 宏明確地傳送此訊息。 <br/>                  |
| [**MCM \_ GETMONTHRANGE**](mcm-getmonthrange.md)             | 使用代表月曆控制項顯示之最高和最低限制的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構) ，抓取日期資訊 (。 您可以使用 [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) 宏明確地傳送此訊息。 <br/>                        |
| [**MCM \_ GETRANGE**](mcm-getrange.md)                       | 抓取月曆控制項設定的最小和最大允許日期。 您可以使用 [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) 宏明確地傳送此訊息。 <br/>                                                                                                                 |
| [**MCM \_ GETSELRANGE**](mcm-getselrange.md)                 | 抓取代表使用者目前所選取日期範圍上限和下限的日期資訊。 您可以使用 [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) 宏明確地傳送此訊息。 <br/>                                                                       |
| [**MCM \_ GETTODAY**](mcm-gettoday.md)                       | 針對月曆控制項的日期，抓取指定為 "today" 的日期資訊。 您可以使用 [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) 宏明確地傳送此訊息。 <br/>                                                                                                      |
| [**MCM \_ GETUNICODEFORMAT**](mcm-getunicodeformat.md)       | 抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 [**MonthCal \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) 宏。 <br/>                                                                                                                             |
| [**MCM \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**](mcm-hittest.md)                         | 判斷月曆控制項的哪個部分位於螢幕上的指定點。 您可以使用 [**MonthCal \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) 宏明確地傳送此訊息。 <br/>                                                                                                               |
| [**MCM \_ SETCALENDARBORDER**](mcm-setcalendarborder.md)     | 設定框線的大小（以圖元為單位）。 您可以使用 [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) 宏明確地傳送此訊息。<br/>                                                                                                                                                  |
| [**MCM \_ SETCALID**](mcm-setcalid.md)                       | 設定給定行事曆控制項的行事曆識別碼。 您可以使用 [**MonthCal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) 宏明確地傳送此訊息。<br/>                                                                                                                                                 |
| [**MCM \_ SETCOLOR**](mcm-setcolor.md)                       | 設定月曆控制項指定部分的色彩。 您可以使用 [**MonthCal \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) 宏明確地傳送此訊息。 <br/>                                                                                                                                     |
| [**MCM \_ SETCURRENTVIEW**](mcm-setcurrentview.md)           | 設定行事曆的目前視圖。 您可以使用 [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) 宏明確地傳送此訊息。<br/>                                                                                                                                                   |
| [**MCM \_ SETCURSEL**](mcm-setcursel.md)                     | 針對月曆控制項設定目前選取的日期。 如果指定的日期不在 view 中，控制項會更新顯示，使其變成可供觀看。 您可以使用 [**MonthCal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) 宏明確地傳送此訊息。 <br/>                                       |
| [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md)                 | 設定當月月曆控制項中目前可見的所有月份的日期狀態。 您可以使用 [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) 宏明確地傳送此訊息。 <br/>                                                                                                |
| [**MCM \_ SETFIRSTDAYOFWEEK**](mcm-setfirstdayofweek.md)     | 設定月曆控制項的每週第一天。 您可以使用 [**MonthCal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) 宏明確地傳送此訊息。 <br/>                                                                                                                      |
| [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md)           | 設定可在月曆控制項中選取的最大天數。 您可以使用 [**MonthCal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) 宏明確地傳送此訊息。 <br/>                                                                                                       |
| [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md)             | 設定月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) 宏明確地傳送此訊息。 <br/>                       |
| [**MCM \_ SETRANGE**](mcm-setrange.md)                       | 設定月曆控制項的最小和最大允許日期。 您可以使用 [**MonthCal \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) 宏明確地傳送此訊息。 <br/>                                                                                                                          |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md)                 | 將月曆控制項的選取範圍設定為指定的日期範圍。 您可以使用 [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) 宏明確地傳送此訊息。 <br/>                                                                                                                        |
| [**MCM \_ SETTODAY**](mcm-settoday.md)                       | 設定月曆控制項的 "today" 選項。 您可以使用 [**MonthCal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) 宏明確地傳送此訊息。 <br/>                                                                                                                                            |
| [**MCM \_ SETUNICODEFORMAT**](mcm-setunicodeformat.md)       | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以明確地傳送此訊息，或使用 [**MonthCal \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) 宏。 <br/> |
| [**MCM \_ SIZERECTTOMIN**](mcm-sizerecttomin.md)             | 計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。 您可以使用 [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) 宏明確地傳送此訊息。<br/>                             |



 

### <a name="notifications"></a>通知



| 主題                                                              | 目錄                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MCN \_ GETDAYSTATE](mcn-getdaystate.md)                            | 由月曆控制項傳送，可要求有關如何顯示個別日期的資訊。 此通知碼只會由使用 [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) 樣式的月曆控制項來傳送，而且會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [MCN \_ SELCHANGE](mcn-selchange.md)                                | 月曆控制項在目前選取日期或日期範圍變更時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                  |
| [MCN \_ SELECT](mcn-select.md)                                      | 當使用者在月曆控制項中做出明確的日期選取時，由月曆控制項傳送。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                   |
| [MCN \_ VIEWCHANGE](mcn-viewchange.md)                              | 由月曆控制項在目前的視圖變更時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                                                                |
| [NM \_ RELEASEDCAPTURE (monthcal) ](nm-releasedcapture-monthcal-.md) | 通知 monthcal 控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                           |



 

### <a name="structures"></a>結構



| 主題                                  | 目錄                                                                                                                                                                                                                                                           |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo)       | 包含行事曆控制項部分的相關資訊。<br/>                                                                                                                                                                                                  |
| [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) | 攜帶月曆控制項的點擊測試點特定資訊。 此結構會搭配 [**MCM \_ system.windows.media.visualtreehelper.hittest**](mcm-hittest.md) 訊息和對應的 [**MonthCal \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) 宏使用。 <br/>                |
| [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate)       | 攜帶處理 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知碼所需的資訊。 此結構的所有成員都是用於輸入，除了 **prgDayState** 之外，接收應用程式必須在處理 MCN \_ GETDAYSTATE 時設定。 <br/> |
| [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange)     | 攜帶處理 [MCN \_ SELCHANGE](mcn-selchange.md) 通知碼所需的資訊。 <br/>                                                                                                                                                     |
| [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange)   | 儲存處理 [MCN \_ VIEWCHANGE](mcn-viewchange.md) 通知程式碼所需的資訊。<br/>                                                                                                                                                     |



 

### <a name="constants"></a>常數



| 主題                                                              | 目錄                                                                                  |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [月曆控制項樣式](month-calendar-control-styles.md) | 當建立月曆控制項時，會使用下列樣式常數。 <br/> |



 

### <a name="data-types"></a>資料類型



| 主題                                  | 目錄                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**MONTHDAYSTATE**](monthdaystate.md) | **MONTHDAYSTATE** 資料型別是保存每個月各天狀態的位位。<br/> |



 

 

