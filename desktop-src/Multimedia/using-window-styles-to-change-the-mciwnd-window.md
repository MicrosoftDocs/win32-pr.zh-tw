---
title: 使用視窗樣式變更 MCIWnd 視窗
description: 使用視窗樣式變更 MCIWnd 視窗
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967889"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="5235a-104">使用視窗樣式變更 MCIWnd 視窗</span><span class="sxs-lookup"><span data-stu-id="5235a-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="5235a-105">如同任何視窗，您可以從使用 [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) 函式指定的標準視窗樣式中進行選擇，以變更 MCIWnd 視窗的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="5235a-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="5235a-106">此外，您還可以從 MCIWnd 視窗特定的數個其他視窗樣式中選擇。</span><span class="sxs-lookup"><span data-stu-id="5235a-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="5235a-107">使用這些樣式，您的應用程式可以透過下列方式變更這些 MCIWnd 視窗：</span><span class="sxs-lookup"><span data-stu-id="5235a-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="5235a-108">變更視窗大小。</span><span class="sxs-lookup"><span data-stu-id="5235a-108">Change window size.</span></span>
-   <span data-ttu-id="5235a-109">隱藏或顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="5235a-109">Hide or display controls.</span></span>
-   <span data-ttu-id="5235a-110">發出通知訊息。</span><span class="sxs-lookup"><span data-stu-id="5235a-110">Issue notification messages.</span></span>
-   <span data-ttu-id="5235a-111">在標題列中顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="5235a-111">Display information in the title bar.</span></span>

<span data-ttu-id="5235a-112">您可以藉由在 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式中指定視窗樣式來設定視窗樣式，也可以使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏來變更現有 MCIWnd 視窗的樣式。</span><span class="sxs-lookup"><span data-stu-id="5235a-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="5235a-113">您也可以使用 [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) 宏，查詢其目前樣式的 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="5235a-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="5235a-114">如需 MCIWnd 特定視窗樣式的清單，請參閱 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)。</span><span class="sxs-lookup"><span data-stu-id="5235a-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 