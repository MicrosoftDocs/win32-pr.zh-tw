---
description: H.264 影片類型
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: H.264 影片類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935612"
---
# <a name="h264-video-types"></a><span data-ttu-id="3582f-103">H.264 影片類型</span><span class="sxs-lookup"><span data-stu-id="3582f-103">H.264 Video Types</span></span>

<span data-ttu-id="3582f-104">下列是針對 h.264 video 定義的媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="3582f-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="3582f-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="3582f-105">Subtype</span></span>                | <span data-ttu-id="3582f-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="3582f-106">FOURCC</span></span> | <span data-ttu-id="3582f-107">Description</span><span class="sxs-lookup"><span data-stu-id="3582f-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="3582f-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="3582f-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="3582f-109">AVC1</span><span class="sxs-lookup"><span data-stu-id="3582f-109">'AVC1'</span></span> | <span data-ttu-id="3582f-110">位流不含開始代碼。</span><span class="sxs-lookup"><span data-stu-id="3582f-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="3582f-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="3582f-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="3582f-112">H264</span><span class="sxs-lookup"><span data-stu-id="3582f-112">'H264'</span></span> | <span data-ttu-id="3582f-113">位流與開始代碼。</span><span class="sxs-lookup"><span data-stu-id="3582f-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="3582f-114">**MEDIASUBTYPE \_ h264**</span><span class="sxs-lookup"><span data-stu-id="3582f-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="3582f-115">h264</span><span class="sxs-lookup"><span data-stu-id="3582f-115">'h264'</span></span> | <span data-ttu-id="3582f-116">相當於 **MEDIASUBTYPE \_ H264**，具有不同的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="3582f-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="3582f-117">**MEDIASUBTYPE \_ X264**</span><span class="sxs-lookup"><span data-stu-id="3582f-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="3582f-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="3582f-118">'X264'</span></span> | <span data-ttu-id="3582f-119">相當於 **MEDIASUBTYPE \_ H264**，具有不同的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="3582f-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="3582f-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="3582f-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="3582f-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="3582f-121">'x264'</span></span> | <span data-ttu-id="3582f-122">相當於 **MEDIASUBTYPE \_ H264**，具有不同的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="3582f-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="3582f-123">這些子類型 Guid 會在 wmcodecdsp 中宣告。</span><span class="sxs-lookup"><span data-stu-id="3582f-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="3582f-124">這些媒體類型的主要差異在於位流中的起始碼是否存在。</span><span class="sxs-lookup"><span data-stu-id="3582f-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="3582f-125">如果子類型為 **MEDIASUBTYPE \_ AVC1**，則位流不會包含開始程式碼。</span><span class="sxs-lookup"><span data-stu-id="3582f-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="3582f-126">使用開始代碼的 h.264 位流</span><span class="sxs-lookup"><span data-stu-id="3582f-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="3582f-127">以無線方式傳輸，或包含在 MPEG 2 程式或傳輸串流中，或在 HD DVD 上錄製的 h.264 bitstreams，會如 ITU-T 的附錄 B 中所述格式化。</span><span class="sxs-lookup"><span data-stu-id="3582f-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="3582f-128">根據此規格，位流包含一連串的網路抽象層單位 (NALUs) ，其中每個單位的開頭都是等於0x000001 或0x00000001 的起始程式碼。</span><span class="sxs-lookup"><span data-stu-id="3582f-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="3582f-129">當位流中有起始程式碼時，會使用下列媒體類型：</span><span class="sxs-lookup"><span data-stu-id="3582f-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3582f-130">主要類型</span><span class="sxs-lookup"><span data-stu-id="3582f-130">Major type</span></span>  | <span data-ttu-id="3582f-131">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="3582f-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="3582f-132">子類型</span><span class="sxs-lookup"><span data-stu-id="3582f-132">Subtypes</span></span>    | <span data-ttu-id="3582f-133">**MEDIASUBTYPE \_H264**、 **MEDIASUBTYPE \_ h264**、 **MEDIASUBTYPE \_ X264** 或 **MEDIASUBTYPE \_ X264**</span><span class="sxs-lookup"><span data-stu-id="3582f-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="3582f-134">格式類型</span><span class="sxs-lookup"><span data-stu-id="3582f-134">Format type</span></span> | <span data-ttu-id="3582f-135">**格式 \_VideoInfo**、 **format \_ VideoInfo2**、 **format \_ MPEG2Video** 或 **GUID \_ Null**</span><span class="sxs-lookup"><span data-stu-id="3582f-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="3582f-136">如果格式類型為 **GUID \_ Null**，則不存在任何格式結構。</span><span class="sxs-lookup"><span data-stu-id="3582f-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="3582f-137">當位流包含開始程式碼時，此處所列的任何格式類型都已足夠，因為此解碼器不需要任何額外的資訊來剖析串流。</span><span class="sxs-lookup"><span data-stu-id="3582f-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="3582f-138">位流已包含此解碼器所需的所有資訊，而起始程式碼可讓解碼器找出每個 NALU 的開頭。</span><span class="sxs-lookup"><span data-stu-id="3582f-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="3582f-139">下列子類型相同：</span><span class="sxs-lookup"><span data-stu-id="3582f-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="3582f-140">位流不含起始碼</span><span class="sxs-lookup"><span data-stu-id="3582f-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="3582f-141">[設定] 容器格式會儲存不含起始代碼的 h.264 資料。</span><span class="sxs-lookup"><span data-stu-id="3582f-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="3582f-142">相反地，每個 NALU 的前面都會加上長度欄位，這會提供 NALU 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3582f-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="3582f-143">長度欄位的大小可能會有所不同，但通常是1、2或4個位元組。</span><span class="sxs-lookup"><span data-stu-id="3582f-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="3582f-144">當位流中沒有起始碼時，會使用下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3582f-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="3582f-145">主要類型</span><span class="sxs-lookup"><span data-stu-id="3582f-145">Major type</span></span>  | <span data-ttu-id="3582f-146">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="3582f-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="3582f-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="3582f-147">Subtype</span></span>     | <span data-ttu-id="3582f-148">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="3582f-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="3582f-149">格式類型</span><span class="sxs-lookup"><span data-stu-id="3582f-149">Format type</span></span> | <span data-ttu-id="3582f-150">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="3582f-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="3582f-151">格式區塊是 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="3582f-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="3582f-152">應填入此結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3582f-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="3582f-153">**hdr**：描述位流的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構。</span><span class="sxs-lookup"><span data-stu-id="3582f-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="3582f-154">結構的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 部分之後不會有色彩表，而且 **biClrUsed** 必須為零。</span><span class="sxs-lookup"><span data-stu-id="3582f-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="3582f-155">**dwStartTimeCode**：未使用。</span><span class="sxs-lookup"><span data-stu-id="3582f-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="3582f-156">設定為零。</span><span class="sxs-lookup"><span data-stu-id="3582f-156">Set to zero.</span></span>
-   <span data-ttu-id="3582f-157">**cbSequenceHeader**： **dwSequenceHeader** 陣列的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3582f-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="3582f-158">**dwProfile**：指定 h.264 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3582f-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="3582f-159">**dwLevel**：指定 h.264 層級。</span><span class="sxs-lookup"><span data-stu-id="3582f-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="3582f-160">**dwFlags**：每個 **NALU** 之前出現的長度欄位所使用的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3582f-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="3582f-161">[長度] 欄位表示下列 NALU 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3582f-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="3582f-162">例如，如果 **dwFlags** 是4，則每個 NALU 的前面都會加上4個位元組的長度欄位。</span><span class="sxs-lookup"><span data-stu-id="3582f-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="3582f-163">有效的值為1、2和4。</span><span class="sxs-lookup"><span data-stu-id="3582f-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="3582f-164">**dwSequenceHeader**：一個位元組陣列，其中可能包含 sequence 參數集 (SPS) ，以及 (PPS) NALUs 的圖片參數集。</span><span class="sxs-lookup"><span data-stu-id="3582f-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="3582f-165">「配置」容器可能會包含 sequence 參數集 (SPS) 或圖片參數集 (PPS) 作為檔案標頭中的特殊 NAL 單位或個別資料流程 (不同于影片串流) 。</span><span class="sxs-lookup"><span data-stu-id="3582f-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="3582f-166">當建立格式時，媒體類型可以在 **dwSequenceHeader** 陣列中指定 SPS 和 PPS NAL 單位。</span><span class="sxs-lookup"><span data-stu-id="3582f-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="3582f-167">如果 **cbSequenceHeader** 大於零，則 **dwSequenceHeader** 是位元組陣列的開頭，其中包含 SPS 和 PPS NALUs （以2位元組長度欄位分隔），而所有以網路位元組順序排列， (位元組由大到小的) 。</span><span class="sxs-lookup"><span data-stu-id="3582f-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="3582f-168">您可以同時具有 SPS 和 PPS，而不是其中一個類型，或無。</span><span class="sxs-lookup"><span data-stu-id="3582f-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="3582f-169">您可以檢查 NALU 本身的 **nal \_ unit \_ type** 欄位來判斷每個 NALU 的實際型別。</span><span class="sxs-lookup"><span data-stu-id="3582f-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="3582f-170">使用此媒體類型時，每個媒體範例都會從 NALU 的開頭開始，而 NAL 的單位則不會跨越樣本。</span><span class="sxs-lookup"><span data-stu-id="3582f-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="3582f-171">這可讓解碼器從資料損毀或捨棄的範例復原。</span><span class="sxs-lookup"><span data-stu-id="3582f-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



