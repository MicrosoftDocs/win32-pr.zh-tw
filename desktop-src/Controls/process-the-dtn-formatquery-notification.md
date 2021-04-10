---
title: 如何處理 DTN_FORMATQUERY 通知
description: 本主題示範如何處理日期和時間選擇器所傳送的格式查詢通知， (DTP) 控制項。
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933750"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="31393-103">如何處理 DTN \_ FORMATQUERY 通知</span><span class="sxs-lookup"><span data-stu-id="31393-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="31393-104">本主題示範如何處理日期和時間選擇器所傳送的格式查詢通知， (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="31393-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="31393-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="31393-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="31393-106">技術</span><span class="sxs-lookup"><span data-stu-id="31393-106">Technologies</span></span>

-   [<span data-ttu-id="31393-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="31393-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="31393-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="31393-108">Prerequisites</span></span>

-   <span data-ttu-id="31393-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="31393-109">C/C++</span></span>
-   <span data-ttu-id="31393-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="31393-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="31393-111">指示</span><span class="sxs-lookup"><span data-stu-id="31393-111">Instructions</span></span>


<span data-ttu-id="31393-112">DTP 控制項會傳送 [DTN \_ FORMATQUERY](dtn-formatquery.md) 通知碼，以要求控制項內回呼欄位的最大可能大小的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="31393-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="31393-113">您的應用程式必須處理此訊息，以確保所有欄位都能正確顯示。</span><span class="sxs-lookup"><span data-stu-id="31393-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="31393-114">下列 c + + 程式碼範例是應用程式定義的函式，它會藉由計算指定回呼欄位最大可能字串的寬度，來處理 [DTN \_ FORMATQUERY](dtn-formatquery.md) 通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="31393-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="31393-115">**安全性警告：** 不當使用 **lstrcmp** 可能會危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="31393-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="31393-116">例如，在下列程式碼範例中呼叫 **lstrcmp** 之前，您應該確定兩個字串是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="31393-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="31393-117">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="31393-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
}
```



## <a name="related-topics"></a><span data-ttu-id="31393-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="31393-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31393-119">使用日期時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="31393-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="31393-120">日期和時間選擇器控制項參考</span><span class="sxs-lookup"><span data-stu-id="31393-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="31393-121">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="31393-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




