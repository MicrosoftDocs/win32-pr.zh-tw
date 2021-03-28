---
description: 當多個監視器是桌面的一部分時，物件可以在監視器之間順暢地移動。
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: 關於多顯示器監視器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5997e39768d01522ae1fdd2e976c611e67826350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972468"
---
# <a name="about-multiple-display-monitors"></a><span data-ttu-id="b8b87-103">關於多顯示器監視器</span><span class="sxs-lookup"><span data-stu-id="b8b87-103">About Multiple Display Monitors</span></span>

<span data-ttu-id="b8b87-104">當多個監視器是桌面的一部分時，物件可以在監視器之間順暢地移動。</span><span class="sxs-lookup"><span data-stu-id="b8b87-104">When multiple monitors are part of the desktop, objects can travel seamlessly between monitors.</span></span> <span data-ttu-id="b8b87-105">也就是說，您可以將視窗或快捷方式從某個監視器拖曳到另一個監視器，而您可以調整視窗的大小以涵蓋多個監視器。</span><span class="sxs-lookup"><span data-stu-id="b8b87-105">That is, you can drag windows or shortcuts from one monitor to another, and you can size windows to cover more than one monitor.</span></span> <span data-ttu-id="b8b87-106">此外，如果某個監視器安裝在另一個監視器之上，則離開上方監視器底部的游標會顯示在下方監視器的上方。</span><span class="sxs-lookup"><span data-stu-id="b8b87-106">Also, if one monitor is installed above another, a cursor that leaves the bottom of the upper monitor appears at the top of the lower monitor.</span></span>

