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
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="25887-103">如何處理 DTN \_ 格式通知</span><span class="sxs-lookup"><span data-stu-id="25887-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="25887-104">本主題示範如何處理日期和時間選擇器所傳送的格式通知， (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="25887-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="25887-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="25887-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="25887-106">技術</span><span class="sxs-lookup"><span data-stu-id="25887-106">Technologies</span></span>

-   [<span data-ttu-id="25887-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="25887-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="25887-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="25887-108">Prerequisites</span></span>

-   <span data-ttu-id="25887-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="25887-109">C/C++</span></span>
-   <span data-ttu-id="25887-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="25887-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="25887-111">指示</span><span class="sxs-lookup"><span data-stu-id="25887-111">Instructions</span></span>


<span data-ttu-id="25887-112">DTP 控制項會傳送 [DTN \_ 格式](dtn-format.md) 通知，要求將顯示在控制項回呼欄位中的文字。</span><span class="sxs-lookup"><span data-stu-id="25887-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="25887-113">您的應用程式必須處理此通知，才能讓 DTP 控制項顯示原本不支援的資訊。</span><span class="sxs-lookup"><span data-stu-id="25887-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="25887-114">下列 c + + 程式碼範例是應用程式定義的函式 (**DoFormat**) ，藉由提供回呼欄位的文字字串來處理 [DTN \_ 格式](dtn-format.md) 的通知碼。</span><span class="sxs-lookup"><span data-stu-id="25887-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="25887-115">應用程式會呼叫 **GetDayNum** 應用程式定義的函式，以要求要在回呼字串中使用的天數。</span><span class="sxs-lookup"><span data-stu-id="25887-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


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



<span data-ttu-id="25887-116">**GetDayNum 應用程式定義函數**</span><span class="sxs-lookup"><span data-stu-id="25887-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="25887-117">應用程式定義的範例函式 **DoFormat** 會呼叫下列 **GetDayNum** 應用程式定義的函式，以根據目前的日期來要求日期號碼。</span><span class="sxs-lookup"><span data-stu-id="25887-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="25887-118">**GetDayNum** 會傳回 **整數值，代表一年** 中的目前日期，從0到366。</span><span class="sxs-lookup"><span data-stu-id="25887-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="25887-119">在處理期間，此函式會呼叫另一個應用程式定義的函數 **IsLeapYr**。</span><span class="sxs-lookup"><span data-stu-id="25887-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


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



<span data-ttu-id="25887-120">**IsLeapYr 應用程式定義函數**</span><span class="sxs-lookup"><span data-stu-id="25887-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="25887-121">應用程式定義函數 **GetDayNum** 會呼叫 **IsLeapYr** 函數來判斷目前年份是否為閏年。</span><span class="sxs-lookup"><span data-stu-id="25887-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="25887-122">**IsLeapYr** 會傳回 **布林** 值，如果它是閏年份，則為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="25887-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="25887-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="25887-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25887-124">使用日期時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="25887-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="25887-125">日期和時間選擇器控制項參考</span><span class="sxs-lookup"><span data-stu-id="25887-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="25887-126">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="25887-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




