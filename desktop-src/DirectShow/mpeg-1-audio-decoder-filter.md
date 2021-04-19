---
description: MPEG-2 音訊解碼篩選器
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: MPEG-2 音訊解碼篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973950"
---
# <a name="mpeg-1-audio-decoder-filter"></a><span data-ttu-id="21cd3-103">MPEG-2 音訊解碼篩選器</span><span class="sxs-lookup"><span data-stu-id="21cd3-103">MPEG-1 Audio Decoder Filter</span></span>

<span data-ttu-id="21cd3-104">將 MPEG-2 的第一層和第 II 層音訊解碼為 PCM。</span><span class="sxs-lookup"><span data-stu-id="21cd3-104">Decodes MPEG-1 Layer I and Layer II audio to PCM.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21cd3-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="21cd3-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="21cd3-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="21cd3-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cd3-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="21cd3-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="21cd3-108">MEDIATYPE_Audio，FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="21cd3-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span></span><br/> <span data-ttu-id="21cd3-109">下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="21cd3-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="21cd3-110">MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="21cd3-110">MEDIASUBTYPE_MPEG1Packet</span></span></li>
<li><span data-ttu-id="21cd3-111">MEDIASUBTYPE_MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="21cd3-111">MEDIASUBTYPE_MPEG1Payload</span></span></li>
<li><span data-ttu-id="21cd3-112">MEDIASUBTYPE_MPEG1AudioPayload</span><span class="sxs-lookup"><span data-stu-id="21cd3-112">MEDIASUBTYPE_MPEG1AudioPayload</span></span></li>
<li><span data-ttu-id="21cd3-113">GUID_Null</span><span class="sxs-lookup"><span data-stu-id="21cd3-113">GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cd3-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="21cd3-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="21cd3-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="21cd3-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cd3-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="21cd3-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="21cd3-117">MEDIATYPE_Audio，MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="21cd3-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cd3-118">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="21cd3-118">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="21cd3-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="21cd3-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cd3-120">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="21cd3-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="21cd3-121">CLSID_CMpegAudioCodec</span><span class="sxs-lookup"><span data-stu-id="21cd3-121">CLSID_CMpegAudioCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cd3-122">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="21cd3-122">Property Page CLSID</span></span></td>
<td><span data-ttu-id="21cd3-123">CLSID_MpegAudioDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="21cd3-123">CLSID_MpegAudioDecoderPropertyPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cd3-124">可執行檔</span><span class="sxs-lookup"><span data-stu-id="21cd3-124">Executable</span></span></td>
<td><span data-ttu-id="21cd3-125">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="21cd3-125">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21cd3-126"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="21cd3-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="21cd3-127">0x03680001</span><span class="sxs-lookup"><span data-stu-id="21cd3-127">0x03680001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21cd3-128"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="21cd3-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="21cd3-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="21cd3-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="21cd3-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="21cd3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21cd3-131">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="21cd3-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




