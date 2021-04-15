---
title: 關於監視設定
description: 關於監視設定
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- 監視、關於
- 監視，色彩校正
- 監視，調整監視器顯示區域
- 監視，儲存監視設定
- 監視、還原監視設定
- 監視，廠商功能
- 色彩校正
- 調整監視器顯示區域
- 正在儲存監視設定
- 還原監視設定
- 廠商功能
- 監視設定，色彩校正
- 監視設定，關於
- 監視設定，調整監視器顯示區域
- 監視設定，儲存監視設定
- 監視設定、還原監視設定
- 監視設定、廠商功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507177"
---
# <a name="about-monitor-configuration"></a><span data-ttu-id="8e75d-120">關於監視設定</span><span class="sxs-lookup"><span data-stu-id="8e75d-120">About Monitor Configuration</span></span>

<span data-ttu-id="8e75d-121">監視設定功能的用途包括：</span><span class="sxs-lookup"><span data-stu-id="8e75d-121">Uses for the monitor configuration functions include:</span></span>

-   <span data-ttu-id="8e75d-122">色彩校正。</span><span class="sxs-lookup"><span data-stu-id="8e75d-122">Color calibration.</span></span> <span data-ttu-id="8e75d-123">正確校準的監視器會正確地重現色彩。</span><span class="sxs-lookup"><span data-stu-id="8e75d-123">A properly calibrated monitor reproduces colors correctly.</span></span> <span data-ttu-id="8e75d-124">色彩校正應用程式通常會顯示測試模式，並且具有可變更監視設定的控制項。</span><span class="sxs-lookup"><span data-stu-id="8e75d-124">Typically, a color calibration application displays a test pattern and has controls to change a monitor setting.</span></span> <span data-ttu-id="8e75d-125">使用者會變更設定，直到符合條件為止，然後針對每個監視設定重複此程式，直到校準監視器為止。</span><span class="sxs-lookup"><span data-stu-id="8e75d-125">The user changes the setting until a condition is met, and repeats this process for each monitor setting until the monitor is calibrated.</span></span>
-   <span data-ttu-id="8e75d-126">調整監視器的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="8e75d-126">Adjusting the monitor's display area.</span></span> <span data-ttu-id="8e75d-127">您可以使用監視設定功能來變更監視器顯示區域的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="8e75d-127">The monitor configuration functions can be used to change the size and position of a monitor's display area.</span></span> <span data-ttu-id="8e75d-128">例如，當 LCD 監視器使用類比連接器連接到電腦時，會在圖形配接器架構緩衝區中的圖元之間有一對一的對應，以及在 LCD 監視器上的圖元之間取得最佳影像品質。</span><span class="sxs-lookup"><span data-stu-id="8e75d-128">For example, when an LCD monitor is connected to a computer by using an analog connector, the best image quality is obtained when there is a one-to-one mapping between pixels in the graphics card's frame buffer and pixels on the LCD monitor.</span></span>
-   <span data-ttu-id="8e75d-129">正在儲存和還原監視設定。</span><span class="sxs-lookup"><span data-stu-id="8e75d-129">Saving and restoring monitor settings.</span></span> <span data-ttu-id="8e75d-130">有些使用者需要多組監視設定，因為不同的案例需要不同的監視設定。</span><span class="sxs-lookup"><span data-stu-id="8e75d-130">Some users need multiple sets of monitor settings, because different scenarios require different monitor settings.</span></span> <span data-ttu-id="8e75d-131">例如，針對桌面應用程式最理想的監視設定，不是觀看電視的最佳設定。</span><span class="sxs-lookup"><span data-stu-id="8e75d-131">For example, monitor settings that are optimal for desktop applications are not optimal for watching television.</span></span>
-   <span data-ttu-id="8e75d-132">使用廠商特定的監視器功能。</span><span class="sxs-lookup"><span data-stu-id="8e75d-132">Using vendor-specific monitor features.</span></span> <span data-ttu-id="8e75d-133">製造商可以使用監視設定功能來建立應用程式，以使用監視的廠商特定功能。</span><span class="sxs-lookup"><span data-stu-id="8e75d-133">Using the monitor configuration functions, manufacturers can create applications that use the vendor-specific features of the monitor.</span></span>

<span data-ttu-id="8e75d-134">監視設定函數分為高階層級和低層級的函式。</span><span class="sxs-lookup"><span data-stu-id="8e75d-134">The monitor configuration functions are divided into high-level and low-level functions.</span></span> <span data-ttu-id="8e75d-135">高階函式比低層級函數更容易使用。</span><span class="sxs-lookup"><span data-stu-id="8e75d-135">The high-level functions are easier to use than the low-level functions.</span></span> <span data-ttu-id="8e75d-136">若要使用高階函式，您不需要知道顯示資料通道命令介面 (DDC/CI) 的任何相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e75d-136">To use the high-level functions, you do not need to know anything about the Display Data Channel Command Interface (DDC/CI).</span></span> <span data-ttu-id="8e75d-137">不過，高階函式不會讓您存取監視的廠商特定功能。</span><span class="sxs-lookup"><span data-stu-id="8e75d-137">However, the high-level functions do not give you access to vendor-specific features of the monitor.</span></span>

<span data-ttu-id="8e75d-138">低層級函式是 DDC/CI 命令周圍的精簡型包裝函式。</span><span class="sxs-lookup"><span data-stu-id="8e75d-138">The low-level functions are a thin wrapper around the DDC/CI commands.</span></span> <span data-ttu-id="8e75d-139">若要使用低層級的函式，您必須熟悉 DDC/CI 標準，也必須使用 [VESA 監視器控制] 命令集 (MCCS) 標準。</span><span class="sxs-lookup"><span data-stu-id="8e75d-139">To use the low-level functions, you must be familiar with the DDC/CI standard and also with the VESA Monitor Control Command Set (MCCS) standard.</span></span> <span data-ttu-id="8e75d-140">一般而言，除非您只需要使用低層級函式中可用的功能，否則您應該使用高階函式。</span><span class="sxs-lookup"><span data-stu-id="8e75d-140">Generally, you should use the high-level functions unless you need to use features that are available only in the low-level functions.</span></span>

<span data-ttu-id="8e75d-141">高階監視設定功能的設計，是為了讓應用程式無法將監視器置於無法使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e75d-141">The high-level monitor configuration functions are designed so that an application cannot put a monitor into an unusable state.</span></span> <span data-ttu-id="8e75d-142">您可以使用低層級的函式，將 VCP 碼傳送給監視器。</span><span class="sxs-lookup"><span data-stu-id="8e75d-142">The low-level functions can be used to send VCP codes to the monitor.</span></span> <span data-ttu-id="8e75d-143">不過，請注意，有些 VCP 碼可以停用重要的功能，或讓監視進入使用者看不到顯示影像的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e75d-143">However, be aware that some VCP codes can disable important functionality or put the monitor into a state where the user cannot see the display image.</span></span> <span data-ttu-id="8e75d-144">如需詳細資訊，請參閱) standard (MCCS 的 [VESA 監視器控制] 命令集。</span><span class="sxs-lookup"><span data-stu-id="8e75d-144">For more information, see the VESA Monitor Control Command Set (MCCS) standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e75d-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e75d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e75d-146">監視設定</span><span class="sxs-lookup"><span data-stu-id="8e75d-146">Monitor Configuration</span></span>](monitor-configuration.md)
</dt> </dl>

 

 




