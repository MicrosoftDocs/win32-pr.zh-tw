---
description: MPEG-2 信號信號媒體類型
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MPEG-2 信號信號媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106991396"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="81483-103">MPEG-2 信號信號媒體類型</span><span class="sxs-lookup"><span data-stu-id="81483-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="81483-104">[Mpeg-2 信號信號](mpeg-2-demultiplexer.md)篩選器可識別下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="81483-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="81483-105">輸入類型</span><span class="sxs-lookup"><span data-stu-id="81483-105">Input Types</span></span>

<span data-ttu-id="81483-106">主要類型一律為 **媒體型 \_ 串流**。</span><span class="sxs-lookup"><span data-stu-id="81483-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="81483-107">子類型可以是下列任何一項。</span><span class="sxs-lookup"><span data-stu-id="81483-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="81483-108">GUID</span><span class="sxs-lookup"><span data-stu-id="81483-108">GUID</span></span>                                             | <span data-ttu-id="81483-109">Description</span><span class="sxs-lookup"><span data-stu-id="81483-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81483-110">**KSDATAFORMAT \_ 子類型 \_ BDA \_ MPEG2 \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="81483-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="81483-111">從廣播驅動程式架構傳輸串流 (BDA) 裝置篩選器。</span><span class="sxs-lookup"><span data-stu-id="81483-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="81483-112">MPEG-2 信號信號會將這個子類型視為與 **MEDIASUBTYPE \_ MPEG2 \_ 傳輸** 相同。</span><span class="sxs-lookup"><span data-stu-id="81483-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="81483-113">**MEDIASUBTYPE \_ MPEG2 \_ 計畫**</span><span class="sxs-lookup"><span data-stu-id="81483-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="81483-114">程式資料流程</span><span class="sxs-lookup"><span data-stu-id="81483-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="81483-115">**MEDIASUBTYPE \_ MPEG2 \_ 傳輸**</span><span class="sxs-lookup"><span data-stu-id="81483-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="81483-116">傳輸串流 (TS) ，包含188個位元組的封包</span><span class="sxs-lookup"><span data-stu-id="81483-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="81483-117">**MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="81483-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="81483-118">具有 "strided" 封包的傳輸資料流程。</span><span class="sxs-lookup"><span data-stu-id="81483-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="81483-119">此子類型表示 TS 封包可以填補額外的位元組。</span><span class="sxs-lookup"><span data-stu-id="81483-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="81483-120">如需詳細資訊，請參閱 [**MPEG2 \_ 傳輸 \_ STRIDE**](mpeg2-transport-stride.md)。</span><span class="sxs-lookup"><span data-stu-id="81483-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="81483-121">針對 strided 傳輸封包 (**MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ stride**) ，每個媒體範例都必須包含整數個傳輸封包，如 [**MPEG2 \_ 傳輸 \_ 跨距**](mpeg2-transport-stride.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="81483-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="81483-122">對於所有其他輸入類型，範例界限沒有任何限制;個別的封包可以跨越範例界限。</span><span class="sxs-lookup"><span data-stu-id="81483-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="81483-123">輸出型別</span><span class="sxs-lookup"><span data-stu-id="81483-123">Output Types</span></span>

<span data-ttu-id="81483-124">MPEG-2 信號信號不會驗證輸出類型;下游篩選器負責剖析它從信號剖析收到的資料。</span><span class="sxs-lookup"><span data-stu-id="81483-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="81483-125">不過，下游篩選器通常會接受下列類型做為信號的輸出。</span><span class="sxs-lookup"><span data-stu-id="81483-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="81483-126">MPEG 2 區段</span><span class="sxs-lookup"><span data-stu-id="81483-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81483-127">主要類型</span><span class="sxs-lookup"><span data-stu-id="81483-127">Major Type</span></span></td>
<td><span data-ttu-id="81483-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="81483-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81483-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="81483-129">Subtype</span></span></td>
<td><span data-ttu-id="81483-130">下列任何一項：</span><span class="sxs-lookup"><span data-stu-id="81483-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="81483-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>： ATSC 服務資訊。</span><span class="sxs-lookup"><span data-stu-id="81483-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="81483-132"><strong>MEDIASUBTYPE_DVB_SI</strong>： Dvb-t 服務資訊。</span><span class="sxs-lookup"><span data-stu-id="81483-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="81483-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>：整合服務數位廣播 (ISDB) 服務資訊。</span><span class="sxs-lookup"><span data-stu-id="81483-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="81483-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>： mpeg-2 區段資料。</span><span class="sxs-lookup"><span data-stu-id="81483-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81483-135">格式類型</span><span class="sxs-lookup"><span data-stu-id="81483-135">Format Type</span></span></td>
<td><span data-ttu-id="81483-136">無</span><span class="sxs-lookup"><span data-stu-id="81483-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="81483-137">MPEG-2 影片</span><span class="sxs-lookup"><span data-stu-id="81483-137">MPEG-2 Video</span></span>



|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="81483-138">主要類型</span><span class="sxs-lookup"><span data-stu-id="81483-138">Major type</span></span>       | <span data-ttu-id="81483-139">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="81483-139">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="81483-140">Subtype</span><span class="sxs-lookup"><span data-stu-id="81483-140">Subtype</span></span>          | <span data-ttu-id="81483-141">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="81483-141">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="81483-142">格式類型</span><span class="sxs-lookup"><span data-stu-id="81483-142">Format Type</span></span>      | <span data-ttu-id="81483-143">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="81483-143">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="81483-144">格式結構</span><span class="sxs-lookup"><span data-stu-id="81483-144">Format Structure</span></span> | [<span data-ttu-id="81483-145">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="81483-145">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="81483-146">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="81483-146">MPEG-2 Audio</span></span>



|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="81483-147">主要類型</span><span class="sxs-lookup"><span data-stu-id="81483-147">Major type</span></span>       | <span data-ttu-id="81483-148">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="81483-148">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="81483-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="81483-149">Subtype</span></span>          | <span data-ttu-id="81483-150">**MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="81483-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="81483-151">格式類型</span><span class="sxs-lookup"><span data-stu-id="81483-151">Format Type</span></span>      | <span data-ttu-id="81483-152">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="81483-152">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="81483-153">格式結構</span><span class="sxs-lookup"><span data-stu-id="81483-153">Format Structure</span></span> | <span data-ttu-id="81483-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81483-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="81483-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="81483-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81483-156">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="81483-156">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
