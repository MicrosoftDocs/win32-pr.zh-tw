---
description: MPEG-2 信號信號媒體類型
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2 信號信號媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909996"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="172a6-103">MPEG-2 信號信號媒體類型</span><span class="sxs-lookup"><span data-stu-id="172a6-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="172a6-104">[Mpeg-2 信號信號](mpeg-2-demultiplexer.md)篩選器可識別下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="172a6-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="172a6-105">輸入類型</span><span class="sxs-lookup"><span data-stu-id="172a6-105">Input Types</span></span>

<span data-ttu-id="172a6-106">主要類型一律為 **媒體型 \_ 串流**。</span><span class="sxs-lookup"><span data-stu-id="172a6-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="172a6-107">子類型可以是下列任何一項。</span><span class="sxs-lookup"><span data-stu-id="172a6-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="172a6-108">GUID</span><span class="sxs-lookup"><span data-stu-id="172a6-108">GUID</span></span>                                             | <span data-ttu-id="172a6-109">Description</span><span class="sxs-lookup"><span data-stu-id="172a6-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="172a6-110">**KSDATAFORMAT \_ 子類型 \_ BDA \_ MPEG2 \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="172a6-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="172a6-111">從廣播驅動程式架構傳輸串流 (BDA) 裝置篩選器。</span><span class="sxs-lookup"><span data-stu-id="172a6-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="172a6-112">MPEG-2 信號信號會將這個子類型視為與 **MEDIASUBTYPE \_ MPEG2 \_ 傳輸** 相同。</span><span class="sxs-lookup"><span data-stu-id="172a6-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="172a6-113">**MEDIASUBTYPE \_ MPEG2 \_ 計畫**</span><span class="sxs-lookup"><span data-stu-id="172a6-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="172a6-114">程式資料流程</span><span class="sxs-lookup"><span data-stu-id="172a6-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="172a6-115">**MEDIASUBTYPE \_ MPEG2 \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="172a6-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="172a6-116">傳輸串流 (TS) ，包含188個位元組的封包</span><span class="sxs-lookup"><span data-stu-id="172a6-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="172a6-117">**MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="172a6-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="172a6-118">具有 "strided" 封包的傳輸資料流程。</span><span class="sxs-lookup"><span data-stu-id="172a6-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="172a6-119">此子類型表示 TS 封包可以填補額外的位元組。</span><span class="sxs-lookup"><span data-stu-id="172a6-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="172a6-120">如需詳細資訊，請參閱 [**MPEG2 \_ 傳輸 \_ STRIDE**](mpeg2-transport-stride.md)。</span><span class="sxs-lookup"><span data-stu-id="172a6-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="172a6-121">針對 strided 傳輸封包 (**MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ stride**) ，每個媒體範例都必須包含整數個傳輸封包，如 [**MPEG2 \_ 傳輸 \_ 跨距**](mpeg2-transport-stride.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="172a6-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="172a6-122">對於所有其他輸入類型，範例界限沒有任何限制;個別的封包可以跨越範例界限。</span><span class="sxs-lookup"><span data-stu-id="172a6-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="172a6-123">輸出型別</span><span class="sxs-lookup"><span data-stu-id="172a6-123">Output Types</span></span>

<span data-ttu-id="172a6-124">MPEG-2 信號信號不會驗證輸出類型;下游篩選器負責剖析它從信號剖析收到的資料。</span><span class="sxs-lookup"><span data-stu-id="172a6-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="172a6-125">不過，下游篩選器通常會接受下列類型做為信號的輸出。</span><span class="sxs-lookup"><span data-stu-id="172a6-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="172a6-126">MPEG 2 區段</span><span class="sxs-lookup"><span data-stu-id="172a6-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="172a6-127">主要類型</span><span class="sxs-lookup"><span data-stu-id="172a6-127">Major Type</span></span></td>
<td><span data-ttu-id="172a6-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="172a6-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="172a6-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="172a6-129">Subtype</span></span></td>
<td><span data-ttu-id="172a6-130">下列任何一項：</span><span class="sxs-lookup"><span data-stu-id="172a6-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="172a6-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>： ATSC 服務資訊。</span><span class="sxs-lookup"><span data-stu-id="172a6-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="172a6-132"><strong>MEDIASUBTYPE_DVB_SI</strong>： Dvb-t 服務資訊。</span><span class="sxs-lookup"><span data-stu-id="172a6-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="172a6-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>：整合服務數位廣播 (ISDB) 服務資訊。</span><span class="sxs-lookup"><span data-stu-id="172a6-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="172a6-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>： mpeg-2 區段資料。</span><span class="sxs-lookup"><span data-stu-id="172a6-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="172a6-135">格式類型</span><span class="sxs-lookup"><span data-stu-id="172a6-135">Format Type</span></span></td>
<td><span data-ttu-id="172a6-136">無</span><span class="sxs-lookup"><span data-stu-id="172a6-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="172a6-137">MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="172a6-137">MPEG-2 Video</span></span>



| <span data-ttu-id="172a6-138">標籤</span><span class="sxs-lookup"><span data-stu-id="172a6-138">Label</span></span> | <span data-ttu-id="172a6-139">值</span><span class="sxs-lookup"><span data-stu-id="172a6-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="172a6-140">主要類型</span><span class="sxs-lookup"><span data-stu-id="172a6-140">Major type</span></span>       | <span data-ttu-id="172a6-141">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="172a6-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="172a6-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="172a6-142">Subtype</span></span>          | <span data-ttu-id="172a6-143">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="172a6-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="172a6-144">格式類型</span><span class="sxs-lookup"><span data-stu-id="172a6-144">Format Type</span></span>      | <span data-ttu-id="172a6-145">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="172a6-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="172a6-146">格式結構</span><span class="sxs-lookup"><span data-stu-id="172a6-146">Format Structure</span></span> | [<span data-ttu-id="172a6-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="172a6-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="172a6-148">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="172a6-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="172a6-149">標籤</span><span class="sxs-lookup"><span data-stu-id="172a6-149">Label</span></span> | <span data-ttu-id="172a6-150">值</span><span class="sxs-lookup"><span data-stu-id="172a6-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="172a6-151">主要類型</span><span class="sxs-lookup"><span data-stu-id="172a6-151">Major type</span></span>       | <span data-ttu-id="172a6-152">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="172a6-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="172a6-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="172a6-153">Subtype</span></span>          | <span data-ttu-id="172a6-154">**MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="172a6-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="172a6-155">格式類型</span><span class="sxs-lookup"><span data-stu-id="172a6-155">Format Type</span></span>      | <span data-ttu-id="172a6-156">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="172a6-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="172a6-157">格式結構</span><span class="sxs-lookup"><span data-stu-id="172a6-157">Format Structure</span></span> | <span data-ttu-id="172a6-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="172a6-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="172a6-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="172a6-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="172a6-160">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="172a6-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