<span data-ttu-id="b8b87-107">一般情況下，使用者會在系統中排列監視器，以反映實體顯示單位的相片順序;例如，並存或最上層的一或多個位置。</span><span class="sxs-lookup"><span data-stu-id="b8b87-107">Typically, a user arranges the monitors in the system to reflect the arrangement of the physical display units; for example, side-by-side or one-on-top-of-the-other.</span></span> <span data-ttu-id="b8b87-108">使用者會使用 [監視] 索引標籤來執行這項工作，這會透過主控台取代 **顯示內容** 對話方塊中的 [**設定**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="b8b87-108">The user does this with the Monitors tab, which replaces the **Settings** tab in the **Display Properties** dialog box through Control Panel.</span></span> <span data-ttu-id="b8b87-109">這些監視器必須形成一個連續的區域，也就是每個監視器至少會在一個邊緣的一部分上觸及另一個監視器。</span><span class="sxs-lookup"><span data-stu-id="b8b87-109">The monitors must form one contiguous region, that is, each monitor touches another monitor on at least part of one edge.</span></span>

<span data-ttu-id="b8b87-110">移動或調整視窗大小時，標題的部分一定會顯示出來，讓使用者可以使用滑鼠移動視窗並調整其大小。</span><span class="sxs-lookup"><span data-stu-id="b8b87-110">When a window is moved or resized, some part of the caption is always visible so the user can move and resize the window using the mouse.</span></span> <span data-ttu-id="b8b87-111">游標移動受限於監視器區域，因此一律為可見。</span><span class="sxs-lookup"><span data-stu-id="b8b87-111">Cursor movement is restricted to the area of the monitors, so it is always visible.</span></span> <span data-ttu-id="b8b87-112">Shell 圖示位於與工作列相同的監視器上，而工作列可以位於任何監視器上，請參閱 [舊版程式的多個監視器考慮](multiple-monitor-considerations-for-older-programs.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b87-112">Shell icons are positioned on the same monitor as the taskbar, and the taskbar can be on any monitor, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="b8b87-113">多個監視器系統會影響特定的按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="b8b87-113">A multiple monitor system affects certain key combinations.</span></span> <span data-ttu-id="b8b87-114">ALT + PRINTSCRN 按鍵組合會取得前景視窗的快照集，如同往常一樣。</span><span class="sxs-lookup"><span data-stu-id="b8b87-114">The ALT+PRINTSCRN key combination takes a snapshot of the foreground window, as always.</span></span> <span data-ttu-id="b8b87-115">但是，PRINTSCRN 鍵會取得具有滑鼠的監視器快照。</span><span class="sxs-lookup"><span data-stu-id="b8b87-115">However, the PRINTSCRN key takes a snapshot of the monitor that has the mouse.</span></span> <span data-ttu-id="b8b87-116">CTRL + PRINTSCRN 按鍵組合會取得整個虛擬畫面的快照集，請參閱 [虛擬螢幕](the-virtual-screen.md)。</span><span class="sxs-lookup"><span data-stu-id="b8b87-116">The CTRL+PRINTSCRN key combination takes a snapshot of the entire virtual screen, see [The Virtual Screen](the-virtual-screen.md).</span></span>

<span data-ttu-id="b8b87-117">對多個監視器的支援在單一顯示環境中執行時，不會影響應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="b8b87-117">The support for multiple monitors does not affect the performance of applications when running in a single display environment.</span></span> <span data-ttu-id="b8b87-118">也就是說，在單一顯示器系統上執行時，高效能圖形作業程式碼中不會有額外的負荷。</span><span class="sxs-lookup"><span data-stu-id="b8b87-118">That is, when running on a single display system, no additional overhead will be present in the high-performance graphics operations code.</span></span> <span data-ttu-id="b8b87-119">不過，在多個監視器系統中，如果應用程式只在其中一個圖形裝置上執行，效能會稍微受到影響。</span><span class="sxs-lookup"><span data-stu-id="b8b87-119">However, in a multiple monitor system, performance is slightly affected if an application runs only on one of the graphics devices.</span></span> <span data-ttu-id="b8b87-120">此外，如果應用程式跨越多個顯示器，效能可能會受到大幅影響，特別是針對需要大量圖形的作業。</span><span class="sxs-lookup"><span data-stu-id="b8b87-120">Also, performance may be greatly affected if an application spans multiple displays, especially for graphics-intensive operations.</span></span>

<span data-ttu-id="b8b87-121">*全螢幕* 是作業系統所提供的一項功能，可讓使用者將應用程式切換成特殊狀態，讓應用程式可以直接存取 VGA 圖形硬體。</span><span class="sxs-lookup"><span data-stu-id="b8b87-121">*Full-screen* is a feature provided by the operating system that allows a user to toggle an application into a special state where the application can access VGA graphics hardware directly.</span></span> <span data-ttu-id="b8b87-122">對於需要高效能的遊戲和其他以圖形為主的應用程式，這是一項重要的功能。</span><span class="sxs-lookup"><span data-stu-id="b8b87-122">This is a key feature for games and other graphics-focused applications that require high performance.</span></span> <span data-ttu-id="b8b87-123">此外，開發人員通常會使用它來進行文字編輯，因為它可讓文字滾動更快速。</span><span class="sxs-lookup"><span data-stu-id="b8b87-123">Also, it is often used by developers for text editing since it enables very fast text scrolling.</span></span>

<span data-ttu-id="b8b87-124">在多重監視器環境中，只有一個圖形裝置可與 VGA 相容。</span><span class="sxs-lookup"><span data-stu-id="b8b87-124">In a multiple monitor environment, only one graphics device can be VGA compatible.</span></span> <span data-ttu-id="b8b87-125">這是電腦硬體的限制，需要只有一部裝置回應任何硬體位址。</span><span class="sxs-lookup"><span data-stu-id="b8b87-125">This is a limitation of computer hardware which requires that only one device respond to any hardware address.</span></span> <span data-ttu-id="b8b87-126">因為 VGA 硬體相容性標準需要特定的硬體位址，電腦中只能有一個 VGA 圖形裝置，而且只有此裝置可以實際回應 VGA 位址。</span><span class="sxs-lookup"><span data-stu-id="b8b87-126">Because the VGA hardware compatibility standard requires specific hardware addresses, only one VGA graphics device can be present in a machine and only this device can physically respond to VGA addresses.</span></span> <span data-ttu-id="b8b87-127">因此，需要全螢幕的應用程式只會在支援 VGA 硬體相容性的特定裝置上執行。</span><span class="sxs-lookup"><span data-stu-id="b8b87-127">Thus, applications that require going full screen will only run on the particular device that supports VGA hardware compatibility.</span></span>

<span data-ttu-id="b8b87-128">本總覽提供下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b8b87-128">This overview provides information on the following topics.</span></span>

-   [<span data-ttu-id="b8b87-129">虛擬畫面</span><span class="sxs-lookup"><span data-stu-id="b8b87-129">The Virtual Screen</span></span>](the-virtual-screen.md)
-   [<span data-ttu-id="b8b87-130">HMONITOR 和裝置內容</span><span class="sxs-lookup"><span data-stu-id="b8b87-130">HMONITOR and the Device Context</span></span>](hmonitor-and-the-device-context.md)
-   [<span data-ttu-id="b8b87-131">列舉和顯示控制項</span><span class="sxs-lookup"><span data-stu-id="b8b87-131">Enumeration and Display Control</span></span>](enumeration-and-display-control.md)
-   [<span data-ttu-id="b8b87-132">多個監視系統計量</span><span class="sxs-lookup"><span data-stu-id="b8b87-132">Multiple Monitor System Metrics</span></span>](multiple-monitor-system-metrics.md)
-   [<span data-ttu-id="b8b87-133">使用多個監視器作為獨立顯示器</span><span class="sxs-lookup"><span data-stu-id="b8b87-133">Using Multiple Monitors as Independent Displays</span></span>](using-multiple-monitors-as-independent-displays.md)
-   [<span data-ttu-id="b8b87-134">多顯示器顯示器上的色彩</span><span class="sxs-lookup"><span data-stu-id="b8b87-134">Colors on Multiple Display Monitors</span></span>](colors-on-multiple-display-monitors.md)
-   [<span data-ttu-id="b8b87-135">將物件放置在多個顯示監視器上</span><span class="sxs-lookup"><span data-stu-id="b8b87-135">Positioning Objects on Multiple Display Monitors</span></span>](positioning-objects-on-multiple-display-monitors.md)
-   [<span data-ttu-id="b8b87-136">不同系統上的多個監視器應用程式</span><span class="sxs-lookup"><span data-stu-id="b8b87-136">Multiple Monitor Applications on Different Systems</span></span>](multiple-monitor-applications-on-different-systems.md)
-   [<span data-ttu-id="b8b87-137">舊版程式的多個監視器考慮</span><span class="sxs-lookup"><span data-stu-id="b8b87-137">Multiple Monitor Considerations for Older Programs</span></span>](multiple-monitor-considerations-for-older-programs.md)

 

 



