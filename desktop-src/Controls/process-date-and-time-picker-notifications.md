---
title: 如何處理日期和時間選擇器通知
description: 本節示範如何處理日期和時間選擇器的通知。
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b904c464677a81151b03e3ae89085847e4e8bdf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024359"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="a2a74-103">如何處理日期和時間選擇器通知</span><span class="sxs-lookup"><span data-stu-id="a2a74-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="a2a74-104">本節示範如何處理日期和時間選擇器的通知。</span><span class="sxs-lookup"><span data-stu-id="a2a74-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a2a74-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="a2a74-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a2a74-106">技術</span><span class="sxs-lookup"><span data-stu-id="a2a74-106">Technologies</span></span>

-   [<span data-ttu-id="a2a74-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="a2a74-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a2a74-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="a2a74-108">Prerequisites</span></span>

-   <span data-ttu-id="a2a74-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a2a74-109">C/C++</span></span>
-   <span data-ttu-id="a2a74-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="a2a74-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a2a74-111">指示</span><span class="sxs-lookup"><span data-stu-id="a2a74-111">Instructions</span></span>


<span data-ttu-id="a2a74-112">日期和時間選擇器 () 控制項會在控制項中發生事件（通常是由使用者輸入觸發）時，將通知訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="a2a74-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="a2a74-113">您的應用程式必須包含程式碼，以判斷通知訊息的類型並適當地回應。</span><span class="sxs-lookup"><span data-stu-id="a2a74-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="a2a74-114">如果您打算在應用程式中搭配使用回呼欄位與 DTP 控制項，您必須準備好處理 [DTN \_ FORMATQUERY](dtn-formatquery.md)、 [DTN \_ 格式](dtn-format.md)和 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="a2a74-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="a2a74-115">如需回呼欄位的詳細資訊，請參閱 [回呼欄位](date-and-time-picker-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="a2a74-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="a2a74-116">下列 c + + 程式碼範例會識別由 DTP 控制項所傳送的通知訊息，並呼叫適當的應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="a2a74-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="a2a74-117">請參閱下列主題中的程式碼範例，以瞭解如何處理此範例中所顯示的通知。</span><span class="sxs-lookup"><span data-stu-id="a2a74-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2a74-118">如何處理 DTN \_ DATETIMECHANGE 通知</span><span class="sxs-lookup"><span data-stu-id="a2a74-118">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="a2a74-119">如何處理 DTN \_ FORMATQUERY 通知</span><span class="sxs-lookup"><span data-stu-id="a2a74-119">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="a2a74-120">如何處理 DTN \_ 格式通知</span><span class="sxs-lookup"><span data-stu-id="a2a74-120">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="a2a74-121">如何處理 DTN \_ WMKEYDOWN 通知</span><span class="sxs-lookup"><span data-stu-id="a2a74-121">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="a2a74-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2a74-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2a74-123">日期和時間選擇器通知</span><span class="sxs-lookup"><span data-stu-id="a2a74-123">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="a2a74-124">日期和時間選擇器控制項參考</span><span class="sxs-lookup"><span data-stu-id="a2a74-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a2a74-125">使用日期時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="a2a74-125">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="a2a74-126">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="a2a74-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




