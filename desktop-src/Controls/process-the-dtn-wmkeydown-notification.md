---
title: 如何處理 DTN_WMKEYDOWN 通知
description: 本主題將示範如何處理 DTN \_ WMKEYDOWN 通知。 處理此通知程式碼可讓控制項的擁有者在控制項的回呼欄位內提供對按鍵的特定回應。
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842908"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="ba44f-104">如何處理 DTN \_ WMKEYDOWN 通知</span><span class="sxs-lookup"><span data-stu-id="ba44f-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="ba44f-105">本主題將示範如何處理 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="ba44f-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="ba44f-106">處理此通知程式碼可讓控制項的擁有者在控制項的回呼欄位內提供對按鍵的特定回應。</span><span class="sxs-lookup"><span data-stu-id="ba44f-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ba44f-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="ba44f-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ba44f-108">技術</span><span class="sxs-lookup"><span data-stu-id="ba44f-108">Technologies</span></span>

-   [<span data-ttu-id="ba44f-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="ba44f-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ba44f-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="ba44f-110">Prerequisites</span></span>

-   <span data-ttu-id="ba44f-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ba44f-111">C/C++</span></span>
-   <span data-ttu-id="ba44f-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="ba44f-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ba44f-113">指示</span><span class="sxs-lookup"><span data-stu-id="ba44f-113">Instructions</span></span>


<span data-ttu-id="ba44f-114">日期和時間選擇器 (DTP) 控制項傳送 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 訊息，以報告使用者已在回呼欄位中輸入輸入。</span><span class="sxs-lookup"><span data-stu-id="ba44f-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="ba44f-115">如果您想要模擬標準 DTP 欄位所支援的相同鍵盤回應，或提供自訂回應，您的應用程式必須包含程式碼來處理此通知。</span><span class="sxs-lookup"><span data-stu-id="ba44f-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="ba44f-116">下列 c + + 程式碼範例是應用程式定義的函數，可處理 [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="ba44f-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="ba44f-117">**安全性警告：** 不當使用 **lstrcmp** 可能會危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="ba44f-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="ba44f-118">例如，在下列程式碼範例中呼叫 **lstrcmp** 之前，您應該確定兩個字串是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="ba44f-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="ba44f-119">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="ba44f-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="ba44f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba44f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba44f-121">使用日期時間選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="ba44f-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="ba44f-122">日期和時間選擇器控制項參考</span><span class="sxs-lookup"><span data-stu-id="ba44f-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ba44f-123">日期和時間選擇器</span><span class="sxs-lookup"><span data-stu-id="ba44f-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




