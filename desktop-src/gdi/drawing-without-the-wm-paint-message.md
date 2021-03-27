---
description: 雖然應用程式會在執行 WM 油漆訊息時執行大部分的繪圖作業，但是在 \_ 不依賴 WM 油漆訊息的情況下，應用程式通常會更有效率地在視窗中直接繪製 \_ 。
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: 沒有 WM_PAINT 訊息的繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66695e85b700de6f62366dedb6fe082f410d4385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848555"
---
# <a name="drawing-without-the-wm_paint-message"></a><span data-ttu-id="9ca8a-103">不含 WM \_ 油漆訊息的繪圖</span><span class="sxs-lookup"><span data-stu-id="9ca8a-103">Drawing Without the WM\_PAINT Message</span></span>

<span data-ttu-id="9ca8a-104">雖然應用程式會在執行 [**WM \_ 油漆**](wm-paint.md) 訊息時執行大部分的繪圖作業，但是在不依賴 **WM \_ 油漆** 訊息的情況下，應用程式通常會更有效率地在視窗中直接繪製。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-104">Although applications carry out most drawing operations while the [**WM\_PAINT**](wm-paint.md) message is processing, it is sometimes more efficient for an application to draw directly in a window without relying on the **WM\_PAINT** message.</span></span> <span data-ttu-id="9ca8a-105">當使用者需要立即意見反應時（例如選取文字和拖曳或調整物件大小時），這會很有用。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-105">This can be useful when the user needs immediate feedback, such as when selecting text and dragging or sizing an object.</span></span> <span data-ttu-id="9ca8a-106">在這種情況下，應用程式通常會在處理鍵盤或滑鼠訊息時繪製。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-106">In such cases, the application usually draws while processing keyboard or mouse messages.</span></span>

<span data-ttu-id="9ca8a-107">若要在視窗中繪製，而不使用 [**WM \_ 油漆**](wm-paint.md) 訊息，應用程式會使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來取得視窗的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-107">To draw in a window without using a [**WM\_PAINT**](wm-paint.md) message, the application uses the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function to retrieve a display device context for the window.</span></span> <span data-ttu-id="9ca8a-108">使用顯示裝置內容時，應用程式可以在視窗中繪製，並避免侵到其他視窗。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-108">With the display device context, the application can draw in the window and avoid intruding into other windows.</span></span> <span data-ttu-id="9ca8a-109">當應用程式完成繪圖時，它會呼叫 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放顯示裝置內容，以供其他應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-109">When the application has finished drawing, it calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context for use by other applications.</span></span>

<span data-ttu-id="9ca8a-110">在不使用 [**WM \_ 油漆**](wm-paint.md) 訊息的情況下繪製時，應用程式通常不會使視窗失效。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-110">When drawing without using a [**WM\_PAINT**](wm-paint.md) message, the application usually does not invalidate the window.</span></span> <span data-ttu-id="9ca8a-111">相反地，它會以方便您還原視窗和移除繪圖的方式進行繪製。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-111">Instead, it draws in such a fashion that it can easily restore the window and remove the drawing.</span></span> <span data-ttu-id="9ca8a-112">例如，當使用者選取文字或物件時，應用程式通常會藉由反轉視窗中已有的專案來繪製選取專案。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-112">For example, when the user selects text or an object, the application typically draws the selection by inverting whatever is already in the window.</span></span> <span data-ttu-id="9ca8a-113">應用程式可以移除選取專案，並還原視窗的原始內容，只要再次反轉就可以了。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-113">The application can remove the selection and restore the original contents of the window by simply inverting again.</span></span>

<span data-ttu-id="9ca8a-114">應用程式會負責仔細管理它對視窗所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-114">The application is responsible for carefully managing any changes it makes to the window.</span></span> <span data-ttu-id="9ca8a-115">尤其是，如果應用程式繪製選取專案，並出現中間的 [**WM \_ 油漆**](wm-paint.md) 訊息，應用程式必須確保在訊息期間完成的任何繪製都不會損毀選取專案。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-115">In particular, if an application draws a selection and an intervening [**WM\_PAINT**](wm-paint.md) message occurs, the application must ensure that any drawing done during the message does not corrupt the selection.</span></span> <span data-ttu-id="9ca8a-116">為了避免這種情況，許多應用程式會移除選取專案、執行一般繪圖作業，然後在繪圖完成時還原選取專案。</span><span class="sxs-lookup"><span data-stu-id="9ca8a-116">To avoid this, many applications remove the selection, carry out usual drawing operations, and then restore the selection when drawing is complete.</span></span>

 

 



