---
title: 'IMAPI.EXE 資料類型 (Imapi2) '
description: 光學媒體和相關聯裝置的規格會定義專案的範圍值，例如 DVD 結構描述、光碟資訊描述和功能頁面大小。
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7793bab123e2939bdc2f5a68bb705d7468da5666
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966146"
---
# <a name="imapi-data-types"></a><span data-ttu-id="45a3c-115">IMAPI.EXE 資料類型</span><span class="sxs-lookup"><span data-stu-id="45a3c-115">IMAPI Data Types</span></span>

<span data-ttu-id="45a3c-116">光學媒體和相關聯裝置的規格會定義專案的範圍值，例如 DVD 結構描述、光碟資訊描述和功能頁面大小。</span><span class="sxs-lookup"><span data-stu-id="45a3c-116">Specifications for optical media and associated devices define range values for items such as the DVD structure description, disc information description, and feature page size.</span></span> <span data-ttu-id="45a3c-117">IMAPI.EXE 會定義下列不帶正負號的長整數 (ULONG) 強制範圍值限制的類型。</span><span class="sxs-lookup"><span data-stu-id="45a3c-117">IMAPI defines the following unsigned long integer (ULONG) types that enforce range value limits.</span></span> <span data-ttu-id="45a3c-118">這些類型會嚴格定義為參數的最佳 IDL 驗證，以及做為相關呼叫端的檔，以提供特定資料傳輸作業的上限。</span><span class="sxs-lookup"><span data-stu-id="45a3c-118">These types are defined strictly for optimal IDL validation of parameters and as a documentation aid to callers regarding the upper limits for certain data transfer operations available.</span></span>


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| <span data-ttu-id="45a3c-119">資料類型</span><span class="sxs-lookup"><span data-stu-id="45a3c-119">Data type</span></span>                                                                                                                                  | <span data-ttu-id="45a3c-120">描述</span><span class="sxs-lookup"><span data-stu-id="45a3c-120">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45a3c-121"><span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ IMAPI2 \_ DVD \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="45a3c-121"><span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG\_IMAPI2\_DVD\_STRUCTURE**</span></span>                | <span data-ttu-id="45a3c-122">範圍：0、65535 (0、0x0000FFFF) </span><span class="sxs-lookup"><span data-stu-id="45a3c-122">Range: 0,65535 (0,0x0000FFFF)</span></span><br/> <span data-ttu-id="45a3c-123">因為有兩個位元組的配置欄位，所以 DVD 結構限制為64KB。</span><span class="sxs-lookup"><span data-stu-id="45a3c-123">The DVD structure is limited to 64KB due to a two-byte allocation field.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="45a3c-124"><span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**ULONG \_ IMAPI2 \_ 介面卡 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="45a3c-124"><span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**ULONG\_IMAPI2\_ADAPTER\_DESCRIPTOR**</span></span> | <span data-ttu-id="45a3c-125">範圍：0、268435455 (0、0x0FFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="45a3c-125">Range: 0,268435455 (0,0x0FFFFFFF)</span></span><br/> <span data-ttu-id="45a3c-126">介面卡描述項的大小不會以隱含方式限制。</span><span class="sxs-lookup"><span data-stu-id="45a3c-126">The adapter descriptor is not implicitly limited in size.</span></span><br/>                                                                                                                                                                                                |
| <span data-ttu-id="45a3c-127"><span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**ULONG \_ IMAPI2 \_ 裝置 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="45a3c-127"><span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**ULONG\_IMAPI2\_DEVICE\_DESCRIPTOR**</span></span>    | <span data-ttu-id="45a3c-128">範圍：0、268435455 (0、0x0FFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="45a3c-128">Range: 0,268435455 (0,0x0FFFFFFF)</span></span><br/> <span data-ttu-id="45a3c-129">裝置描述項的大小不會以隱含方式限制。</span><span class="sxs-lookup"><span data-stu-id="45a3c-129">The device descriptor is not implicitly limited in size.</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="45a3c-130"><span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG \_ IMAPI2 \_ 光碟 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="45a3c-130"><span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**ULONG\_IMAPI2\_DISC\_INFORMATION**</span></span>       | <span data-ttu-id="45a3c-131">範圍：0、65538 (0、0x00010002) </span><span class="sxs-lookup"><span data-stu-id="45a3c-131">Range: 0,65538 (0,0x00010002)</span></span><br/> <span data-ttu-id="45a3c-132">[大小] 欄位的光碟資訊限制為64KB 加2個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-132">Disc information is limited to 64KB plus 2 bytes for the size field.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="45a3c-133"><span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG \_ IMAPI2 \_ 追蹤 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="45a3c-133"><span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG\_IMAPI2\_TRACK\_INFORMATION**</span></span>    | <span data-ttu-id="45a3c-134">範圍：0、65538 (0、0x00010002) </span><span class="sxs-lookup"><span data-stu-id="45a3c-134">Range: 0,65538 (0,0x00010002)</span></span><br/> <span data-ttu-id="45a3c-135">[大小] 欄位的追蹤資訊限制為64KB 加2個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-135">Track information is limited to 64KB plus 2 bytes for the size field.</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="45a3c-136"><span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**ULONG \_ IMAPI2 \_ 功能 \_ 頁面**</span><span class="sxs-lookup"><span data-stu-id="45a3c-136"><span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**ULONG\_IMAPI2\_FEATURE\_PAGE**</span></span>                   | <span data-ttu-id="45a3c-137">範圍： 0256 (0，0x00000100) </span><span class="sxs-lookup"><span data-stu-id="45a3c-137">Range: 0,256 (0,0x00000100)</span></span><br/> <span data-ttu-id="45a3c-138">單一功能頁面的限制為256個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-138">A single feature page is limited to 256 bytes.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="45a3c-139"><span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**ULONG \_ IMAPI2 \_ 模式 \_ 頁面**</span><span class="sxs-lookup"><span data-stu-id="45a3c-139"><span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**ULONG\_IMAPI2\_MODE\_PAGE**</span></span>                            | <span data-ttu-id="45a3c-140">範圍： 0257 (0，0x00000101) </span><span class="sxs-lookup"><span data-stu-id="45a3c-140">Range: 0,257 (0,0x00000101)</span></span><br/> <span data-ttu-id="45a3c-141">單一模式頁面的限制為257個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-141">A single mode page is limited to 257 bytes.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="45a3c-142"><span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ IMAPI2 \_ 所有 \_ 功能 \_ 頁面**</span><span class="sxs-lookup"><span data-stu-id="45a3c-142"><span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG\_IMAPI2\_ALL\_FEATURE\_PAGES**</span></span>   | <span data-ttu-id="45a3c-143">範圍：0、65536 (0、0x00010000) </span><span class="sxs-lookup"><span data-stu-id="45a3c-143">Range: 0,65536 (0,0x00010000)</span></span><br/> <span data-ttu-id="45a3c-144">功能的數目限制為兩個位元組的欄位。</span><span class="sxs-lookup"><span data-stu-id="45a3c-144">The number of features is limited to a two-byte field.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="45a3c-145"><span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ IMAPI2 \_ 所有 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="45a3c-145"><span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG\_IMAPI2\_ALL\_PROFILES**</span></span>                   | <span data-ttu-id="45a3c-146">範圍：0、63 (0、0x0000003F) </span><span class="sxs-lookup"><span data-stu-id="45a3c-146">Range: 0,63 (0,0x0000003F)</span></span><br/> <span data-ttu-id="45a3c-147">裝置的設定檔數目是適用于單一功能的設定檔數目。</span><span class="sxs-lookup"><span data-stu-id="45a3c-147">The number of profiles for a device is the number of profiles that fit in a single feature.</span></span> <span data-ttu-id="45a3c-148">每個設定檔都會佔用四個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-148">Each profile occupies four bytes.</span></span> <span data-ttu-id="45a3c-149">單一功能可以保留252個額外的資料位元組，足以儲存最多63個設定檔。</span><span class="sxs-lookup"><span data-stu-id="45a3c-149">A single feature can hold 252 additional bytes of data, enough to store a maximum of 63 profiles.</span></span><br/>                                 |
| <span data-ttu-id="45a3c-150"><span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ IMAPI2 \_ 所有 \_ 模式 \_ 頁面**</span><span class="sxs-lookup"><span data-stu-id="45a3c-150"><span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG\_IMAPI2\_ALL\_MODE\_PAGES**</span></span>            | <span data-ttu-id="45a3c-151">範圍：0、32763 (0、0x00007FFB) </span><span class="sxs-lookup"><span data-stu-id="45a3c-151">Range: 0,32763 (0,0x00007FFB)</span></span><br/> <span data-ttu-id="45a3c-152">裝置的模式頁面計數。</span><span class="sxs-lookup"><span data-stu-id="45a3c-152">Count of the mode pages for a device.</span></span> <span data-ttu-id="45a3c-153">計數（via 模式 \_ SENSE10）受限於雙位元組欄位。</span><span class="sxs-lookup"><span data-stu-id="45a3c-153">The count, via MODE\_SENSE10, is limited to a two-byte field.</span></span><br/> <span data-ttu-id="45a3c-154">模式參數標頭是8個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-154">The mode parameter header is 8 bytes.</span></span> <span data-ttu-id="45a3c-155">每個頁面至少都有兩個位元組。</span><span class="sxs-lookup"><span data-stu-id="45a3c-155">Each page is at least two bytes.</span></span> <span data-ttu-id="45a3c-156">模式頁面的最大數目是32763： (65535-8) /2 四捨五入。</span><span class="sxs-lookup"><span data-stu-id="45a3c-156">The maximum number of mode pages is 32763: (65535 - 8)/2 rounded down.</span></span><br/> |
| <span data-ttu-id="45a3c-157"><span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ IMAPI2 \_ 非零**</span><span class="sxs-lookup"><span data-stu-id="45a3c-157"><span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG\_IMAPI2\_NONZERO**</span></span>                                   | <span data-ttu-id="45a3c-158">範圍：1、2147483647 (1、0x7FFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="45a3c-158">Range: 1,2147483647 (1,0x7FFFFFFF)</span></span><br/> <span data-ttu-id="45a3c-159">泛型非零值，可用來驗證值不是零。</span><span class="sxs-lookup"><span data-stu-id="45a3c-159">Generic nonzero value that can be used to verify that a value is not zero.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="45a3c-160"><span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ IMAPI2 \_ 非 \_ 負值**</span><span class="sxs-lookup"><span data-stu-id="45a3c-160"><span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG\_IMAPI2\_NOT\_NEGATIVE**</span></span>                   | <span data-ttu-id="45a3c-161">範圍：0、2147483647 (0、0x7FFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="45a3c-161">Range: 0, 2147483647 (0,0x7FFFFFFF)</span></span><br/> <span data-ttu-id="45a3c-162">具有非負數值的32位整數。</span><span class="sxs-lookup"><span data-stu-id="45a3c-162">A 32-bit integer with non-negative value.</span></span><br/>                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="45a3c-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="45a3c-163">Requirements</span></span>



| <span data-ttu-id="45a3c-164">需求</span><span class="sxs-lookup"><span data-stu-id="45a3c-164">Requirement</span></span> | <span data-ttu-id="45a3c-165">值</span><span class="sxs-lookup"><span data-stu-id="45a3c-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="45a3c-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45a3c-166">Minimum supported client</span></span><br/> | <span data-ttu-id="45a3c-167">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45a3c-167">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="45a3c-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45a3c-168">Minimum supported server</span></span><br/> | <span data-ttu-id="45a3c-169">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45a3c-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="45a3c-170">標頭</span><span class="sxs-lookup"><span data-stu-id="45a3c-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="45a3c-171"><dt>Imapi2。h</dt></span><span class="sxs-lookup"><span data-stu-id="45a3c-171"><dt>Imapi2.h</dt></span></span> </dl> |



 

 





