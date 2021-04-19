---
description: 條件式包裝函式篩選
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: 條件式包裝函式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997061"
---
# <a name="acm-wrapper-filter"></a><span data-ttu-id="b34e1-103">條件式包裝函式篩選</span><span class="sxs-lookup"><span data-stu-id="b34e1-103">ACM Wrapper Filter</span></span>

<span data-ttu-id="b34e1-104">「通過包裝函式」篩選器可讓音訊壓縮管理員 (的) 編解碼器來聯結篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b34e1-104">The ACM Wrapper filter enables Audio Compression Manager (ACM) codecs to join a filter graph.</span></span> <span data-ttu-id="b34e1-105">它可做為解壓縮篩選器或壓縮篩選器。</span><span class="sxs-lookup"><span data-stu-id="b34e1-105">It can act either as a decompression filter or as a compression filter.</span></span>

<span data-ttu-id="b34e1-106">作為解壓縮篩選器，LegacyAmFilterCategory) 的 [DirectShow 篩選器] 類別中會出現 [] 的 [DirectShow 篩選器] (類別， \_ 並具有正常的業績 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b34e1-106">As a decompression filter, the ACM Wrapper appears in the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory) and has a merit of MERIT\_NORMAL.</span></span> <span data-ttu-id="b34e1-107">輸入 pin 的連接媒體類型會決定篩選器所使用的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="b34e1-107">The connection media type on the input pin determines which codec the filter uses.</span></span> <span data-ttu-id="b34e1-108">一般而言，應用程式不需要將篩選準則加入至篩選圖形;篩選圖形管理員會在需要時自動提取。</span><span class="sxs-lookup"><span data-stu-id="b34e1-108">Typically, the application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span> <span data-ttu-id="b34e1-109">解壓縮只適用于 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="b34e1-109">Decompression is only to PCM audio.</span></span>

<span data-ttu-id="b34e1-110">若為壓縮篩選，則會在 [音訊壓縮機] 類別中顯示「」類別 (CLSID \_ AudioCompressorCategory) ，並有 \_ 「 \_ 未使用」的優點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b34e1-110">As a compression filter, the ACM Wrapper appears in the "Audio Compressors" category (CLSID\_AudioCompressorCategory) and has a merit of MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="b34e1-111">每個編解碼器都會顯示為個別的實例。</span><span class="sxs-lookup"><span data-stu-id="b34e1-111">Each codec appears as a separate instance.</span></span> <span data-ttu-id="b34e1-112">針對壓縮，您無法直接使用 CoCreateInstance 建立篩選器。</span><span class="sxs-lookup"><span data-stu-id="b34e1-112">For compression, you cannot directly create the filter with CoCreateInstance.</span></span> <span data-ttu-id="b34e1-113">相反地，您必須使用系統裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="b34e1-113">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="b34e1-114">如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="b34e1-114">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b34e1-115">篩選介面</span><span class="sxs-lookup"><span data-stu-id="b34e1-115">Filter interfaces</span></span></td>
<td><span data-ttu-id="b34e1-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、IPersist、IPersistPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b34e1-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b34e1-117">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="b34e1-117">Input pin media types</span></span></td>
<td><span data-ttu-id="b34e1-118">MEDIATYPE_Audio、MEDIASUBTYPE_Null FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="b34e1-118">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b34e1-119">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="b34e1-119">Input pin interfaces</span></span></td>
<td><span data-ttu-id="b34e1-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b34e1-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b34e1-121">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="b34e1-121">Output pin media types</span></span></td>
<td><span data-ttu-id="b34e1-122">MEDIATYPE_Audio、MEDIASUBTYPE_PCM FORMAT_WaveFormatEx。可能的任何組合如下：</span><span class="sxs-lookup"><span data-stu-id="b34e1-122">MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Any combination of the following are possible:</span></span><br/>
<ul>
<li><span data-ttu-id="b34e1-123">每秒樣本數 (kHz) ：44.1、22.05、11.025 或8.0。</span><span class="sxs-lookup"><span data-stu-id="b34e1-123">Samples per second (kHz): 44.1, 22.05, 11.025, or 8.0.</span></span></li>
<li><span data-ttu-id="b34e1-124">通道：身歷聲或 mono。</span><span class="sxs-lookup"><span data-stu-id="b34e1-124">Channels: Stereo or mono.</span></span></li>
<li><span data-ttu-id="b34e1-125">每個樣本的位數：8或16。</span><span class="sxs-lookup"><span data-stu-id="b34e1-125">Bits per sample: 8 or 16.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b34e1-126">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="b34e1-126">Output pin interfaces</span></span></td>
<td><span data-ttu-id="b34e1-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b34e1-127"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b34e1-128">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="b34e1-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="b34e1-129">CLSID_ACMWrapper</span><span class="sxs-lookup"><span data-stu-id="b34e1-129">CLSID_ACMWrapper</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b34e1-130">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="b34e1-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="b34e1-131">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="b34e1-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b34e1-132">可執行檔</span><span class="sxs-lookup"><span data-stu-id="b34e1-132">Executable</span></span></td>
<td><span data-ttu-id="b34e1-133">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b34e1-133">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b34e1-134"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="b34e1-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="b34e1-135">MERIT_NORMAL 或 MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="b34e1-135">MERIT_NORMAL or MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b34e1-136"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="b34e1-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="b34e1-137">CLSID_LegacyAmFilterCategory 或 CLSID_AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="b34e1-137">CLSID_LegacyAmFilterCategory or CLSID_AudioCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b34e1-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="b34e1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b34e1-139">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="b34e1-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




