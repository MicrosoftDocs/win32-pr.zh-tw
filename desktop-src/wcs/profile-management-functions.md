---
title: 設定檔管理功能
description: 設定檔管理功能
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- Windows Color System (WCS) ，設定檔
- WCS (Windows 色彩系統) ，設定檔
- 影像色彩管理，設定檔
- 色彩管理，設定檔
- 色彩，設定檔
- WCS 參考，設定檔
- WCS 的參考，設定檔
- 設定檔管理
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106993767"
---
# <a name="profile-management-functions"></a><span data-ttu-id="92bdb-118">設定檔管理功能</span><span class="sxs-lookup"><span data-stu-id="92bdb-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="92bdb-119">設定檔管理功能</span><span class="sxs-lookup"><span data-stu-id="92bdb-119">Profile Management Functions</span></span>

<span data-ttu-id="92bdb-120">下列 API 函數在設定檔管理中很有用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="92bdb-121">函式</span><span class="sxs-lookup"><span data-stu-id="92bdb-121">Function</span></span>                                                                               | <span data-ttu-id="92bdb-122">描述</span><span class="sxs-lookup"><span data-stu-id="92bdb-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92bdb-123">**AssociateColorProfileWithDeviceW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="92bdb-124">將指定的色彩設定檔與指定的裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="92bdb-125">[**CreateProfileFromLogColorSpaceW**] ( (/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) </span><span class="sxs-lookup"><span data-stu-id="92bdb-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="92bdb-126">將邏輯 [色彩空間](c.md) 轉換成 [裝置設定檔](d.md)。</span><span class="sxs-lookup"><span data-stu-id="92bdb-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="92bdb-127">**DisassociateColorProfileFromDeviceW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="92bdb-128">解除指定的色彩設定檔與指定電腦上的指定裝置。</span><span class="sxs-lookup"><span data-stu-id="92bdb-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="92bdb-129">**EnumColorProfilesW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="92bdb-130">列舉滿足指定列舉準則的所有設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="92bdb-131">**GetColorDirectoryW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="92bdb-132">抓取指定電腦上 Windows COLOR 目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="92bdb-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="92bdb-133">**GetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="92bdb-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="92bdb-134">從直接色彩顯示面板取得 gamma 曲線。</span><span class="sxs-lookup"><span data-stu-id="92bdb-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="92bdb-135">**GetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="92bdb-136">抓取已針對指定標準 [色彩空間](c.md)註冊的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="92bdb-137">**InstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="92bdb-138">安裝指定的設定檔，以便在指定的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="92bdb-139">設定檔也會複製到 COLOR 目錄。</span><span class="sxs-lookup"><span data-stu-id="92bdb-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="92bdb-140">**RegisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="92bdb-141">將指定的識別值與指定的色彩管理模組動態連結程式庫產生關聯 (的 CMM DLL) 。</span><span class="sxs-lookup"><span data-stu-id="92bdb-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="92bdb-142">當此識別碼出現在色彩設定檔中時，Windows 可以找到對應的 CMM，以便建立轉換。</span><span class="sxs-lookup"><span data-stu-id="92bdb-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="92bdb-143">**SetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="92bdb-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="92bdb-144">設定直接色彩顯示面板上的 gamma 曲線。</span><span class="sxs-lookup"><span data-stu-id="92bdb-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="92bdb-145">**SetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="92bdb-146">針對指定的標準 [色彩空間](c.md)，註冊指定的設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="92bdb-147">您可以使用 [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew)來查詢設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="92bdb-148">**UninstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="92bdb-149">從指定的電腦移除指定的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="92bdb-150">相關聯的檔案會選擇性地從系統中刪除。</span><span class="sxs-lookup"><span data-stu-id="92bdb-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="92bdb-151">**UnregisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="92bdb-152">從指定的色彩管理模組動態連結程式庫分離指定的識別碼值， (CMM DLL) 。</span><span class="sxs-lookup"><span data-stu-id="92bdb-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="92bdb-153">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="92bdb-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="92bdb-154">將指定的 WCS 色彩設定檔與指定的裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="92bdb-155">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="92bdb-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="92bdb-156">將 WCS 設定檔轉換成 ICC 設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="92bdb-157">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="92bdb-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="92bdb-158">解除指定的 WCS 色彩設定檔與指定電腦上的指定裝置。</span><span class="sxs-lookup"><span data-stu-id="92bdb-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="92bdb-159">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="92bdb-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="92bdb-160">列舉符合指定設定檔管理範圍中的列舉準則的所有色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="92bdb-161">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="92bdb-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="92bdb-162">傳回 [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) 函式列舉色彩設定檔所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="92bdb-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="92bdb-163">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="92bdb-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="92bdb-164">抓取裝置的預設色彩設定檔，或如果未指定裝置，則抓取與裝置無關的預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="92bdb-165">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="92bdb-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="92bdb-166">傳回裝置預設色彩設定檔名稱的大小（以位元組為單位），包括 **Null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="92bdb-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="92bdb-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="92bdb-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="92bdb-168">抓取指定設定檔管理範圍中的預設轉譯意圖。</span><span class="sxs-lookup"><span data-stu-id="92bdb-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="92bdb-169">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="92bdb-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="92bdb-170">判斷使用者是否已選擇針對指定的裝置使用每個使用者設定檔關聯清單。</span><span class="sxs-lookup"><span data-stu-id="92bdb-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="92bdb-171">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="92bdb-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="92bdb-172">建立指定之色彩設定檔的控制碼。</span><span class="sxs-lookup"><span data-stu-id="92bdb-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="92bdb-173">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="92bdb-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="92bdb-174">設定指定設定檔管理範圍中指定配置檔案類型的預設色彩設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="92bdb-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="92bdb-175">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="92bdb-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="92bdb-176">設定指定設定檔管理範圍中的預設轉譯意圖。</span><span class="sxs-lookup"><span data-stu-id="92bdb-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="92bdb-177">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="92bdb-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="92bdb-178">允許使用者指定是否要針對指定的裝置使用每個使用者設定檔關聯清單。</span><span class="sxs-lookup"><span data-stu-id="92bdb-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="92bdb-179">設定檔耗用量函數</span><span class="sxs-lookup"><span data-stu-id="92bdb-179">Profile Consumption Functions</span></span>

<span data-ttu-id="92bdb-180">設定檔耗用量 Api 是 ICM2 中採用 ICC 或 WCS XML 設定檔、設定檔控制碼或轉譯意圖作為參數的 Api，以及一組適用于 WCS 設定檔的新 Api，可支援應用程式色彩管理程式碼。</span><span class="sxs-lookup"><span data-stu-id="92bdb-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="92bdb-181">設定檔和設定檔管理功能</span><span class="sxs-lookup"><span data-stu-id="92bdb-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="92bdb-182">設定檔管理工作流程是以現有的 ICM2 Api 為基礎，這些 Api 已增強，可提供額外的功能來修訂應用程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="92bdb-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="92bdb-183">設定檔包含色彩處理演算法用來轉譯不同色彩空間之間色彩的資訊。</span><span class="sxs-lookup"><span data-stu-id="92bdb-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="92bdb-184">設定檔管理提供一種方式來查詢和指定在不同階段使用哪些設定檔來處理色彩處理模型，以管理各種具有不同色彩特性的周邊裝置色彩輸出。</span><span class="sxs-lookup"><span data-stu-id="92bdb-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="92bdb-185">設定檔管理提供下列一組功能：</span><span class="sxs-lookup"><span data-stu-id="92bdb-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="92bdb-186">安裝色彩設定檔以供系統使用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="92bdb-187">將一或多個已安裝的色彩設定檔與任何特定裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="92bdb-188">在設定檔中選擇特定類型的預設色彩設定檔，可用於特定的色彩處理階段。</span><span class="sxs-lookup"><span data-stu-id="92bdb-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="92bdb-189">這可能適用于裝置相關設定檔中的裝置，或安裝在系統中的設定檔，而不是特定裝置。</span><span class="sxs-lookup"><span data-stu-id="92bdb-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="92bdb-190">列舉色彩設定檔，以滿足系統中所安裝設定檔之間的特定準則。</span><span class="sxs-lookup"><span data-stu-id="92bdb-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="92bdb-191">WCS 設定檔的副檔名為 ". cdmp" （適用于 DMPs）、". camp" （Camp）和 ". gmmp" （適用于 GMMPs）。</span><span class="sxs-lookup"><span data-stu-id="92bdb-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="92bdb-192">**每個使用者設定檔管理，並在 LUA 內容中啟用執行**</span><span class="sxs-lookup"><span data-stu-id="92bdb-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="92bdb-193">目前檔中所述的設計目標如下所示：</span><span class="sxs-lookup"><span data-stu-id="92bdb-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="92bdb-194">舊版 ICM2 的執行不提供個別使用者設定檔管理的支援。</span><span class="sxs-lookup"><span data-stu-id="92bdb-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="92bdb-195">不同的使用者不能有自己的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="92bdb-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="92bdb-196">在 Vista 中，WCS 設定檔管理基礎結構可讓使用者針對大部分功能設定個別的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="92bdb-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="92bdb-197">所有舊版 ICM2 設定檔管理 Api 都會修改整個系統的設定，而且需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="92bdb-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="92bdb-198">在 Windows Vista 中，所有使用者都是在最低許可權的使用者帳戶中執行， (LUA) 設定，而系統管理員可以選擇性地提升許可權，以執行修改全系統設定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="92bdb-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="92bdb-199">在 WCS 設定檔管理中，所有每個使用者的設定檔設定都可在 LUA 內容中進行設定。</span><span class="sxs-lookup"><span data-stu-id="92bdb-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="92bdb-200">設定檔管理應用程式可以執行為 LUA 設定，增加其使用範圍，並確保系統的安全性不會受到危害。</span><span class="sxs-lookup"><span data-stu-id="92bdb-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="92bdb-201">Vista 中的設定檔管理提供下列優於舊版 ICM2 基礎結構的增強功能：</span><span class="sxs-lookup"><span data-stu-id="92bdb-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="92bdb-202">它可讓設定檔與裝置、預設設定檔設定，以及列舉每個使用者和整個系統範圍中的設定檔相關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="92bdb-203">安裝設定檔會維持系統的範圍，而且需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="92bdb-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="92bdb-204">這與裝置安裝期間的設定檔安裝一致，因為裝置安裝全系統，且需要系統管理許可權。</span><span class="sxs-lookup"><span data-stu-id="92bdb-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="92bdb-205">是否可以從 LUA 內容安裝裝置，是針對該類別的裝置所支援的裝置。</span><span class="sxs-lookup"><span data-stu-id="92bdb-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="92bdb-206">例如，在 Vista 中，如果使用者已被授與使用驅動程式存放區原則的網域系統管理員將檔案複製到驅動程式存放區的許可權，就可以從 LUA 內容進行印表機安裝。</span><span class="sxs-lookup"><span data-stu-id="92bdb-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="92bdb-207">色彩設定檔管理基礎結構不需要在這方面做任何特殊的動作，因為安裝會在多工緩衝處理器內容中進行。</span><span class="sxs-lookup"><span data-stu-id="92bdb-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="92bdb-208">修改每個使用者範圍中的設定檔設定可以在 LUA 內容中完成;需要系統管理許可權的全系統修改。</span><span class="sxs-lookup"><span data-stu-id="92bdb-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="92bdb-209">需要讀取設定資訊的設定檔管理作業，可以在每個使用者和全系統設定的 LUA 內容中完成。</span><span class="sxs-lookup"><span data-stu-id="92bdb-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="92bdb-210">設定檔管理範圍表示執行的作業範圍;每位使用者或整個系統。</span><span class="sxs-lookup"><span data-stu-id="92bdb-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="92bdb-211">針對每個作業，其會指出是否可以從 LUA 內容進行。</span><span class="sxs-lookup"><span data-stu-id="92bdb-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="92bdb-212">如果無法在 LUA 內容中執行作業，對應的設定檔管理 API 會傳回失敗並拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="92bdb-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="92bdb-213">使用 API 的應用程式（例如色彩管理主控台）可以讓使用者使用 OTS 或同意 UI) 提升至系統管理內容 (，然後從提高許可權的內容中呼叫 API，如此作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="92bdb-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="92bdb-214">作業</span><span class="sxs-lookup"><span data-stu-id="92bdb-214">Operation</span></span>

<span data-ttu-id="92bdb-215">設定檔管理範圍</span><span class="sxs-lookup"><span data-stu-id="92bdb-215">Profile Management Scope</span></span>

<span data-ttu-id="92bdb-216">前置條件</span><span class="sxs-lookup"><span data-stu-id="92bdb-216">Pre-condition</span></span>

<span data-ttu-id="92bdb-217">後置條件</span><span class="sxs-lookup"><span data-stu-id="92bdb-217">Post-condition</span></span>

<span data-ttu-id="92bdb-218">LUA 內容中的可執行檔</span><span class="sxs-lookup"><span data-stu-id="92bdb-218">Executable in LUA context</span></span>

<span data-ttu-id="92bdb-219">$ {ROWSPAN2} $Install 設定檔 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-220">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-220">System wide</span></span>

<span data-ttu-id="92bdb-221">設定檔已複製、安裝到系統中，並且可供使用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="92bdb-222">所有使用者的整個系統和目前使用者範圍中的設定檔是可列舉的。</span><span class="sxs-lookup"><span data-stu-id="92bdb-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="92bdb-223">在安裝設備磁碟機時，受驅動程式安裝原則所規範。</span><span class="sxs-lookup"><span data-stu-id="92bdb-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="92bdb-224">否，否則為。</span><span class="sxs-lookup"><span data-stu-id="92bdb-224">No, otherwise.</span></span>

<span data-ttu-id="92bdb-225">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-225">Current user</span></span>

<span data-ttu-id="92bdb-226">不支援</span><span class="sxs-lookup"><span data-stu-id="92bdb-226">Not supported</span></span>

<span data-ttu-id="92bdb-227">$ {ROWSPAN2} $Uninstall 設定檔 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-228">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-228">System wide</span></span>

<span data-ttu-id="92bdb-229">設定檔安裝在系統中</span><span class="sxs-lookup"><span data-stu-id="92bdb-229">Profile is installed in the system</span></span>

<span data-ttu-id="92bdb-230">從系統卸載的設定檔，並選擇性地從設定檔存放區刪除。</span><span class="sxs-lookup"><span data-stu-id="92bdb-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="92bdb-231">設定檔無法再使用，且在任何範圍中都不可列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="92bdb-232">No</span><span class="sxs-lookup"><span data-stu-id="92bdb-232">No</span></span>

<span data-ttu-id="92bdb-233">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-233">Current user</span></span>

<span data-ttu-id="92bdb-234">不支援</span><span class="sxs-lookup"><span data-stu-id="92bdb-234">Not supported</span></span>

<span data-ttu-id="92bdb-235">具有裝置 $ {REMOVE} $ 的 $ {ROWSPAN2} $Associate 設定檔</span><span class="sxs-lookup"><span data-stu-id="92bdb-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-236">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-236">System wide</span></span>

<span data-ttu-id="92bdb-237">設定檔已安裝，且其類型為 ICC 或 CDMP</span><span class="sxs-lookup"><span data-stu-id="92bdb-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="92bdb-238">所有使用者都可以使用設定檔來與裝置搭配使用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="92bdb-239">它是可列舉的，適用于全系統範圍，以及與裝置相關聯之所有使用者的目前使用者範圍。</span><span class="sxs-lookup"><span data-stu-id="92bdb-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="92bdb-240">No</span><span class="sxs-lookup"><span data-stu-id="92bdb-240">No</span></span>

<span data-ttu-id="92bdb-241">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-241">Current user</span></span>

<span data-ttu-id="92bdb-242">已安裝設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-242">Profile is installed.</span></span> <span data-ttu-id="92bdb-243">設定檔是否已經與全系統範圍中的裝置相關聯，而且屬於 ICC 或 CDMP 類型，並不重要。</span><span class="sxs-lookup"><span data-stu-id="92bdb-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="92bdb-244">目前的使用者可以使用設定檔來與裝置搭配使用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="92bdb-245">它只有在目前使用者的範圍內是可列舉的 (除非有與裝置相關聯的全系統關聯) 。</span><span class="sxs-lookup"><span data-stu-id="92bdb-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="92bdb-246">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-246">Yes</span></span>

<span data-ttu-id="92bdb-247">來自裝置 $ {REMOVE} $ 的 $ {ROWSPAN2} $Disassociate 設定檔</span><span class="sxs-lookup"><span data-stu-id="92bdb-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-248">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-248">System wide</span></span>

<span data-ttu-id="92bdb-249">設定檔與整個系統範圍中的裝置相關聯，且類型為 ICC 或 CDMP</span><span class="sxs-lookup"><span data-stu-id="92bdb-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="92bdb-250">設定檔已不再可供使用 (除了其目前使用者範圍內具有此關聯的使用者，也) 。</span><span class="sxs-lookup"><span data-stu-id="92bdb-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="92bdb-251">它在整個系統範圍中不可列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="92bdb-252">但是，對於在其範圍內具有這個關聯的使用者而言，它可以在目前使用者的範圍內列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="92bdb-253">No</span><span class="sxs-lookup"><span data-stu-id="92bdb-253">No</span></span>

<span data-ttu-id="92bdb-254">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-254">Current user</span></span>

<span data-ttu-id="92bdb-255">設定檔與目前使用者範圍中的裝置相關聯 (無論它是否與整個系統範圍) 相關聯，且其類型為 ICC 或 CDMP。</span><span class="sxs-lookup"><span data-stu-id="92bdb-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="92bdb-256">設定檔已無法再使用，或與裝置相關聯的可列舉（依目前使用者 (），除非它也與裝置) 的全系統範圍相關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="92bdb-257">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-257">Yes</span></span>

<span data-ttu-id="92bdb-258">$ {ROWSPAN2} $Set 配置檔案類型 (DMP 或 ICC) 作為裝置 $ {REMOVE} $ 的預設值</span><span class="sxs-lookup"><span data-stu-id="92bdb-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-259">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-259">System wide</span></span>

<span data-ttu-id="92bdb-260">設定檔的類型為 ICC 或 CDMP</span><span class="sxs-lookup"><span data-stu-id="92bdb-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="92bdb-261">此設定檔預設會用於裝置的特定類型，除了在其目前使用者範圍中覆寫此設定的使用者之外。</span><span class="sxs-lookup"><span data-stu-id="92bdb-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="92bdb-262"> (設定檔已安裝並與裝置系統寬度相關聯（如果尚未安裝的話）。 ) </span><span class="sxs-lookup"><span data-stu-id="92bdb-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="92bdb-263">No</span><span class="sxs-lookup"><span data-stu-id="92bdb-263">No</span></span>

<span data-ttu-id="92bdb-264">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-264">Current user</span></span>

<span data-ttu-id="92bdb-265">設定檔的類型為 ICC 或 CDMP</span><span class="sxs-lookup"><span data-stu-id="92bdb-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="92bdb-266">預設會在目前使用者的情況下，針對特定類型與裝置使用設定檔，而不考慮這個的全系統預設。</span><span class="sxs-lookup"><span data-stu-id="92bdb-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="92bdb-267"> (設定檔已安裝，並與目前使用者的裝置產生關聯（如果沒有的話）。 ) </span><span class="sxs-lookup"><span data-stu-id="92bdb-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="92bdb-268">是，如果已安裝設定檔</span><span class="sxs-lookup"><span data-stu-id="92bdb-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="92bdb-269">$ {ROWSPAN2} $Set 設定檔的類型 (ICC、DMP、CAMP、GMMP) 和子類型組合，作為全域預設 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-270">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-270">System wide</span></span>

<span data-ttu-id="92bdb-271">只有 ICC 和 CDMP 設定檔可以與裝置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="92bdb-272">預設會針對特定類型使用設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="92bdb-273">使用者可以在目前使用者的範圍內覆寫此設定。</span><span class="sxs-lookup"><span data-stu-id="92bdb-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="92bdb-274"> (已安裝設定檔（如果尚未安裝的話）。 ) </span><span class="sxs-lookup"><span data-stu-id="92bdb-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="92bdb-275">No</span><span class="sxs-lookup"><span data-stu-id="92bdb-275">No</span></span>

<span data-ttu-id="92bdb-276">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-276">Current user</span></span>

<span data-ttu-id="92bdb-277">只有 ICC 和 CDMP 設定檔可以與裝置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="92bdb-278">預設會針對目前使用者的特定類型使用設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="92bdb-279"> (已安裝設定檔（如果尚未安裝的話）。 ) </span><span class="sxs-lookup"><span data-stu-id="92bdb-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="92bdb-280">是，如果已安裝設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="92bdb-281">$ {ROWSPAN2} $Erase 特定預設設定檔設定的目前使用者覆寫，如此一來，系統預設一律會使用 (作為 fallback) 即使是目前使用者的範圍。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-282">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-282">System wide</span></span>

<span data-ttu-id="92bdb-283">不適用</span><span class="sxs-lookup"><span data-stu-id="92bdb-283">Not applicable</span></span>

<span data-ttu-id="92bdb-284">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-284">Current user</span></span>

<span data-ttu-id="92bdb-285">即使是針對預設設定檔設定的最新使用者查詢，也會傳回整個系統的設定，以供使用。</span><span class="sxs-lookup"><span data-stu-id="92bdb-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="92bdb-286">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-286">Yes</span></span>

<span data-ttu-id="92bdb-287">$ {ROWSPAN2} $Enumerate 已安裝的設定檔，滿足特定準則 (例如裝置類別、設定檔類別等等。 ) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-288">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-288">System wide</span></span>

<span data-ttu-id="92bdb-289">只有 ICC 和 CDMP 設定檔可以與裝置產生關聯和列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="92bdb-290">系統會列舉已安裝且符合全系統範圍中指定之準則的設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="92bdb-291">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-291">Yes</span></span>

<span data-ttu-id="92bdb-292">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-292">Current user</span></span>

<span data-ttu-id="92bdb-293">只有 ICC 和 CDMP 設定檔可以與裝置建立關聯，因此會針對裝置進行列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="92bdb-294">系統會列舉已安裝且符合全系統範圍中指定之準則的設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="92bdb-295">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-295">Yes</span></span>

<span data-ttu-id="92bdb-296">$ {ROWSPAN2} $Enumerate 設定檔與滿足特定條件的特定裝置相關聯，例如裝置類別和設定檔類別 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-297">全系統</span><span class="sxs-lookup"><span data-stu-id="92bdb-297">System wide</span></span>

<span data-ttu-id="92bdb-298">只有 ICC 和 CDMP 設定檔可以與裝置產生關聯和列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="92bdb-299">系統會列舉與整個系統範圍中的裝置相關聯的設定檔，並符合全系統範圍中指定的準則。</span><span class="sxs-lookup"><span data-stu-id="92bdb-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="92bdb-300">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-300">Yes</span></span>

<span data-ttu-id="92bdb-301">目前使用者</span><span class="sxs-lookup"><span data-stu-id="92bdb-301">Current user</span></span>

<span data-ttu-id="92bdb-302">只有 ICC 和 CDMP 設定檔可以與裝置產生關聯和列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="92bdb-303">與目前使用者範圍中的裝置相關聯的設定檔（包括系統範圍的關聯）以及滿足目前使用者範圍中指定的準則，都會加以列舉。</span><span class="sxs-lookup"><span data-stu-id="92bdb-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="92bdb-304">Yes</span><span class="sxs-lookup"><span data-stu-id="92bdb-304">Yes</span></span>



 

<span data-ttu-id="92bdb-305">有效的色彩配置檔案類型是由 COLORPROFILETYPE 列舉所提供。</span><span class="sxs-lookup"><span data-stu-id="92bdb-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="92bdb-306">有效的色彩設定檔子類型是由 COLORPROFILESUBTYPE 列舉所提供。</span><span class="sxs-lookup"><span data-stu-id="92bdb-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="92bdb-307">下表顯示有效的配置檔案類型/子類型組合。</span><span class="sxs-lookup"><span data-stu-id="92bdb-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="92bdb-308">COLORPROFILETYPE</span><span class="sxs-lookup"><span data-stu-id="92bdb-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="92bdb-309">有效的 COLORPROFILESUBTYPE</span><span class="sxs-lookup"><span data-stu-id="92bdb-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="92bdb-310">備註</span><span class="sxs-lookup"><span data-stu-id="92bdb-310">Notes</span></span>

<span data-ttu-id="92bdb-311">裝置預設</span><span class="sxs-lookup"><span data-stu-id="92bdb-311">Device Default</span></span>

<span data-ttu-id="92bdb-312">全域預設值</span><span class="sxs-lookup"><span data-stu-id="92bdb-312">Global Default</span></span>

<span data-ttu-id="92bdb-313">預定用途</span><span class="sxs-lookup"><span data-stu-id="92bdb-313">Intended Use</span></span>

<span data-ttu-id="92bdb-314">預定用途</span><span class="sxs-lookup"><span data-stu-id="92bdb-314">Intended Use</span></span>

<span data-ttu-id="92bdb-315">CPT \_ ICC</span><span class="sxs-lookup"><span data-stu-id="92bdb-315">CPT\_ICC</span></span>

<span data-ttu-id="92bdb-316">CPST \_ 無</span><span class="sxs-lookup"><span data-stu-id="92bdb-316">CPST\_NONE</span></span>

<span data-ttu-id="92bdb-317">取得/設定與裝置相關聯的預設 ICC 設定檔</span><span class="sxs-lookup"><span data-stu-id="92bdb-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="92bdb-318">CPST \_ RGBWorkingSpace 或 CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="92bdb-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="92bdb-319">取得/設定 ICC 設定檔為全域 RGB 或自訂工作空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="92bdb-320">請參閱附註。</span><span class="sxs-lookup"><span data-stu-id="92bdb-320">See Note.</span></span>

<span data-ttu-id="92bdb-321">COLORPROFILETYPE CPT \_ ICC 和 CPT \_ DMP 互相排斥。</span><span class="sxs-lookup"><span data-stu-id="92bdb-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="92bdb-322">您為指定工作空間設定的預設色彩設定檔 (RGB 或自訂) 可以是 ICC 設定檔或 DMP 設定檔，但不能同時為兩者。</span><span class="sxs-lookup"><span data-stu-id="92bdb-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="92bdb-323">CPT \_ DMP</span><span class="sxs-lookup"><span data-stu-id="92bdb-323">CPT\_DMP</span></span>

<span data-ttu-id="92bdb-324">CPST \_ 無</span><span class="sxs-lookup"><span data-stu-id="92bdb-324">CPST\_NONE</span></span>

<span data-ttu-id="92bdb-325">取得/設定與裝置相關聯的預設 DMP 設定檔</span><span class="sxs-lookup"><span data-stu-id="92bdb-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="92bdb-326">CPST \_ RGBWorkingSpace 或 CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="92bdb-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="92bdb-327">取得/設定 DMP 設定檔為全域 RGB 或自訂工作空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="92bdb-328">請參閱附註。</span><span class="sxs-lookup"><span data-stu-id="92bdb-328">See Note.</span></span>

<span data-ttu-id="92bdb-329">COLORPROFILETYPE CPT \_ ICC 和 CPT \_ DMP 互相排斥。</span><span class="sxs-lookup"><span data-stu-id="92bdb-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="92bdb-330">您為指定工作空間設定的預設色彩設定檔 (RGB 或自訂) 可以是 ICC 設定檔或 DMP 設定檔，但不能同時為兩者。</span><span class="sxs-lookup"><span data-stu-id="92bdb-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="92bdb-331">呼叫 WcsSetDefaultColorProfile 以將 DMP 設定檔設定為 RGB 工作空間或自訂工作空間的預設設定檔時，只有類型為 RGBVirtualDevice、LCD 或 CRT 的 DMP 設定檔是有效的。</span><span class="sxs-lookup"><span data-stu-id="92bdb-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="92bdb-332">當呼叫 WcsSetDefaultColorProfile 來將 ICC 設定檔設定為 RGB 工作空間或自訂工作空間的預設設定檔時，只有其類別為 "spac" 或 "" 且色彩空間為 "RGB" 的 ICC 設定檔才有效。</span><span class="sxs-lookup"><span data-stu-id="92bdb-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="92bdb-333">此架構是根據上述列舉和資料表中所述的作業需求所設計。</span><span class="sxs-lookup"><span data-stu-id="92bdb-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="92bdb-334">設定檔管理公用 API 層</span><span class="sxs-lookup"><span data-stu-id="92bdb-334">Profile management public API layer</span></span>

<span data-ttu-id="92bdb-335">由於舊版 ICM2 Api 不支援設定檔管理範圍，因此需要一組新的 WCS 設定檔管理 Api，將設定檔管理範圍定義為全系統或目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="92bdb-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="92bdb-336">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-336">?</span></span> <span data-ttu-id="92bdb-337">舊版 ICM2 Api 會繼續支援以提供回溯相容性，並使用對呼叫隱含的設定檔管理範圍。</span><span class="sxs-lookup"><span data-stu-id="92bdb-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="92bdb-338">o ICM2 可在目前使用者範圍上運作的 Api？</span><span class="sxs-lookup"><span data-stu-id="92bdb-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="92bdb-339">這是針對在 WCS 設定檔管理中，系統範圍和目前使用者範圍所支援的作業。</span><span class="sxs-lookup"><span data-stu-id="92bdb-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="92bdb-340">舊版 ICM2 Api 會以目前使用者的設定檔管理範圍，在新的 WCS Api 上呼叫。</span><span class="sxs-lookup"><span data-stu-id="92bdb-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="92bdb-341">從使用者的角度來看，這是合理的，因為這可讓您從繼承應用程式進行個別使用者的設定，也可以在 LUA 內容中執行大部分的作業。</span><span class="sxs-lookup"><span data-stu-id="92bdb-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="92bdb-342">o ICM2 可在整個系統範圍內運作的 Api？</span><span class="sxs-lookup"><span data-stu-id="92bdb-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="92bdb-343">這適用于作業 (安裝設定檔和卸載設定檔，) 僅支援全系統範圍。</span><span class="sxs-lookup"><span data-stu-id="92bdb-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="92bdb-344">不會建立新的 WCS 設定檔管理 Api，而且可以修改現有的 Api。</span><span class="sxs-lookup"><span data-stu-id="92bdb-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="92bdb-345">設定檔管理作業的基礎會在下列設定資料實體上運作，以建立色彩處理演算法的內容以提供色彩管理功能。</span><span class="sxs-lookup"><span data-stu-id="92bdb-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="92bdb-346">它們是裝置特定或全域 (裝置獨立) 設定。</span><span class="sxs-lookup"><span data-stu-id="92bdb-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="92bdb-347">o 裝置特定設定資料：？</span><span class="sxs-lookup"><span data-stu-id="92bdb-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="92bdb-348">與特定裝置相關聯的配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="92bdb-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="92bdb-349">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-349">?</span></span> <span data-ttu-id="92bdb-350">與裝置相關聯之不同配置檔案類型的預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="92bdb-351">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-351">?</span></span> <span data-ttu-id="92bdb-352">用於列舉的設定檔的比對模式。</span><span class="sxs-lookup"><span data-stu-id="92bdb-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="92bdb-353">o Global configuration data：？</span><span class="sxs-lookup"><span data-stu-id="92bdb-353">o Global configuration data: ?</span></span> <span data-ttu-id="92bdb-354">系統中安裝的配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="92bdb-354">List of profiles installed in the system.</span></span> <span data-ttu-id="92bdb-355">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-355">?</span></span> <span data-ttu-id="92bdb-356">不同配置檔案類型的全域預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="92bdb-356">Global default profile for different profile types.</span></span> <span data-ttu-id="92bdb-357">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-357">?</span></span> <span data-ttu-id="92bdb-358">設定資料儲存體的基礎執行會在設定資料的儲存體範圍內進行， (裝置獨立或裝置特定的) （可以是全系統或目前的使用者）。</span><span class="sxs-lookup"><span data-stu-id="92bdb-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="92bdb-359">這與設定檔管理範圍不同。</span><span class="sxs-lookup"><span data-stu-id="92bdb-359">This is different from profile management scope.</span></span> <span data-ttu-id="92bdb-360">如果該作業目前的使用者設定不存在，則具有目前使用者設定檔管理範圍的作業可能會從整個系統的儲存範圍中讀取。</span><span class="sxs-lookup"><span data-stu-id="92bdb-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="92bdb-361">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-361">?</span></span> <span data-ttu-id="92bdb-362">ICM2/WCS API 層會在此儲存層中呼叫，以使用適當的儲存體範圍來取得和設定資料。</span><span class="sxs-lookup"><span data-stu-id="92bdb-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="92bdb-363">儲存層對設定檔管理範圍是透明的。</span><span class="sxs-lookup"><span data-stu-id="92bdb-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="92bdb-364">結合目前使用者和全系統儲存範圍的資料，根據 API 呼叫端所指定的設定檔管理範圍來建立或更新設定的邏輯。</span><span class="sxs-lookup"><span data-stu-id="92bdb-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="92bdb-365">此邏輯存在於 ICM2/WCS API 層中。</span><span class="sxs-lookup"><span data-stu-id="92bdb-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="92bdb-366">裝置特定的儲存層</span><span class="sxs-lookup"><span data-stu-id="92bdb-366">Device-specific storage layer</span></span>

<span data-ttu-id="92bdb-367">不同裝置類別的儲存體（例如列印、捕捉或顯示）可能會彼此不同。</span><span class="sxs-lookup"><span data-stu-id="92bdb-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="92bdb-368">例如，您必須使用標準列印 Api （例如 SetPrinterDataEx 和 GetPrinterDataEx）來儲存列印裝置的設定資料，讓設定檔得以複製，並在點對列印連線期間將設定傳送至用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="92bdb-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="92bdb-369">?</span><span class="sxs-lookup"><span data-stu-id="92bdb-369">?</span></span> <span data-ttu-id="92bdb-370">這一層會使用一般預先定義的介面來匯出開啟存放區、取得資料、設定資料和關閉存放區的功能，讓設定檔管理設定儲存層可以在這些介面中呼叫這些介面，同時對該裝置的資料儲存方式是透明的。</span><span class="sxs-lookup"><span data-stu-id="92bdb-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="92bdb-371">下圖說明這個架構。</span><span class="sxs-lookup"><span data-stu-id="92bdb-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="92bdb-372">設定檔管理公用 API 層</span><span class="sxs-lookup"><span data-stu-id="92bdb-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="92bdb-373">$ {ROWSPAN2} $Legacy ICM2 Api 來進行僅支援 Vista 中全系統設定檔管理範圍的作業 (安裝、卸載，以及取得色彩目錄) 。</span><span class="sxs-lookup"><span data-stu-id="92bdb-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="92bdb-374">他們會以適當的儲存體範圍呼叫設定儲存層。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-375">在 Vista 中支援全系統和目前使用者設定檔管理範圍之作業的舊版 ICM2 API (安裝、卸載和取得色彩目錄) 以外的所有作業。</span><span class="sxs-lookup"><span data-stu-id="92bdb-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="92bdb-376">它們會在目前使用者的範圍上隱含地運作，並以目前使用者的設定檔管理範圍呼叫新的 WCS API。</span><span class="sxs-lookup"><span data-stu-id="92bdb-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="92bdb-377">新的 WCS API，具備全系統和目前的使用者設定檔管理範圍支援。</span><span class="sxs-lookup"><span data-stu-id="92bdb-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="92bdb-378">他們會以適當的儲存體範圍呼叫設定儲存層。</span><span class="sxs-lookup"><span data-stu-id="92bdb-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="92bdb-379">設定檔管理設定儲存層</span><span class="sxs-lookup"><span data-stu-id="92bdb-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="92bdb-380">與裝置無關的全域設定常式</span><span class="sxs-lookup"><span data-stu-id="92bdb-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="92bdb-381">裝置特定設定常式</span><span class="sxs-lookup"><span data-stu-id="92bdb-381">Device-specific configuration routines</span></span>

<span data-ttu-id="92bdb-382">$ {ROWSPAN3} $Profile 安裝和與裝置無關的預設設定檔設定管理，其支援全系統和目前的使用者儲存範圍。 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92bdb-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="92bdb-383">裝置關聯和裝置特定的預設設定檔設定管理，在全系統和目前使用者的儲存體範圍中受到支援。</span><span class="sxs-lookup"><span data-stu-id="92bdb-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="92bdb-384">Device-Specific 儲存層</span><span class="sxs-lookup"><span data-stu-id="92bdb-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="92bdb-385">列印特定的儲存體</span><span class="sxs-lookup"><span data-stu-id="92bdb-385">Print specific storage</span></span>

<span data-ttu-id="92bdb-386">顯示特定的儲存體</span><span class="sxs-lookup"><span data-stu-id="92bdb-386">Display specific storage</span></span>

<span data-ttu-id="92bdb-387">捕獲特定儲存體</span><span class="sxs-lookup"><span data-stu-id="92bdb-387">Capture specific storage</span></span>



 

<span data-ttu-id="92bdb-388">在 Vista 中僅支援全系統設定檔管理範圍之作業的舊版 ICM2 Api 沒有任何行為變更。</span><span class="sxs-lookup"><span data-stu-id="92bdb-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="92bdb-389">安裝和卸載作業落在此類別中。</span><span class="sxs-lookup"><span data-stu-id="92bdb-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="92bdb-390">適用于支援全系統和目前使用者設定檔管理範圍之作業的舊版 ICM2 Api，其行為會變更為 [查詢] 和 [設定目前使用者] 設定。</span><span class="sxs-lookup"><span data-stu-id="92bdb-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="92bdb-391">安裝和卸載以外的所有作業都屬於此類別。</span><span class="sxs-lookup"><span data-stu-id="92bdb-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




