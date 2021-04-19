---
title: 使用 High-Level 監視設定函數
description: 使用 High-Level 監視設定函數
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- 監視，函數
- 監視，高階設定函數
- 監視，列舉實體監視器
- 監視，持續設定
- 監視設定、高階設定功能
- 監視設定，函數
- 監視設定，列舉實體監視器
- 監視設定、連續設定
- 列舉實體監視器
- 高階設定函數
- 持續監視設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff494388aac91d8aacd92ed4fe345722ea18659f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969101"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a><span data-ttu-id="684de-114">使用 High-Level 監視設定函數</span><span class="sxs-lookup"><span data-stu-id="684de-114">Using the High-Level Monitor Configuration Functions</span></span>

## <a name="enumerating-physical-monitors"></a><span data-ttu-id="684de-115">列舉實體監視器</span><span class="sxs-lookup"><span data-stu-id="684de-115">Enumerating Physical Monitors</span></span>

<span data-ttu-id="684de-116">有幾個函式會列舉顯示裝置，包括 [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) 和 [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)。</span><span class="sxs-lookup"><span data-stu-id="684de-116">There are several functions that enumerate display devices, including [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) and [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span> <span data-ttu-id="684de-117">這些函式記載于 Windows GDI 檔的 [ [多個顯示監視器](/windows/desktop/gdi/multiple-display-monitors)] 主題下。</span><span class="sxs-lookup"><span data-stu-id="684de-117">These functions are documented in the Windows GDI documentation, under the topic [Multiple Display Monitors](/windows/desktop/gdi/multiple-display-monitors).</span></span> <span data-ttu-id="684de-118">這些函數會傳回 **HMONITOR** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="684de-118">These functions return **HMONITOR** handles.</span></span> <span data-ttu-id="684de-119">不過，儘管名稱， **HMONITOR** 控制碼也可以與一個以上的實體監視器相關聯。</span><span class="sxs-lookup"><span data-stu-id="684de-119">Despite the name, however, an **HMONITOR** handle can be associated with more than one physical monitor.</span></span> <span data-ttu-id="684de-120">若要設定監視的設定，應用程式必須藉由呼叫 [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)來取得實體監視器的唯一控制碼。</span><span class="sxs-lookup"><span data-stu-id="684de-120">To configure the settings on a monitor, the application must get a unique handle to the physical monitor by calling [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).</span></span>

<span data-ttu-id="684de-121">如果您的應用程式使用 Direct3D，您可以藉由呼叫 [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)從 direct3d 裝置取得監視器控制碼。</span><span class="sxs-lookup"><span data-stu-id="684de-121">If your application uses Direct3D, you can get a monitor handle from a Direct3D device by calling [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9).</span></span>

## <a name="supported-functions"></a><span data-ttu-id="684de-122">支援的函式</span><span class="sxs-lookup"><span data-stu-id="684de-122">Supported Functions</span></span>

<span data-ttu-id="684de-123">監視器可能不支援所有的監視設定功能。</span><span class="sxs-lookup"><span data-stu-id="684de-123">A monitor might not support all of the monitor configuration functions.</span></span> <span data-ttu-id="684de-124">若要找出監視器支援哪些功能，請呼叫 [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="684de-124">To find out which functions a monitor supports, call [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).</span></span>

## <a name="continuous-monitor-settings"></a><span data-ttu-id="684de-125">持續監視設定</span><span class="sxs-lookup"><span data-stu-id="684de-125">Continuous Monitor Settings</span></span>

<span data-ttu-id="684de-126">*持續* 監視設定可以範圍介於最小值和最大值之間。</span><span class="sxs-lookup"><span data-stu-id="684de-126">A *continuous* monitor setting is one that can range between some minimum and maximum value.</span></span> <span data-ttu-id="684de-127">大部分的高階監視設定函數都會控制連續監視設定。</span><span class="sxs-lookup"><span data-stu-id="684de-127">Most of the high-level monitor configuration functions control continuous monitor settings.</span></span> <span data-ttu-id="684de-128">例如，亮度和對比是連續的設定。</span><span class="sxs-lookup"><span data-stu-id="684de-128">For example, brightness and contrast are continuous settings.</span></span>

<span data-ttu-id="684de-129">持續監視設定沒有定義的真實世界單位。</span><span class="sxs-lookup"><span data-stu-id="684de-129">Continuous monitor settings do not have defined real-world units.</span></span> <span data-ttu-id="684de-130">這些單位是任意的，而且可能會因不同的製造商而異。</span><span class="sxs-lookup"><span data-stu-id="684de-130">The units are arbitrary and can vary from one manufacturer to another.</span></span> <span data-ttu-id="684de-131">例如，如果兩個監視器具有相同的亮度值，則某個監視器可能會比其他監視器更亮。</span><span class="sxs-lookup"><span data-stu-id="684de-131">If two monitors have the same brightness value, for example, one monitor might look much brighter than another.</span></span> <span data-ttu-id="684de-132">一般而言，應用程式會向使用者呈現滑杆控制項或上下按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="684de-132">Typically, an application will present slider controls or up-down controls to the user.</span></span> <span data-ttu-id="684de-133">然後，使用者可以調整設定，以提供最佳的主觀品質。</span><span class="sxs-lookup"><span data-stu-id="684de-133">The user can then adjust the settings to give the best subjective quality.</span></span>

## <a name="changes-in-monitor-state"></a><span data-ttu-id="684de-134">監視狀態的變更</span><span class="sxs-lookup"><span data-stu-id="684de-134">Changes in Monitor State</span></span>

<span data-ttu-id="684de-135">監視器可能會因各種原因而變更狀態，包括：</span><span class="sxs-lookup"><span data-stu-id="684de-135">A monitor can change states for various reasons, including:</span></span>

-   <span data-ttu-id="684de-136">使用者會使用監視的前端面板控制項來變更設定。</span><span class="sxs-lookup"><span data-stu-id="684de-136">The user changes the settings with the monitor's front-panel controls.</span></span>
-   <span data-ttu-id="684de-137">使用者變更監視器的螢幕解析度、更新頻率或位深度。</span><span class="sxs-lookup"><span data-stu-id="684de-137">The user changes the monitor's screen resolution, refresh rate, or bit depth.</span></span>
-   <span data-ttu-id="684de-138">應用程式會使用低層級的監視功能來變更無法從高階函式存取的設定。</span><span class="sxs-lookup"><span data-stu-id="684de-138">The application uses the low-level monitor functions to change a setting that is not accessible from the high-level functions.</span></span>
-   <span data-ttu-id="684de-139">應用程式會呼叫 [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) 或 [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)。</span><span class="sxs-lookup"><span data-stu-id="684de-139">The application calls [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) or [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults).</span></span>

<span data-ttu-id="684de-140">所有這些事件都可以變更監視設定。</span><span class="sxs-lookup"><span data-stu-id="684de-140">All of these events can change monitor settings.</span></span> <span data-ttu-id="684de-141">它們也可以變更設定的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="684de-141">They can also change the minimum and maximum value of a setting.</span></span>

## <a name="dependencies-among-monitor-settings"></a><span data-ttu-id="684de-142">監視設定之間的相依性</span><span class="sxs-lookup"><span data-stu-id="684de-142">Dependencies Among Monitor Settings</span></span>

<span data-ttu-id="684de-143">變更色溫可能會變更目前的磁片磁碟機並進行設定，相反地，反向也是如此。</span><span class="sxs-lookup"><span data-stu-id="684de-143">Changing the color temperature can change the current drive and gain settings, and the reverse is also true.</span></span> <span data-ttu-id="684de-144">這些是高階監視設定功能之間唯一的相依性。</span><span class="sxs-lookup"><span data-stu-id="684de-144">Those are the only dependencies among the high-level monitor configuration functions.</span></span> <span data-ttu-id="684de-145">其他設定可能只能透過低層級的監視功能來存取。</span><span class="sxs-lookup"><span data-stu-id="684de-145">Other settings might be accessible only through the low-level monitor functions.</span></span> <span data-ttu-id="684de-146">這些設定與高階設定之間可能會有相依性。</span><span class="sxs-lookup"><span data-stu-id="684de-146">There might be dependencies between those settings and the high-level settings.</span></span> <span data-ttu-id="684de-147">這些相依性是廠商特定的。</span><span class="sxs-lookup"><span data-stu-id="684de-147">These dependencies are vendor-specific.</span></span> <span data-ttu-id="684de-148">應用程式可以透過數種方式來處理這個問題：</span><span class="sxs-lookup"><span data-stu-id="684de-148">An application can handle this problem in several ways:</span></span>

-   <span data-ttu-id="684de-149">只使用高階函數。</span><span class="sxs-lookup"><span data-stu-id="684de-149">Use only high-level functions.</span></span>
-   <span data-ttu-id="684de-150">呼叫低層級函數之後，取得每個監視設定的目前值。</span><span class="sxs-lookup"><span data-stu-id="684de-150">After calling a low-level function, get the current value of every monitor setting.</span></span> <span data-ttu-id="684de-151">可惜的是，這種方法可能會很慢，因為取得每項設定大約需要40毫秒。</span><span class="sxs-lookup"><span data-stu-id="684de-151">Unfortunately, this approach can be slow, because getting each setting takes about 40 milliseconds.</span></span>
-   <span data-ttu-id="684de-152">使用低層級的函式，只搭配您瞭解其行為的特定監視模型。</span><span class="sxs-lookup"><span data-stu-id="684de-152">Use low-level functions only with specific monitor models whose behavior you understand.</span></span>

## <a name="disabled-monitor-settings"></a><span data-ttu-id="684de-153">停用的監視設定</span><span class="sxs-lookup"><span data-stu-id="684de-153">Disabled Monitor Settings</span></span>

<span data-ttu-id="684de-154">應用程式無法藉由呼叫高階監視功能來停用任何監視設定。</span><span class="sxs-lookup"><span data-stu-id="684de-154">An application cannot disable any monitor settings by calling the high-level monitor functions.</span></span> <span data-ttu-id="684de-155">但是，如果應用程式使用低層級的函式來變更高階函式不支援的監視設定，則應用程式可能會不小心停用設定。</span><span class="sxs-lookup"><span data-stu-id="684de-155">However, an application might accidentally disable a setting if it uses the low-level functions to change a monitor setting that is not supported by the high-level functions.</span></span> <span data-ttu-id="684de-156">此外，使用者可能會使用前端板控制項來停用設定。</span><span class="sxs-lookup"><span data-stu-id="684de-156">Also, a user might disable a setting by using the front-panel control.</span></span> <span data-ttu-id="684de-157">這些行為是廠商特定的行為。</span><span class="sxs-lookup"><span data-stu-id="684de-157">These behaviors are vendor-specific.</span></span>

<span data-ttu-id="684de-158">如果監視設定變成停用，任何設定或抓取該設定的函式都會失敗，並將最後一個錯誤碼設定為 [ \_ 停用錯誤] \_ 監視 \_ 設定。</span><span class="sxs-lookup"><span data-stu-id="684de-158">If a monitor setting becomes disabled, any function that sets or retrieves that setting will fail and set the last-error code to ERROR\_DISABLED\_MONITOR\_SETTING.</span></span> <span data-ttu-id="684de-159">發生這種情況時，應用程式可以執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="684de-159">When this occurs, the application can do one of the following:</span></span>

-   <span data-ttu-id="684de-160">顯示錯誤訊息，並向使用者建議使用前端板控制項來調整設定。</span><span class="sxs-lookup"><span data-stu-id="684de-160">Display an error message and suggest to the user that he or she try adjusting the setting by using the front-panel control.</span></span>
-   <span data-ttu-id="684de-161">呼叫 [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) 函數。</span><span class="sxs-lookup"><span data-stu-id="684de-161">Call the [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) function.</span></span> <span data-ttu-id="684de-162">如果監視的「MC \_ 還原 \_ 出廠 \_ 預設值」 \_ 啟用 \_ 監視 \_ 設定功能旗標，則此函式會啟用高階監視功能所支援的所有監視設定。</span><span class="sxs-lookup"><span data-stu-id="684de-162">If a monitor has the MC\_RESTORE\_FACTORY\_DEFAULTS\_ENABLES\_MONITOR\_SETTINGS capabilities flag, this function enables all of the monitor settings that are supported by the high-level monitor functions.</span></span> <span data-ttu-id="684de-163">可惜的是，此函式也會將監視器設定重設為其原廠預設值。</span><span class="sxs-lookup"><span data-stu-id="684de-163">Unfortunately, the function also resets the monitor settings to their factory default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="684de-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="684de-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="684de-165">使用監視設定</span><span class="sxs-lookup"><span data-stu-id="684de-165">Using Monitor Configuration</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 