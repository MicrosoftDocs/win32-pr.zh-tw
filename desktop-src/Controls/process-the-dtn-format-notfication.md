---
title: 如何處理 DTN_FORMAT 通知
description: 本主題示範如何處理日期和時間選擇器所傳送的格式通知， (DTP) 控制項。
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842895"
---
# <a name="how-to-process-the-dtn_format-notification"></a>如何處理 DTN \_ 格式通知

本主題示範如何處理日期和時間選擇器所傳送的格式通知， (DTP) 控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


DTP 控制項會傳送 [DTN \_ 格式](dtn-format.md) 通知，要求將顯示在控制項回呼欄位中的文字。 您的應用程式必須處理此通知，才能讓 DTP 控制項顯示原本不支援的資訊。

下列 c + + 程式碼範例是應用程式定義的函式 (**DoFormat**) ，藉由提供回呼欄位的文字字串來處理 [DTN \_ 格式](dtn-format.md) 的通知碼。 應用程式會呼叫 **GetDayNum** 應用程式定義的函式，以要求要在回呼字串中使用的天數。


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



**GetDayNum 應用程式定義函數**

應用程式定義的範例函式 **DoFormat** 會呼叫下列 **GetDayNum** 應用程式定義的函式，以根據目前的日期來要求日期號碼。 **GetDayNum** 會傳回 **整數值，代表一年** 中的目前日期，從0到366。 在處理期間，此函式會呼叫另一個應用程式定義的函數 **IsLeapYr**。


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



**IsLeapYr 應用程式定義函數**

應用程式定義函數 **GetDayNum** 會呼叫 **IsLeapYr** 函數來判斷目前年份是否為閏年。 **IsLeapYr** 會傳回 **布林** 值，如果它是閏年份，則為 **TRUE** ，否則為 **FALSE** 。


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
}        
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用日期時間選擇器控制項](using-date-and-time-picker.md)
</dt> <dt>

[日期和時間選擇器控制項參考](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[日期和時間選擇器](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




