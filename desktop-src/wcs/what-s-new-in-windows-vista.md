---
title: Windows Vista 的新功能
description: 映射色彩管理的版本 1.0 (ICM) 已在 Microsoft Windows 95 中提供，並在 Windows 裝置內容中提供基本的色彩管理功能。
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS) ，Windows Vista
- WCS (Windows Color System) ，Windows Vista
- 影像色彩管理，Windows Vista
- 色彩管理，Windows Vista
- 色彩，Windows Vista
- Windows Color System (WCS) ，作業系統
- WCS (Windows 色彩系統) ，作業系統
- 影像色彩管理，作業系統
- 色彩管理，作業系統
- 色彩，作業系統
- 影像色彩管理 (ICM)
- 'ICM (影像色彩管理) '
- Windows Vista 色彩管理
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "106997592"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="9e446-116">Windows Vista 的新功能</span><span class="sxs-lookup"><span data-stu-id="9e446-116">What's New in Windows Vista</span></span>

<span data-ttu-id="9e446-117">映射色彩管理的版本 1.0 (ICM) 已在 Microsoft Windows 95 中提供，並在 Windows 裝置內容中提供基本的色彩管理功能。</span><span class="sxs-lookup"><span data-stu-id="9e446-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="9e446-118">ICM 版本2.0 已在 Windows 98、Windows Millennium Edition、Windows 2000 和 WindowsXP 中提供，並包含各種在裝置內容以外實行色彩管理的新功能。</span><span class="sxs-lookup"><span data-stu-id="9e446-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="9e446-119">這些新函式適用于需求較高的色彩管理需求，並讓應用程式能更充分掌控色彩管理進程。</span><span class="sxs-lookup"><span data-stu-id="9e446-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="9e446-120">隨著 Windows Vista 的發行，ICM 2.0 現在已包含在 Windows Color System (WCS) 1.0，這會增加更多功能。</span><span class="sxs-lookup"><span data-stu-id="9e446-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="9e446-121">下表列出新的應用程式開發介面 (API) 隨附于 Windows Vista 中。</span><span class="sxs-lookup"><span data-stu-id="9e446-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="9e446-122">Windows Vista 中的新 API 傳送</span><span class="sxs-lookup"><span data-stu-id="9e446-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="9e446-123">列舉</span><span class="sxs-lookup"><span data-stu-id="9e446-123">Enumerations</span></span>

<span data-ttu-id="9e446-124">API 名稱</span><span class="sxs-lookup"><span data-stu-id="9e446-124">API Name</span></span>

<span data-ttu-id="9e446-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9e446-125">Header</span></span>

<span data-ttu-id="9e446-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e446-126">Library</span></span>

