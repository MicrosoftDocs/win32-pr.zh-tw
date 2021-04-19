---
title: 監視設定函數
description: 監視設定函數
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- 監視，函數
- 監視，高階函數
- 監視，低層級函數
- 監視，列舉函數
- 高層級函數
- 低層級函數
- 列舉函數
- 監視設定，函數
- 監視設定、高階功能
- 監視設定、低層級功能
- 監視設定、列舉函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86925cd25912c17b8fb1bdd339888e5429de135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106980270"
---
# <a name="monitor-configuration-functions"></a><span data-ttu-id="57d15-114">監視設定函數</span><span class="sxs-lookup"><span data-stu-id="57d15-114">Monitor Configuration Functions</span></span>

<span data-ttu-id="57d15-115">下列函式是用來從監視取得資訊，以及變更監視的設定。</span><span class="sxs-lookup"><span data-stu-id="57d15-115">The following functions are used to get information from a monitor and to change a monitor's settings.</span></span> <span data-ttu-id="57d15-116">監視設定函數會分類為高階函式、低層級函式和列舉函數。</span><span class="sxs-lookup"><span data-stu-id="57d15-116">Monitor configuration functions are categorized into high-level functions, low-level functions, and enumeration functions.</span></span> <span data-ttu-id="57d15-117">如需詳細資訊，請參閱 [使用監視器](using-monitor-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="57d15-117">For more information, see [Using Monitor Configuration](using-monitor-configuration.md).</span></span>

## <a name="high-level-functions"></a><span data-ttu-id="57d15-118">High-Level 函式</span><span class="sxs-lookup"><span data-stu-id="57d15-118">High-Level Functions</span></span>



