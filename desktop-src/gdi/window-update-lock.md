---
description: 視窗更新鎖定是在視窗中繪製的暫時暫停。
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: 視窗更新鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192387"
---
# <a name="window-update-lock"></a><span data-ttu-id="2b481-103">視窗更新鎖定</span><span class="sxs-lookup"><span data-stu-id="2b481-103">Window Update Lock</span></span>

<span data-ttu-id="2b481-104">*視窗更新鎖定* 是在視窗中繪製的暫時暫停。</span><span class="sxs-lookup"><span data-stu-id="2b481-104">A *window update lock* is a temporary suspension of drawing in a window.</span></span> <span data-ttu-id="2b481-105">當使用者移動或調整視窗大小時，系統會使用鎖定來防止其他視窗在追蹤矩形上繪製。</span><span class="sxs-lookup"><span data-stu-id="2b481-105">The system uses the lock to prevent other windows from drawing over the tracking rectangle whenever the user moves or sizes a window.</span></span> <span data-ttu-id="2b481-106">如果應用程式使用自己的視窗執行類似的移動或調整大小作業，則可以使用鎖定來防止繪圖。</span><span class="sxs-lookup"><span data-stu-id="2b481-106">Applications can use the lock to prevent drawing if they carry out similar moving or sizing operations with their own windows.</span></span>

<span data-ttu-id="2b481-107">應用程式會使用 [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) 函數來設定或清除視窗更新鎖定，並指定要鎖定的視窗。</span><span class="sxs-lookup"><span data-stu-id="2b481-107">An application uses the [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) function to set or clear a window update lock, specifying the window to lock.</span></span> <span data-ttu-id="2b481-108">鎖定會套用至指定的視窗及其所有子視窗。</span><span class="sxs-lookup"><span data-stu-id="2b481-108">The lock applies to the specified window and all of its child windows.</span></span> <span data-ttu-id="2b481-109">設定鎖定時， [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 和 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式會傳回具有空白可見區域的顯示裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2b481-109">When the lock is set, the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) and [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) functions return a display device context with a visible region that is empty.</span></span> <span data-ttu-id="2b481-110">在此情況下，應用程式可以繼續在視窗中繪製，但是會裁剪所有輸出。</span><span class="sxs-lookup"><span data-stu-id="2b481-110">Given this, the application can continue to draw in the window, but all output is clipped.</span></span> <span data-ttu-id="2b481-111">鎖定會持續存在，直到應用程式透過呼叫 **LockWindowUpdate** 來清除它，並為視窗指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2b481-111">The lock persists until the application clears it by calling **LockWindowUpdate**, specifying **NULL** for the window.</span></span> <span data-ttu-id="2b481-112">雖然 **LockWindowUpdate** 會強制視窗的可見區域是空的，但函式不會讓指定的視窗變成隱藏的，也不會清除 WS \_ 可見的樣式位。</span><span class="sxs-lookup"><span data-stu-id="2b481-112">Although **LockWindowUpdate** forces a window's visible region to be empty, the function does not make the specified window invisible and does not clear the WS\_VISIBLE style bit.</span></span>

<span data-ttu-id="2b481-113">設定鎖定之後，應用程式可以使用 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式（具有 DCX \_ LOCKWINDOWUPDATE 值）來取得顯示裝置內容，以在鎖定的視窗上繪製。</span><span class="sxs-lookup"><span data-stu-id="2b481-113">After the lock is set, the application can use the [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, with the DCX\_LOCKWINDOWUPDATE value, to retrieve a display device context to draw over the locked window.</span></span> <span data-ttu-id="2b481-114">這可讓應用程式在處理鍵盤或滑鼠訊息時繪製追蹤矩形。</span><span class="sxs-lookup"><span data-stu-id="2b481-114">This allows the application to draw a tracking rectangle when processing keyboard or mouse messages.</span></span> <span data-ttu-id="2b481-115">當使用者移動和調整視窗大小時，系統就會使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="2b481-115">The system uses this method when the user moves and sizes windows.</span></span> <span data-ttu-id="2b481-116">**GetDCEx** 會從顯示裝置內容快取抓取顯示裝置內容，因此應用程式必須在繪圖之後儘快釋放裝置內容。</span><span class="sxs-lookup"><span data-stu-id="2b481-116">**GetDCEx** retrieves the display device context from the display device context cache, so the application must release the device context as soon as possible after drawing.</span></span>

<span data-ttu-id="2b481-117">設定視窗更新鎖定時，系統會為每個鎖定視窗建立累積的周框。</span><span class="sxs-lookup"><span data-stu-id="2b481-117">While a window update lock is set, the system creates an accumulated bounding rectangle for each locked window.</span></span> <span data-ttu-id="2b481-118">清除鎖定時，系統會使用此周框來設定視窗和其子視窗的更新區域，強制執行最終的 [**WM \_ 繪製**](wm-paint.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="2b481-118">When the lock is cleared, the system uses this bounding rectangle to set the update region for the window and its child windows, forcing an eventual [**WM\_PAINT**](wm-paint.md) message.</span></span> <span data-ttu-id="2b481-119">如果累積的周框是空的 (也就是，如果) 設定鎖定時發生繪圖，則不會設定更新區域。</span><span class="sxs-lookup"><span data-stu-id="2b481-119">If the accumulated bounding rectangle is empty (that is, if no drawing has occurred while the lock was set), the update region is not set.</span></span>

 

 



