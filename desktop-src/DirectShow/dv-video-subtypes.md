---
description: 針對 DV 影片定義了許多子類型。 每個都有 FOURCC 碼和對應的 GUID 值。 並非所有這些格式都受到支援;如需詳細資訊，請參閱「備註」一節。
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: 'DV 影片子類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984787"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="72fb9-105">DV 影片子類型</span><span class="sxs-lookup"><span data-stu-id="72fb9-105">DV Video Subtypes</span></span>

<span data-ttu-id="72fb9-106">針對 DV 影片定義了許多子類型。</span><span class="sxs-lookup"><span data-stu-id="72fb9-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="72fb9-107">每個都有 FOURCC 碼和對應的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="72fb9-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="72fb9-108">並非所有這些格式都受到支援;如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="72fb9-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="72fb9-109">取用者格式</span><span class="sxs-lookup"><span data-stu-id="72fb9-109">Consumer Formats</span></span>



| <span data-ttu-id="72fb9-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="72fb9-110">FOURCC</span></span> | <span data-ttu-id="72fb9-111">GUID</span><span class="sxs-lookup"><span data-stu-id="72fb9-111">GUID</span></span>               | <span data-ttu-id="72fb9-112">資料速率</span><span class="sxs-lookup"><span data-stu-id="72fb9-112">Data Rate</span></span> | <span data-ttu-id="72fb9-113">Description</span><span class="sxs-lookup"><span data-stu-id="72fb9-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="72fb9-114">'dvsl'</span><span class="sxs-lookup"><span data-stu-id="72fb9-114">'dvsl'</span></span> | <span data-ttu-id="72fb9-115">MEDIASUBTYPE \_ dvsl</span><span class="sxs-lookup"><span data-stu-id="72fb9-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="72fb9-116">12.5 Mbps</span><span class="sxs-lookup"><span data-stu-id="72fb9-116">12.5 Mbps</span></span> | <span data-ttu-id="72fb9-117">SD-DVCR (525-60 或 625-50) </span><span class="sxs-lookup"><span data-stu-id="72fb9-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="72fb9-118">'dvsd'</span><span class="sxs-lookup"><span data-stu-id="72fb9-118">'dvsd'</span></span> | <span data-ttu-id="72fb9-119">MEDIASUBTYPE \_ dvsd</span><span class="sxs-lookup"><span data-stu-id="72fb9-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="72fb9-120">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="72fb9-120">25 Mbps</span></span>   | <span data-ttu-id="72fb9-121">SDL-DVCR (525-60 或 625-50) </span><span class="sxs-lookup"><span data-stu-id="72fb9-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="72fb9-122">'dvhd'</span><span class="sxs-lookup"><span data-stu-id="72fb9-122">'dvhd'</span></span> | <span data-ttu-id="72fb9-123">MEDIASUBTYPE \_ dvhd</span><span class="sxs-lookup"><span data-stu-id="72fb9-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="72fb9-124">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="72fb9-124">50 Mbps</span></span>   | <span data-ttu-id="72fb9-125">HD-DVCR (1125-60 或 1250-50) </span><span class="sxs-lookup"><span data-stu-id="72fb9-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="72fb9-126">如需這些格式的詳細資訊，請參閱 IEC-61834。</span><span class="sxs-lookup"><span data-stu-id="72fb9-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="72fb9-127">Professional 格式</span><span class="sxs-lookup"><span data-stu-id="72fb9-127">Professional Formats</span></span>



| <span data-ttu-id="72fb9-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="72fb9-128">FOURCC</span></span> | <span data-ttu-id="72fb9-129">GUID</span><span class="sxs-lookup"><span data-stu-id="72fb9-129">GUID</span></span>               | <span data-ttu-id="72fb9-130">資料速率</span><span class="sxs-lookup"><span data-stu-id="72fb9-130">Data Rate</span></span> | <span data-ttu-id="72fb9-131">Description</span><span class="sxs-lookup"><span data-stu-id="72fb9-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="72fb9-132">'dv25'</span><span class="sxs-lookup"><span data-stu-id="72fb9-132">'dv25'</span></span> | <span data-ttu-id="72fb9-133">MEDIASUBTYPE \_ dv25</span><span class="sxs-lookup"><span data-stu-id="72fb9-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="72fb9-134">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="72fb9-134">25 Mbps</span></span>   | <span data-ttu-id="72fb9-135">DVCPRO 25 (525-60 或 625-50) 。</span><span class="sxs-lookup"><span data-stu-id="72fb9-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="72fb9-136">'dv50'</span><span class="sxs-lookup"><span data-stu-id="72fb9-136">'dv50'</span></span> | <span data-ttu-id="72fb9-137">MEDIASUBTYPE \_ dv50</span><span class="sxs-lookup"><span data-stu-id="72fb9-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="72fb9-138">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="72fb9-138">50 Mbps</span></span>   | <span data-ttu-id="72fb9-139">DVCPRO 50 (525-60 或 625-50) </span><span class="sxs-lookup"><span data-stu-id="72fb9-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="72fb9-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="72fb9-140">'dvh1'</span></span> | <span data-ttu-id="72fb9-141">MEDIASUBTYPE \_ dvh1</span><span class="sxs-lookup"><span data-stu-id="72fb9-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="72fb9-142">100 Mbps</span><span class="sxs-lookup"><span data-stu-id="72fb9-142">100 Mbps</span></span>  | <span data-ttu-id="72fb9-143">DVCPRO 100 (1080/60i、1080/50i 或 720/60P) </span><span class="sxs-lookup"><span data-stu-id="72fb9-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="72fb9-144">如需有關 dv25 和 dv50 的詳細資訊，以及有關 dvh1 的詳細資訊，請參閱 [SMPTE] 314M。</span><span class="sxs-lookup"><span data-stu-id="72fb9-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="72fb9-145">其他</span><span class="sxs-lookup"><span data-stu-id="72fb9-145">Miscellaneous</span></span>

