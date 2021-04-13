---
title: 桌面視窗管理員
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300775"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="ee0c0-103">桌面視窗管理員</span><span class="sxs-lookup"><span data-stu-id="ee0c0-103">The Desktop Window Manager</span></span>

<span data-ttu-id="ee0c0-104">在 Windows Vista 之前，Windows 程式會直接在螢幕上繪製。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="ee0c0-105">換句話說，程式會直接寫入視訊卡所顯示的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="ee0c0-106">如果視窗沒有正確地重新繪製，則這種方法可能會造成視覺構件。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="ee0c0-107">比方說，如果使用者將一個視窗拖曳到另一個視窗，而且下一個視窗無法迅速重新繪製，最上層的視窗就會留下一個線索：</span><span class="sxs-lookup"><span data-stu-id="ee0c0-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![顯示重新繪製構件的螢幕擷取畫面。](images/graphics04.png)

<span data-ttu-id="ee0c0-109">原因是這兩個 windows 繪製至相同的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="ee0c0-110">拖曳最上方的視窗時，必須重新繪製其下的視窗。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="ee0c0-111">如果重新繪製的速度太慢，則會導致上圖所示的構件。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="ee0c0-112">Windows Vista 藉由引進桌面視窗管理員 (DWM) 來徹底改變 windows 的繪製方式。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="ee0c0-113">當 DWM 啟用時，視窗不會再直接繪製到顯示緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="ee0c0-114">相反地，每個視窗會繪製到螢幕上的記憶體緩衝區，也稱為 *螢幕外介面*。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="ee0c0-115">DWM 接著會將這些介面合成至螢幕。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-115">The DWM then composites these surfaces to the screen.</span></span>

![顯示 dwm 如何將桌面合成的圖表。](images/graphics05.png)

<span data-ttu-id="ee0c0-117">DWM 提供許多優於舊版圖形架構的優點。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="ee0c0-118">減少重新繪製訊息。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-118">Fewer repaint messages.</span></span> <span data-ttu-id="ee0c0-119">當視窗被另一個視窗阻擋時，受阻礙的視窗就不需要重新繪製。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="ee0c0-120">專案減少。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-120">Reduced artifacts.</span></span> <span data-ttu-id="ee0c0-121">先前，拖曳視窗可以建立視覺構件，如所述。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="ee0c0-122">視覺效果。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-122">Visual effects.</span></span> <span data-ttu-id="ee0c0-123">因為 DWM 負責撰寫螢幕，所以它可以轉譯半透明和模糊的視窗區域。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="ee0c0-124">高 DPI 的自動調整。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="ee0c0-125">雖然調整不是處理高 DPI 的理想方式，但這是較舊的應用程式（不是針對高 DPI 設定所設計）的可行回復。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="ee0c0-126"> (我們稍後會在 [DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)一節中返回此主題。 ) </span><span class="sxs-lookup"><span data-stu-id="ee0c0-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="ee0c0-127">替代的視圖。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-127">Alternative views.</span></span> <span data-ttu-id="ee0c0-128">DWM 可以用各種有趣的方式來使用螢幕外表面。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="ee0c0-129">例如，DWM 是 Windows Flip 3D、縮圖和動畫轉換背後的技術。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="ee0c0-130">不過請注意，不保證會啟用 DWM。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="ee0c0-131">圖形配接器可能不支援 DWM 系統需求，使用者可以透過 [ **系統屬性** ] 控制台停用 dwm。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="ee0c0-132">這表示您的程式不應依賴 DWM 的重新繪製行為。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="ee0c0-133">使用已停用的 DWM 測試您的程式，以確定它會正確地重新繪製。</span><span class="sxs-lookup"><span data-stu-id="ee0c0-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="ee0c0-134">下一個</span><span class="sxs-lookup"><span data-stu-id="ee0c0-134">Next</span></span>

[<span data-ttu-id="ee0c0-135">保留模式與立即模式</span><span class="sxs-lookup"><span data-stu-id="ee0c0-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




