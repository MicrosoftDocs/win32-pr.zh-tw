---
title: 使用 Low-Level 監視設定函數
description: 使用 Low-Level 監視設定函數
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- 監視，函數
- 監視，低層級設定功能
- 監視器、DDC/CI
- 監視，顯示資料通道命令介面
- 監視設定、低層級設定功能
- 監視設定，函數
- 監視設定、DDC/CI
- 監視設定，顯示資料通道命令介面
- 低層級設定函數
- 顯示資料通道命令介面
- DDC/CI
- " (MCCS) 的 VESA 監視器控制命令集"
- '監視控制命令集 (MCCS) '
- 'MCCS (監視器控制命令集) '
- '虛擬主控台 (VCP) '
- 'VCP (虛擬主控台) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933183"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="10c6d-119">使用 Low-Level 監視設定函數</span><span class="sxs-lookup"><span data-stu-id="10c6d-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="10c6d-120">使用低層級的監視設定功能之前，您應該先熟悉這些標準：</span><span class="sxs-lookup"><span data-stu-id="10c6d-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="10c6d-121">顯示資料通道命令介面 (DDC/CI) </span><span class="sxs-lookup"><span data-stu-id="10c6d-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="10c6d-122"> (MCCS) 的 VESA 監視器控制命令集</span><span class="sxs-lookup"><span data-stu-id="10c6d-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="10c6d-123">低層級函式的運作方式是取得並設定虛擬主控台 (VCP) 代碼的值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="10c6d-124">VCP 程式碼可以是 *連續* 或 *noncontinuous*。</span><span class="sxs-lookup"><span data-stu-id="10c6d-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="10c6d-125">連續的代碼可以假設零和廠商專屬的最大值之間的任何值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="10c6d-126">Noncontinuous 代碼支援一組已定義的值，也就是廠商專屬的值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="10c6d-127">若要使用低層級的監視設定函數，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="10c6d-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="10c6d-128">藉由呼叫 [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors)或 [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)來取得 **HMONITOR** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="10c6d-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="10c6d-129">呼叫 [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) 以取得與 **HMONITOR** 控制碼相關聯的實體監視器數目。</span><span class="sxs-lookup"><span data-stu-id="10c6d-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="10c6d-130">呼叫 [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) 以取得實體監視器的控制碼清單。</span><span class="sxs-lookup"><span data-stu-id="10c6d-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="10c6d-131">呼叫 [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) 以取得監視器之 DDC/CI 功能字串的長度。</span><span class="sxs-lookup"><span data-stu-id="10c6d-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="10c6d-132">功能字串是包含監視靜態資訊的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="10c6d-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="10c6d-133">字串的其中一個部分會列出監視器支援的 VCP 碼。</span><span class="sxs-lookup"><span data-stu-id="10c6d-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="10c6d-134">此字串也會列出支援的 noncontinuous VCP 代碼值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="10c6d-135">配置緩衝區來保存功能字串，並呼叫 [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) 來取得字串。</span><span class="sxs-lookup"><span data-stu-id="10c6d-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="10c6d-136">剖析功能字串，以判斷監視器支援哪些 VCP 碼。</span><span class="sxs-lookup"><span data-stu-id="10c6d-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="10c6d-137">針對連續的 VCP 程式碼，呼叫 [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) 以取得程式碼的目前和最大值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="10c6d-138">針對 noncontinuous VCP 程式碼，剖析功能字串以取得支援的值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="10c6d-139">呼叫 [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) 以設定 VCP 碼的新值。</span><span class="sxs-lookup"><span data-stu-id="10c6d-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10c6d-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="10c6d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10c6d-141">**使用監視設定**</span><span class="sxs-lookup"><span data-stu-id="10c6d-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 