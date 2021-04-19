---
title: 裝置校正和特性函數
description: 下列函式適用于撰寫裝置校正，以及安裝和校準色彩顯示裝置（例如監視器和印表機）所需的特性工具。
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS) ，函數
- WCS (Windows 色彩系統) ，函數
- 影像色彩管理，函數
- 色彩管理，函數
- 色彩，函數
- WCS 參考，函數
- WCS、函數的參考
- Windows Color System (WCS) 、裝置校正
- WCS (Windows 色彩系統) ，裝置校正
- 影像色彩管理、裝置校正
- 色彩管理，裝置校正
- 色彩，裝置校正
- WCS 參考，裝置校正
- WCS、裝置校正的參考
- Windows Color System (WCS) ，特性
- WCS (Windows 色彩系統) ，特性
- 影像色彩管理，特性
- 色彩管理，特性
- 色彩，特性
- WCS 參考，特性
- WCS 的參考，特性
- 裝置校正
- 校準
- 表徵
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106974827"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="49a76-127">裝置校正和特性函數</span><span class="sxs-lookup"><span data-stu-id="49a76-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="49a76-128">下列函式適用于撰寫裝置校正，以及安裝和校準色彩顯示裝置（例如監視器和印表機）所需的特性工具。</span><span class="sxs-lookup"><span data-stu-id="49a76-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="49a76-129">函式</span><span class="sxs-lookup"><span data-stu-id="49a76-129">Function</span></span> | <span data-ttu-id="49a76-130">描述</span><span class="sxs-lookup"><span data-stu-id="49a76-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="49a76-131">**CloseColorProfile**</span><span class="sxs-lookup"><span data-stu-id="49a76-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="49a76-132">關閉開啟的設定檔控制碼。</span><span class="sxs-lookup"><span data-stu-id="49a76-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="49a76-133">**CreateDeviceLinkProfile**</span><span class="sxs-lookup"><span data-stu-id="49a76-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="49a76-134">使用指定的意圖，從一組色彩設定檔建立國際色彩協會 (ICC) *裝置連結設定檔* 。</span><span class="sxs-lookup"><span data-stu-id="49a76-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="49a76-135">**GetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="49a76-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="49a76-136">從指定的色彩設定檔中指定的已標記設定檔元素，將資料複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="49a76-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="49a76-137">**GetColorProfileElementTag**</span><span class="sxs-lookup"><span data-stu-id="49a76-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="49a76-138">在指定的國際色彩協會)  (的標記資料表中，抓取 *dwIndex* 所指定的標籤名稱，其中 *dwIndex* 是該資料表中以單一為基礎的索引。</span><span class="sxs-lookup"><span data-stu-id="49a76-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="49a76-139">**GetColorProfileFromHandle**</span><span class="sxs-lookup"><span data-stu-id="49a76-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="49a76-140">針對開啟色彩設定檔的控制碼，抓取色彩設定檔內容。</span><span class="sxs-lookup"><span data-stu-id="49a76-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="49a76-141">**GetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="49a76-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="49a76-142">從 ICC 色彩設定檔或 WCS XML 設定檔，抓取或衍生 ICC 標頭結構。</span><span class="sxs-lookup"><span data-stu-id="49a76-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="49a76-143">驅動程式和應用程式應該假設傳回 **TRUE** 只表示傳回的是正確結構化的標頭。</span><span class="sxs-lookup"><span data-stu-id="49a76-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="49a76-144">每個標記仍然需要使用舊版 ICM2 Api 或 XML 架構 Api 獨立進行驗證。</span><span class="sxs-lookup"><span data-stu-id="49a76-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="49a76-145">**GetCountColorProfileElements**</span><span class="sxs-lookup"><span data-stu-id="49a76-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="49a76-146">抓取指定色彩設定檔中的已標記元素數目。</span><span class="sxs-lookup"><span data-stu-id="49a76-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="49a76-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="49a76-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="49a76-148">從指定的 ICC 色彩設定檔抓取 PostScript 層級2色彩轉譯字典。</span><span class="sxs-lookup"><span data-stu-id="49a76-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="49a76-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="49a76-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="49a76-150">從 ICC 色彩設定檔抓取 PostScript 層級2色彩轉譯 [意圖](r.md) 。</span><span class="sxs-lookup"><span data-stu-id="49a76-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="49a76-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="49a76-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="49a76-152">從 ICC 色彩設定檔抓取 PostScript 層級 2 [色彩空間](c.md) 陣列。</span><span class="sxs-lookup"><span data-stu-id="49a76-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="49a76-153">**IsColorProfileTagPresent**</span><span class="sxs-lookup"><span data-stu-id="49a76-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="49a76-154">報告指定的國際色彩協會 (ICC) 標記是否存在於指定的色彩設定檔中。</span><span class="sxs-lookup"><span data-stu-id="49a76-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="49a76-155">**IsColorProfileValid**</span><span class="sxs-lookup"><span data-stu-id="49a76-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="49a76-156">可讓您判斷指定的設定檔是否為有效的國際色彩協會 (ICC) 設定檔，或可用於色彩管理的有效 Windows 色彩系統 (WCS) 設定檔控制碼。</span><span class="sxs-lookup"><span data-stu-id="49a76-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="49a76-157">**OpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="49a76-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="49a76-158">建立指定之色彩設定檔的控制碼。</span><span class="sxs-lookup"><span data-stu-id="49a76-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="49a76-159">然後，控制碼可用於其他設定檔管理功能。</span><span class="sxs-lookup"><span data-stu-id="49a76-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="49a76-160">**SetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="49a76-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="49a76-161">設定 ICC 色彩設定檔中已標記之設定檔元素的元素資料。</span><span class="sxs-lookup"><span data-stu-id="49a76-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="49a76-162">**SetColorProfileElementReference**</span><span class="sxs-lookup"><span data-stu-id="49a76-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="49a76-163">在指定的 ICC 色彩設定檔中，建立參考與現有標記相同資料的新標記。</span><span class="sxs-lookup"><span data-stu-id="49a76-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="49a76-164">**SetColorProfileElementSize**</span><span class="sxs-lookup"><span data-stu-id="49a76-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="49a76-165">設定 ICC 色彩設定檔中標記專案的大小。</span><span class="sxs-lookup"><span data-stu-id="49a76-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="49a76-166">**SetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="49a76-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="49a76-167">設定指定之 ICC 色彩設定檔中的標頭資料。</span><span class="sxs-lookup"><span data-stu-id="49a76-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="49a76-168">**WcsGetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="49a76-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="49a76-169">決定是否啟用顯示校正狀態的系統管理。</span><span class="sxs-lookup"><span data-stu-id="49a76-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="49a76-170">**WcsSetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="49a76-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="49a76-171">決定是否啟用顯示校正狀態的系統管理。</span><span class="sxs-lookup"><span data-stu-id="49a76-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