<span data-ttu-id="72fb9-146">標頭檔 Uuid 中定義了兩個額外的 DV 子類型。</span><span class="sxs-lookup"><span data-stu-id="72fb9-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="72fb9-147">這些會對應至特定 DV 編解碼器所產生的 FOURCC 碼;它們不會對應至任何定義的 DV 標準。</span><span class="sxs-lookup"><span data-stu-id="72fb9-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="72fb9-148">這些子類型已淘汰，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="72fb9-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="72fb9-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="72fb9-149">FOURCC</span></span> | <span data-ttu-id="72fb9-150">GUID</span><span class="sxs-lookup"><span data-stu-id="72fb9-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="72fb9-151">DVCS</span><span class="sxs-lookup"><span data-stu-id="72fb9-151">'DVCS'</span></span> | <span data-ttu-id="72fb9-152">MEDIASUBTYPE \_ DVCS</span><span class="sxs-lookup"><span data-stu-id="72fb9-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="72fb9-153">'DVSD'</span><span class="sxs-lookup"><span data-stu-id="72fb9-153">'DVSD'</span></span> | <span data-ttu-id="72fb9-154">MEDIASUBTYPE \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="72fb9-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="72fb9-155">備註</span><span class="sxs-lookup"><span data-stu-id="72fb9-155">Remarks</span></span>

<span data-ttu-id="72fb9-156">下表顯示 MSDV 和 UVC 驅動程式支援的資料速率（以每秒 mb 數為單位） (Mbps) 。</span><span class="sxs-lookup"><span data-stu-id="72fb9-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="72fb9-157">作業系統</span><span class="sxs-lookup"><span data-stu-id="72fb9-157">Operating System</span></span>                                                                 | <span data-ttu-id="72fb9-158">MSDV (IEEE 1394) 驅動程式</span><span class="sxs-lookup"><span data-stu-id="72fb9-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="72fb9-159">UVC 驅動程式</span><span class="sxs-lookup"><span data-stu-id="72fb9-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="72fb9-160">Windows XP Service Pack 1 或更早版本</span><span class="sxs-lookup"><span data-stu-id="72fb9-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="72fb9-161">12.5、25</span><span class="sxs-lookup"><span data-stu-id="72fb9-161">12.5, 25</span></span>                | <span data-ttu-id="72fb9-162">無法使用</span><span class="sxs-lookup"><span data-stu-id="72fb9-162">Not available</span></span> |
| <span data-ttu-id="72fb9-163">Windows XP Service Pack 2 或更新版本、Windows Server 2003 Service Pack 1 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="72fb9-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="72fb9-164">12.5、25、50、100</span><span class="sxs-lookup"><span data-stu-id="72fb9-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="72fb9-165">12.5、25</span><span class="sxs-lookup"><span data-stu-id="72fb9-165">12.5, 25</span></span>      |



 

<span data-ttu-id="72fb9-166">若是 25 Mbps 的串流，MSDV 驅動程式在 Windows Vista 之前的 Windows Vista 中已經變更，MSDV 驅動程式一律會將媒體類型設定為 \_ 25-Mbps 串流的 MEDIASUBTYPE dvsd，不論來源是 SDL-DVCR 或 DVCPRO 25。</span><span class="sxs-lookup"><span data-stu-id="72fb9-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="72fb9-167">未使用 ' dv25 ' 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="72fb9-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="72fb9-168">從 Windows Vista 開始，MSDV 驅動程式現在會區分這兩種格式。</span><span class="sxs-lookup"><span data-stu-id="72fb9-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="72fb9-169">針對 SDL DVCR，它會繼續使用 ' dvsd ' 子類型。</span><span class="sxs-lookup"><span data-stu-id="72fb9-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="72fb9-170">針對 DVCPRO 25，它現在會使用 ' dv25 ' 子類型。</span><span class="sxs-lookup"><span data-stu-id="72fb9-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="72fb9-171">DirectShow [DV 分隔](dv-splitter-filter.md) 器和 [DV 影片解碼](dv-video-decoder-filter.md) 篩選器只支援 SDL DVCR 格式。</span><span class="sxs-lookup"><span data-stu-id="72fb9-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="72fb9-172">資料可以是 PAL 或 NTSC。</span><span class="sxs-lookup"><span data-stu-id="72fb9-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="72fb9-173">您可以使用協力廠商篩選或編解碼器來剖析其他 DV 格式，只要 MSDV 或 UVC 驅動程式支援資料速率即可。</span><span class="sxs-lookup"><span data-stu-id="72fb9-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="72fb9-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="72fb9-174">Requirements</span></span>



| <span data-ttu-id="72fb9-175">需求</span><span class="sxs-lookup"><span data-stu-id="72fb9-175">Requirement</span></span> | <span data-ttu-id="72fb9-176">值</span><span class="sxs-lookup"><span data-stu-id="72fb9-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="72fb9-177">標頭</span><span class="sxs-lookup"><span data-stu-id="72fb9-177">Header</span></span><br/> | <dl> <span data-ttu-id="72fb9-178"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="72fb9-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72fb9-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72fb9-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72fb9-180">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="72fb9-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="72fb9-181">MSDV 驅動程式</span><span class="sxs-lookup"><span data-stu-id="72fb9-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="72fb9-182">影片子類型</span><span class="sxs-lookup"><span data-stu-id="72fb9-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