| <span data-ttu-id="57d15-119">函式</span><span class="sxs-lookup"><span data-stu-id="57d15-119">Function</span></span>                                                                         | <span data-ttu-id="57d15-120">描述</span><span class="sxs-lookup"><span data-stu-id="57d15-120">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="57d15-121">**DegaussMonitor**</span><span class="sxs-lookup"><span data-stu-id="57d15-121">**DegaussMonitor**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | <span data-ttu-id="57d15-122">Degausses 監視器。</span><span class="sxs-lookup"><span data-stu-id="57d15-122">Degausses a monitor.</span></span>                                                                 |
| [<span data-ttu-id="57d15-123">**GetMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="57d15-123">**GetMonitorBrightness**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | <span data-ttu-id="57d15-124">抓取監視器的最小值、最大值和目前的亮度設定。</span><span class="sxs-lookup"><span data-stu-id="57d15-124">Retrieves a monitor's minimum, maximum, and current brightness settings.</span></span>             |
| [<span data-ttu-id="57d15-125">**GetMonitorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="57d15-125">**GetMonitorCapabilities**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | <span data-ttu-id="57d15-126">抓取監視的設定功能。</span><span class="sxs-lookup"><span data-stu-id="57d15-126">Retrieves the configuration capabilities of a monitor.</span></span>                               |
| [<span data-ttu-id="57d15-127">**GetMonitorColorTemperature**</span><span class="sxs-lookup"><span data-stu-id="57d15-127">**GetMonitorColorTemperature**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | <span data-ttu-id="57d15-128">捕獲監視器目前的色溫。</span><span class="sxs-lookup"><span data-stu-id="57d15-128">Retrieves a monitor's current color temperature.</span></span>                                     |
| [<span data-ttu-id="57d15-129">**GetMonitorContrast**</span><span class="sxs-lookup"><span data-stu-id="57d15-129">**GetMonitorContrast**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | <span data-ttu-id="57d15-130">抓取監視器的最小值、最大值和目前的對比設定。</span><span class="sxs-lookup"><span data-stu-id="57d15-130">Retrieves a monitor's minimum, maximum, and current contrast settings.</span></span>               |
| [<span data-ttu-id="57d15-131">**GetMonitorDisplayAreaPosition**</span><span class="sxs-lookup"><span data-stu-id="57d15-131">**GetMonitorDisplayAreaPosition**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | <span data-ttu-id="57d15-132">抓取監視器的最小值、最大值和目前水準或垂直位置。</span><span class="sxs-lookup"><span data-stu-id="57d15-132">Retrieves a monitor's minimum, maximum, and current horizontal or vertical position.</span></span> |
| [<span data-ttu-id="57d15-133">**GetMonitorDisplayAreaSize**</span><span class="sxs-lookup"><span data-stu-id="57d15-133">**GetMonitorDisplayAreaSize**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | <span data-ttu-id="57d15-134">抓取監視器的最小值、最大值和目前的寬度或高度。</span><span class="sxs-lookup"><span data-stu-id="57d15-134">Retrieves a monitor's minimum, maximum, and current width or height.</span></span>                 |
| [<span data-ttu-id="57d15-135">**GetMonitorRedGreenOrBlueDrive**</span><span class="sxs-lookup"><span data-stu-id="57d15-135">**GetMonitorRedGreenOrBlueDrive**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | <span data-ttu-id="57d15-136">抓取監視的紅色、綠色或藍色的磁片磁碟機值。</span><span class="sxs-lookup"><span data-stu-id="57d15-136">Retrieves a monitor's red, green, or blue drive value.</span></span>                               |
| [<span data-ttu-id="57d15-137">**GetMonitorRedGreenOrBlueGain**</span><span class="sxs-lookup"><span data-stu-id="57d15-137">**GetMonitorRedGreenOrBlueGain**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | <span data-ttu-id="57d15-138">捕獲監視器的紅色、綠色或藍色增益值。</span><span class="sxs-lookup"><span data-stu-id="57d15-138">Retrieves a monitor's red, green, or blue gain value.</span></span>                                |
| [<span data-ttu-id="57d15-139">**GetMonitorTechnologyType**</span><span class="sxs-lookup"><span data-stu-id="57d15-139">**GetMonitorTechnologyType**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | <span data-ttu-id="57d15-140">抓取監視所使用的技術類型。</span><span class="sxs-lookup"><span data-stu-id="57d15-140">Retrieves the type of technology used by a monitor.</span></span>                                  |
| [<span data-ttu-id="57d15-141">**RestoreMonitorFactoryColorDefaults**</span><span class="sxs-lookup"><span data-stu-id="57d15-141">**RestoreMonitorFactoryColorDefaults**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | <span data-ttu-id="57d15-142">將監視的色彩設定還原為其原廠預設值。</span><span class="sxs-lookup"><span data-stu-id="57d15-142">Restores a monitor's color settings to their factory defaults.</span></span>                       |
| [<span data-ttu-id="57d15-143">**RestoreMonitorFactoryDefaults**</span><span class="sxs-lookup"><span data-stu-id="57d15-143">**RestoreMonitorFactoryDefaults**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | <span data-ttu-id="57d15-144">將監視的設定還原為其原廠預設值。</span><span class="sxs-lookup"><span data-stu-id="57d15-144">Restores a monitor's settings to their factory defaults.</span></span>                             |
| [<span data-ttu-id="57d15-145">**SaveCurrentMonitorSettings**</span><span class="sxs-lookup"><span data-stu-id="57d15-145">**SaveCurrentMonitorSettings**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | <span data-ttu-id="57d15-146">將目前的監視器設定儲存至顯示器的非動態儲存體。</span><span class="sxs-lookup"><span data-stu-id="57d15-146">Saves the current monitor settings to the display's nonvolatile storage.</span></span>             |
| [<span data-ttu-id="57d15-147">**SetMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="57d15-147">**SetMonitorBrightness**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | <span data-ttu-id="57d15-148">設定監視的亮度值。</span><span class="sxs-lookup"><span data-stu-id="57d15-148">Sets a monitor's brightness value.</span></span>                                                   |
| [<span data-ttu-id="57d15-149">**SetMonitorColorTemperature**</span><span class="sxs-lookup"><span data-stu-id="57d15-149">**SetMonitorColorTemperature**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | <span data-ttu-id="57d15-150">設定監視器的色溫。</span><span class="sxs-lookup"><span data-stu-id="57d15-150">Sets a monitor's color temperature.</span></span>                                                  |
| [<span data-ttu-id="57d15-151">**SetMonitorContrast**</span><span class="sxs-lookup"><span data-stu-id="57d15-151">**SetMonitorContrast**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | <span data-ttu-id="57d15-152">設定監視的對比值。</span><span class="sxs-lookup"><span data-stu-id="57d15-152">Sets a monitor's contrast value.</span></span>                                                     |
| [<span data-ttu-id="57d15-153">**SetMonitorDisplayAreaPosition**</span><span class="sxs-lookup"><span data-stu-id="57d15-153">**SetMonitorDisplayAreaPosition**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | <span data-ttu-id="57d15-154">設定監視器顯示區域的水準或垂直位置。</span><span class="sxs-lookup"><span data-stu-id="57d15-154">Sets the horizontal or vertical position of a monitor's display area.</span></span>                |
| [<span data-ttu-id="57d15-155">**SetMonitorDisplayAreaSize**</span><span class="sxs-lookup"><span data-stu-id="57d15-155">**SetMonitorDisplayAreaSize**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | <span data-ttu-id="57d15-156">設定監視器顯示區域的寬度或高度。</span><span class="sxs-lookup"><span data-stu-id="57d15-156">Sets the width or height of a monitor's display area.</span></span>                                |
| [<span data-ttu-id="57d15-157">**SetMonitorRedGreenOrBlueDrive**</span><span class="sxs-lookup"><span data-stu-id="57d15-157">**SetMonitorRedGreenOrBlueDrive**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | <span data-ttu-id="57d15-158">設定監視的紅色、綠色或藍色的磁片磁碟機值。</span><span class="sxs-lookup"><span data-stu-id="57d15-158">Sets a monitor's red, green, or blue drive value.</span></span>                                    |
| [<span data-ttu-id="57d15-159">**SetMonitorRedGreenOrBlueGain**</span><span class="sxs-lookup"><span data-stu-id="57d15-159">**SetMonitorRedGreenOrBlueGain**</span></span>](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | <span data-ttu-id="57d15-160">設定監視的紅色、綠色或藍色增益值。</span><span class="sxs-lookup"><span data-stu-id="57d15-160">Sets a monitor's red, green, or blue gain value.</span></span>                                     |



 

## <a name="low-level-functions"></a><span data-ttu-id="57d15-161">Low-Level 函式</span><span class="sxs-lookup"><span data-stu-id="57d15-161">Low-Level Functions</span></span>



| <span data-ttu-id="57d15-162">函式</span><span class="sxs-lookup"><span data-stu-id="57d15-162">Function</span></span>                                                                                   | <span data-ttu-id="57d15-163">描述</span><span class="sxs-lookup"><span data-stu-id="57d15-163">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57d15-164">**CapabilitiesRequestAndCapabilitiesReply**</span><span class="sxs-lookup"><span data-stu-id="57d15-164">**CapabilitiesRequestAndCapabilitiesReply**</span></span>](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | <span data-ttu-id="57d15-165">抓取描述監視器功能的字串。</span><span class="sxs-lookup"><span data-stu-id="57d15-165">Retrieves a string describing a monitor's capabilities.</span></span>                                                        |
| [<span data-ttu-id="57d15-166">**GetCapabilitiesStringLength**</span><span class="sxs-lookup"><span data-stu-id="57d15-166">**GetCapabilitiesStringLength**</span></span>](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | <span data-ttu-id="57d15-167">捕獲監視器功能字串的長度。</span><span class="sxs-lookup"><span data-stu-id="57d15-167">Retrieves the length of a monitor's capabilities string.</span></span>                                                       |
| [<span data-ttu-id="57d15-168">**GetTimingReport**</span><span class="sxs-lookup"><span data-stu-id="57d15-168">**GetTimingReport**</span></span>](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | <span data-ttu-id="57d15-169">捕獲監視器的水準和垂直同步處理頻率。</span><span class="sxs-lookup"><span data-stu-id="57d15-169">Retrieves a monitor's horizontal and vertical synchronization frequencies.</span></span>                                     |
| [<span data-ttu-id="57d15-170">**GetVCPFeatureAndVCPFeatureReply**</span><span class="sxs-lookup"><span data-stu-id="57d15-170">**GetVCPFeatureAndVCPFeatureReply**</span></span>](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | <span data-ttu-id="57d15-171">抓取虛擬主控台的目前值、最大值和程式碼類型 (VCP) 程式碼的監視器。</span><span class="sxs-lookup"><span data-stu-id="57d15-171">Retrieves the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span> |
| [<span data-ttu-id="57d15-172">**SaveCurrentSettings**</span><span class="sxs-lookup"><span data-stu-id="57d15-172">**SaveCurrentSettings**</span></span>](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | <span data-ttu-id="57d15-173">將目前的監視器設定儲存至顯示器的非動態儲存體。</span><span class="sxs-lookup"><span data-stu-id="57d15-173">Saves the current monitor settings to the display's nonvolatile storage.</span></span>                                       |
| [<span data-ttu-id="57d15-174">**SetVCPFeature**</span><span class="sxs-lookup"><span data-stu-id="57d15-174">**SetVCPFeature**</span></span>](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | <span data-ttu-id="57d15-175">設定監視的虛擬主控台 (VCP) 程式碼的值。</span><span class="sxs-lookup"><span data-stu-id="57d15-175">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>                                            |



 

## <a name="enumeration-functions"></a><span data-ttu-id="57d15-176">列舉函數</span><span class="sxs-lookup"><span data-stu-id="57d15-176">Enumeration Functions</span></span>



| <span data-ttu-id="57d15-177">函式</span><span class="sxs-lookup"><span data-stu-id="57d15-177">Function</span></span>                                                                                                   | <span data-ttu-id="57d15-178">描述</span><span class="sxs-lookup"><span data-stu-id="57d15-178">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57d15-179">**DestroyPhysicalMonitor**</span><span class="sxs-lookup"><span data-stu-id="57d15-179">**DestroyPhysicalMonitor**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | <span data-ttu-id="57d15-180">關閉實體監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="57d15-180">Closes a handle to a physical monitor.</span></span>                                                    |
| [<span data-ttu-id="57d15-181">**DestroyPhysicalMonitors**</span><span class="sxs-lookup"><span data-stu-id="57d15-181">**DestroyPhysicalMonitors**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | <span data-ttu-id="57d15-182">關閉實體監視器控制碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="57d15-182">Closes an array of physical monitor handles.</span></span>                                              |
| [<span data-ttu-id="57d15-183">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="57d15-183">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | <span data-ttu-id="57d15-184">捕獲與 **HMONITOR** 監視器控制碼相關聯的實體監視器數目。</span><span class="sxs-lookup"><span data-stu-id="57d15-184">Retrieves the number of physical monitors associated with an **HMONITOR** monitor handle.</span></span> |
| [<span data-ttu-id="57d15-185">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="57d15-185">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | <span data-ttu-id="57d15-186">抓取與 Direct3D 裝置相關聯的實體監視器數目。</span><span class="sxs-lookup"><span data-stu-id="57d15-186">Retrieves the number of physical monitors associated with a Direct3D device.</span></span>              |
| [<span data-ttu-id="57d15-187">**GetPhysicalMonitorsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="57d15-187">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | <span data-ttu-id="57d15-188">抓取與 **HMONITOR** 監視器控制碼相關聯的實體監視器。</span><span class="sxs-lookup"><span data-stu-id="57d15-188">Retrieves the physical monitors associated with an **HMONITOR** monitor handle.</span></span>           |
| [<span data-ttu-id="57d15-189">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="57d15-189">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | <span data-ttu-id="57d15-190">抓取與 Direct3D 裝置相關聯的實體監視器。</span><span class="sxs-lookup"><span data-stu-id="57d15-190">Retrieves the physical monitors associated with a Direct3D device.</span></span>                        |



 

## <a name="internal-functions"></a><span data-ttu-id="57d15-191">內部函數</span><span class="sxs-lookup"><span data-stu-id="57d15-191">Internal Functions</span></span>

<span data-ttu-id="57d15-192">監視器設定 API 會使用下列功能來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="57d15-192">The following functions are used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="57d15-193">應用程式不應呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="57d15-193">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="57d15-194">**DDCCIGetCapabilitiesString**</span><span class="sxs-lookup"><span data-stu-id="57d15-194">**DDCCIGetCapabilitiesString**</span></span>](ddccigetcapabilitiesstring.md)
-   [<span data-ttu-id="57d15-195">**DDCCIGetCapabilitiesStringLength**</span><span class="sxs-lookup"><span data-stu-id="57d15-195">**DDCCIGetCapabilitiesStringLength**</span></span>](ddccigetcapabilitiesstringlength.md)
-   [<span data-ttu-id="57d15-196">**DDCCIGetTimingReport**</span><span class="sxs-lookup"><span data-stu-id="57d15-196">**DDCCIGetTimingReport**</span></span>](ddccigettimingreport.md)
-   [<span data-ttu-id="57d15-197">**DDCCIGetVCPFeature**</span><span class="sxs-lookup"><span data-stu-id="57d15-197">**DDCCIGetVCPFeature**</span></span>](ddccigetvcpfeature.md)
-   [<span data-ttu-id="57d15-198">**DDCCISaveCurrentSettings**</span><span class="sxs-lookup"><span data-stu-id="57d15-198">**DDCCISaveCurrentSettings**</span></span>](ddccisavecurrentsettings.md)
-   [<span data-ttu-id="57d15-199">**DDCCISetVCPFeature**</span><span class="sxs-lookup"><span data-stu-id="57d15-199">**DDCCISetVCPFeature**</span></span>](ddccisetvcpfeature.md)
-   [<span data-ttu-id="57d15-200">**DestroyPhysicalMonitorInternal**</span><span class="sxs-lookup"><span data-stu-id="57d15-200">**DestroyPhysicalMonitorInternal**</span></span>](destroyphysicalmonitorinternal.md)
-   [<span data-ttu-id="57d15-201">**GetNumberOfPhysicalMonitors**</span><span class="sxs-lookup"><span data-stu-id="57d15-201">**GetNumberOfPhysicalMonitors**</span></span>](getnumberofphysicalmonitors.md)
-   [<span data-ttu-id="57d15-202">**GetPhysicalMonitorDescription**</span><span class="sxs-lookup"><span data-stu-id="57d15-202">**GetPhysicalMonitorDescription**</span></span>](getphysicalmonitordescription.md)
-   [<span data-ttu-id="57d15-203">**GetPhysicalMonitors**</span><span class="sxs-lookup"><span data-stu-id="57d15-203">**GetPhysicalMonitors**</span></span>](getphysicalmonitors.md)

## <a name="related-topics"></a><span data-ttu-id="57d15-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="57d15-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57d15-205">監視設定參考</span><span class="sxs-lookup"><span data-stu-id="57d15-205">Monitor Configuration Reference</span></span>](monitor-configuration-reference.md)
</dt> </dl>

 

 