[<span data-ttu-id="9e446-127">**COLORDATATYPE**</span><span class="sxs-lookup"><span data-stu-id="9e446-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="9e446-128">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-128">icm.h</span></span>

<span data-ttu-id="9e446-129">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-129">mscms.lib</span></span>

[<span data-ttu-id="9e446-130">**COLORPROFILESUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="9e446-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="9e446-131">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-131">icm.h</span></span>

<span data-ttu-id="9e446-132">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-132">mscms.lib</span></span>

[<span data-ttu-id="9e446-133">**COLORPROFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="9e446-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="9e446-134">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-134">icm.h</span></span>

<span data-ttu-id="9e446-135">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-135">mscms.lib</span></span>

[<span data-ttu-id="9e446-136">**WCS \_ 設定檔 \_ 管理 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="9e446-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="9e446-137">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-137">icm.h</span></span>

<span data-ttu-id="9e446-138">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-138">mscms.lib</span></span>



 



<span data-ttu-id="9e446-139">函式</span><span class="sxs-lookup"><span data-stu-id="9e446-139">Functions</span></span>

<span data-ttu-id="9e446-140">API 名稱</span><span class="sxs-lookup"><span data-stu-id="9e446-140">API Name</span></span>

<span data-ttu-id="9e446-141">標頭</span><span class="sxs-lookup"><span data-stu-id="9e446-141">Header</span></span>

<span data-ttu-id="9e446-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e446-142">Library</span></span>

[<span data-ttu-id="9e446-143">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="9e446-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="9e446-144">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-144">icm.h</span></span>

<span data-ttu-id="9e446-145">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-145">mscms.lib</span></span>

[<span data-ttu-id="9e446-146">**WcsCheckColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="9e446-147">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-147">icm.h</span></span>

<span data-ttu-id="9e446-148">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-148">mscms.lib</span></span>

[<span data-ttu-id="9e446-149">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="9e446-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="9e446-150">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-150">icm.h</span></span>

<span data-ttu-id="9e446-151">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-151">mscms.lib</span></span>

[<span data-ttu-id="9e446-152">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="9e446-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="9e446-153">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-153">icm.h</span></span>

<span data-ttu-id="9e446-154">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-154">mscms.lib</span></span>

[<span data-ttu-id="9e446-155">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="9e446-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="9e446-156">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-156">icm.h</span></span>

<span data-ttu-id="9e446-157">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-157">mscms.lib</span></span>

[<span data-ttu-id="9e446-158">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="9e446-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="9e446-159">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-159">icm.h</span></span>

<span data-ttu-id="9e446-160">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-160">mscms.lib</span></span>

[<span data-ttu-id="9e446-161">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="9e446-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="9e446-162">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-162">icm.h</span></span>

<span data-ttu-id="9e446-163">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-163">mscms.lib</span></span>

[<span data-ttu-id="9e446-164">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="9e446-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="9e446-165">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-165">icm.h</span></span>

<span data-ttu-id="9e446-166">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-166">mscms.lib</span></span>

[<span data-ttu-id="9e446-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="9e446-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="9e446-168">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-168">icm.h</span></span>

<span data-ttu-id="9e446-169">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-169">mscms.lib</span></span>

[<span data-ttu-id="9e446-170">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="9e446-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="9e446-171">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-171">icm.h</span></span>

<span data-ttu-id="9e446-172">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-172">mscms.lib</span></span>

[<span data-ttu-id="9e446-173">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="9e446-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="9e446-174">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-174">icm.h</span></span>

<span data-ttu-id="9e446-175">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-175">mscms.lib</span></span>

[<span data-ttu-id="9e446-176">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="9e446-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="9e446-177">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-177">icm.h</span></span>

<span data-ttu-id="9e446-178">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-178">mscms.lib</span></span>

[<span data-ttu-id="9e446-179">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="9e446-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="9e446-180">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-180">icm.h</span></span>

<span data-ttu-id="9e446-181">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-181">mscms.lib</span></span>

[<span data-ttu-id="9e446-182">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="9e446-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="9e446-183">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-183">icm.h</span></span>

<span data-ttu-id="9e446-184">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-184">mscms.lib</span></span>

[<span data-ttu-id="9e446-185">**WcsTranslateColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="9e446-186">icm。h</span><span class="sxs-lookup"><span data-stu-id="9e446-186">icm.h</span></span>

<span data-ttu-id="9e446-187">mscms .lib</span><span class="sxs-lookup"><span data-stu-id="9e446-187">mscms.lib</span></span>



 



<span data-ttu-id="9e446-188">介面及其函數</span><span class="sxs-lookup"><span data-stu-id="9e446-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="9e446-189">API 名稱</span><span class="sxs-lookup"><span data-stu-id="9e446-189">API Name</span></span>

<span data-ttu-id="9e446-190">標頭</span><span class="sxs-lookup"><span data-stu-id="9e446-190">Header</span></span>

<span data-ttu-id="9e446-191">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e446-191">Library</span></span>

[<span data-ttu-id="9e446-192">**IDeviceModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="9e446-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="9e446-193">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-193">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-194">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-194">N/A</span></span>

[<span data-ttu-id="9e446-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="9e446-196">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-196">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-197">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-197">N/A</span></span>

[<span data-ttu-id="9e446-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span><span class="sxs-lookup"><span data-stu-id="9e446-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="9e446-199">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-199">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-200">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-200">N/A</span></span>

[<span data-ttu-id="9e446-201">**IDeviceModelPlugin：:D eviceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="9e446-202">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-202">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-203">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-203">N/A</span></span>

[<span data-ttu-id="9e446-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span><span class="sxs-lookup"><span data-stu-id="9e446-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="9e446-205">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-205">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-206">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-206">N/A</span></span>

[<span data-ttu-id="9e446-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span><span class="sxs-lookup"><span data-stu-id="9e446-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="9e446-208">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-208">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-209">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-209">N/A</span></span>

[<span data-ttu-id="9e446-210">**IDeviceModelPlugin::GetNeutralAxis**</span><span class="sxs-lookup"><span data-stu-id="9e446-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="9e446-211">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-211">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-212">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-212">N/A</span></span>

[<span data-ttu-id="9e446-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span><span class="sxs-lookup"><span data-stu-id="9e446-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="9e446-214">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-214">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-215">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-215">N/A</span></span>

[<span data-ttu-id="9e446-216">**IDeviceModelPlugin::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="9e446-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="9e446-217">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-217">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-218">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-218">N/A</span></span>

[<span data-ttu-id="9e446-219">**IDeviceModelPlugin::GetPrimarySamples**</span><span class="sxs-lookup"><span data-stu-id="9e446-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="9e446-220">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-220">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-221">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-221">N/A</span></span>

[<span data-ttu-id="9e446-222">**IDeviceModelPlugin：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="9e446-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="9e446-223">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-223">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-224">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-224">N/A</span></span>

[<span data-ttu-id="9e446-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span><span class="sxs-lookup"><span data-stu-id="9e446-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="9e446-226">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-226">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-227">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-227">N/A</span></span>

[<span data-ttu-id="9e446-228">**IGamutMapModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="9e446-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="9e446-229">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-229">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-230">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-230">N/A</span></span>

[<span data-ttu-id="9e446-231">**IGamutMapModelPlugin：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="9e446-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="9e446-232">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-232">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-233">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-233">N/A</span></span>

[<span data-ttu-id="9e446-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="9e446-235">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-235">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-236">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-236">N/A</span></span>



 



<span data-ttu-id="9e446-237">結構</span><span class="sxs-lookup"><span data-stu-id="9e446-237">Structures</span></span>

<span data-ttu-id="9e446-238">API 名稱</span><span class="sxs-lookup"><span data-stu-id="9e446-238">API Name</span></span>

<span data-ttu-id="9e446-239">標頭</span><span class="sxs-lookup"><span data-stu-id="9e446-239">Header</span></span>

<span data-ttu-id="9e446-240">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e446-240">Library</span></span>

[<span data-ttu-id="9e446-241">**BlackInformation**</span><span class="sxs-lookup"><span data-stu-id="9e446-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="9e446-242">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-242">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-243">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-243">N/A</span></span>

[<span data-ttu-id="9e446-244">**GamutBoundaryDescription**</span><span class="sxs-lookup"><span data-stu-id="9e446-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="9e446-245">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-245">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-246">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-246">N/A</span></span>

[<span data-ttu-id="9e446-247">**XYZColorF**</span><span class="sxs-lookup"><span data-stu-id="9e446-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="9e446-248">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-248">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-249">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-249">N/A</span></span>

[<span data-ttu-id="9e446-250">**JChColorF**</span><span class="sxs-lookup"><span data-stu-id="9e446-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="9e446-251">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-251">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-252">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-252">N/A</span></span>

[<span data-ttu-id="9e446-253">**JabColorF**</span><span class="sxs-lookup"><span data-stu-id="9e446-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="9e446-254">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-254">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-255">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-255">N/A</span></span>

[<span data-ttu-id="9e446-256">**GamutShell**</span><span class="sxs-lookup"><span data-stu-id="9e446-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="9e446-257">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-257">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-258">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-258">N/A</span></span>

[<span data-ttu-id="9e446-259">**GamutShellTriangle**</span><span class="sxs-lookup"><span data-stu-id="9e446-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="9e446-260">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-260">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-261">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-261">N/A</span></span>

[<span data-ttu-id="9e446-262">**PrimaryJabColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="9e446-263">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-263">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-264">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-264">N/A</span></span>

[<span data-ttu-id="9e446-265">**PrimaryXYZColors**</span><span class="sxs-lookup"><span data-stu-id="9e446-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="9e446-266">WcsPlugIn。h</span><span class="sxs-lookup"><span data-stu-id="9e446-266">WcsPlugIn.h</span></span>

<span data-ttu-id="9e446-267">N/A</span><span class="sxs-lookup"><span data-stu-id="9e446-267">N/A</span></span>



 

 

 