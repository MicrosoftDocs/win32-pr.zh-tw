---
description: 除了更新區域之外，每個視窗都有一個可見區域，可定義使用者可見的視窗部分。
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: 視窗區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027138"
---
# <a name="window-regions"></a><span data-ttu-id="9ef26-103">視窗區域</span><span class="sxs-lookup"><span data-stu-id="9ef26-103">Window Regions</span></span>

<span data-ttu-id="9ef26-104">除了更新區域之外，每個視窗都有一個 *可見區域* ，可定義使用者可見的視窗部分。</span><span class="sxs-lookup"><span data-stu-id="9ef26-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="9ef26-105">只要視窗變更大小，或每次移動另一個視窗時，系統就會變更視窗的可見區域，使其遮蔽或公開視窗的一部分。</span><span class="sxs-lookup"><span data-stu-id="9ef26-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="9ef26-106">應用程式無法直接變更可見區域，但是系統會自動使用可見區域來建立針對視窗所抓取之任何顯示裝置內容的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="9ef26-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="9ef26-107">*裁剪區域* 會決定系統允許繪圖的位置。</span><span class="sxs-lookup"><span data-stu-id="9ef26-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="9ef26-108">當應用程式使用 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)、 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來抓取顯示裝置內容時，系統會將裝置內容的裁剪區域設定為可見區域和更新區域的交集。</span><span class="sxs-lookup"><span data-stu-id="9ef26-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="9ef26-109">應用程式可以使用 [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)、 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) 和 [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)等函式來變更裁剪區域，以進一步將繪圖限制為更新區域的特定部分。</span><span class="sxs-lookup"><span data-stu-id="9ef26-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="9ef26-110">WS \_ CLIPCHILDREN 和 ws \_ CLIPSIBLINGS 樣式會進一步指定系統如何計算視窗的可見區域。</span><span class="sxs-lookup"><span data-stu-id="9ef26-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="9ef26-111">如果視窗有一或兩個樣式，則可見區域會排除具有相同父視窗) 的任何子視窗或同級視窗 (視窗。</span><span class="sxs-lookup"><span data-stu-id="9ef26-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="9ef26-112">因此，在這些視窗中 intrude 的繪圖一律會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="9ef26-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 



