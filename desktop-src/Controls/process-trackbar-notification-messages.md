---
title: 如何處理資訊提示通知訊息
description: Trackbars 會傳送一個 WM \_ HSCROLL 或 wm VSCROLL 訊息給父系，以通知其使用者動作的父視窗 \_ 。
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672204"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="06da9-103">如何處理資訊提示通知訊息</span><span class="sxs-lookup"><span data-stu-id="06da9-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="06da9-104">Trackbars 會傳送一個 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息給父系，以通知其使用者動作的父視窗。</span><span class="sxs-lookup"><span data-stu-id="06da9-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="06da9-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="06da9-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="06da9-106">技術</span><span class="sxs-lookup"><span data-stu-id="06da9-106">Technologies</span></span>

-   [<span data-ttu-id="06da9-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="06da9-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="06da9-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="06da9-108">Prerequisites</span></span>

-   <span data-ttu-id="06da9-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="06da9-109">C/C++</span></span>
-   <span data-ttu-id="06da9-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="06da9-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="06da9-111">指示</span><span class="sxs-lookup"><span data-stu-id="06da9-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="06da9-112">處理資訊提示通知訊息</span><span class="sxs-lookup"><span data-stu-id="06da9-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="06da9-113">下列程式碼範例是一種函式，會在執行程式碼段的父視窗收到 [**WM \_ HSCROLL**](wm-hscroll.md) 訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="06da9-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="06da9-114">此範例中的「 [**\_ ENABLESELRANGE**](trackbar-control-styles.md) 」樣式為「tb」。</span><span class="sxs-lookup"><span data-stu-id="06da9-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="06da9-115">滑杆的位置會與選取範圍進行比較，並在必要時，將滑杆移至選取範圍的開始或結束位置。</span><span class="sxs-lookup"><span data-stu-id="06da9-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="06da9-116">備註</span><span class="sxs-lookup"><span data-stu-id="06da9-116">Remarks</span></span>

<span data-ttu-id="06da9-117">包含 [**tb \_ 垂直**](trackbar-control-styles.md) 樣式的 [顯示] 的對話方塊，可以在接收到 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息時使用這個函式。</span><span class="sxs-lookup"><span data-stu-id="06da9-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06da9-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="06da9-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06da9-119">[使用 [使用] 控制項](using-trackbar-controls.md)</span><span class="sxs-lookup"><span data-stu-id="06da9-119">[Using Trackbar Controls](using-trackbar-controls.md)</span></span>
</dt> </dl>

 

 




