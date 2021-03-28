---
description: 應用程式會在不同的時間繪製視窗：當您在第一次建立視窗時、變更視窗的大小時、將視窗從另一個視窗移至最小化或最大化時、從開啟的檔案顯示資料，以及滾動、變更或選取部分顯示的資料時。
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: 在視窗中繪製的時機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42c8c157de5a591be5ad1a6ad3e319cf83220e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319031"
---
# <a name="when-to-draw-in-a-window"></a><span data-ttu-id="23702-103">在視窗中繪製的時機</span><span class="sxs-lookup"><span data-stu-id="23702-103">When to Draw in a Window</span></span>

<span data-ttu-id="23702-104">應用程式會在不同的時間繪製視窗：當您在第一次建立視窗時、變更視窗的大小時、將視窗從另一個視窗移至最小化或最大化時、從開啟的檔案顯示資料，以及滾動、變更或選取部分顯示的資料時。</span><span class="sxs-lookup"><span data-stu-id="23702-104">An application draws in a window at a variety of times: when first creating a window, when changing the size of the window, when moving the window from behind another window, when minimizing or maximizing the window, when displaying data from an opened file, and when scrolling, changing, or selecting a portion of the displayed data.</span></span>

<span data-ttu-id="23702-105">系統會管理動作，例如移動和調整視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="23702-105">The system manages actions such as moving and sizing a window.</span></span> <span data-ttu-id="23702-106">如果動作會影響視窗的內容，系統會將視窗中受影響的部分標示為已準備好進行更新，並在下一個機會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="23702-106">If an action affects the content of the window, the system marks the affected portion of the window as ready for updating and, at the next opportunity, sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure of the window.</span></span> <span data-ttu-id="23702-107">此訊息是應用程式用來判斷必須更新的內容，以及執行必要繪圖的信號。</span><span class="sxs-lookup"><span data-stu-id="23702-107">The message is a signal to the application to determine what must be updated and to carry out the necessary drawing.</span></span>

<span data-ttu-id="23702-108">某些動作是由應用程式管理，例如顯示開啟的檔案和選取顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="23702-108">Some actions are managed by the application, such as displaying open files and selecting displayed data.</span></span> <span data-ttu-id="23702-109">針對這些動作，應用程式可以標示為更新受此動作影響的視窗部分，而導致在下一個機會傳送 [**WM \_ 油漆**](wm-paint.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="23702-109">For these actions, an application can mark for updating the portion of the window affected by the action, causing a [**WM\_PAINT**](wm-paint.md) message to be sent at the next opportunity.</span></span> <span data-ttu-id="23702-110">如果動作需要立即提出意見反應，應用程式可以在動作發生時進行繪製，而不需要等候 **WM \_ 油漆**。</span><span class="sxs-lookup"><span data-stu-id="23702-110">If an action requires immediate feedback, the application can draw while the action takes place, without waiting for **WM\_PAINT**.</span></span> <span data-ttu-id="23702-111">例如，一般應用程式會反白顯示使用者選取的區域，而不是等候下一個 **WM \_ 油漆** 訊息來更新區域。</span><span class="sxs-lookup"><span data-stu-id="23702-111">For example, a typical application highlights the area the user selects rather than waiting for the next **WM\_PAINT** message to update the area.</span></span>

<span data-ttu-id="23702-112">在所有情況下，應用程式只要建立，就可以在視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="23702-112">In all cases, an application can draw in a window as soon as it is created.</span></span> <span data-ttu-id="23702-113">若要在視窗中繪製，應用程式必須先取得視窗的顯示裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="23702-113">To draw in the window, the application must first retrieve a handle to a display device context for the window.</span></span> <span data-ttu-id="23702-114">在理想的情況下，應用程式會在處理 [**WM \_ 油漆**](wm-paint.md) 訊息時，執行大部分的繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="23702-114">Ideally, an application carries out most of its drawing operations during the processing of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="23702-115">在此情況下，應用程式會藉由呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式來抓取顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="23702-115">In this case, the application retrieves a display device context by calling the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function.</span></span> <span data-ttu-id="23702-116">如果應用程式在任何其他時間（例如從 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 內或在鍵盤或滑鼠訊息的處理期間）繪製，則會呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來取出顯示 DC。</span><span class="sxs-lookup"><span data-stu-id="23702-116">If an application draws at any other time, such as from within [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) or during the processing of keyboard or mouse messages, it calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function to retrieve the display DC.</span></span>

 

 
