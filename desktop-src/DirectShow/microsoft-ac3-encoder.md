---
description: Microsoft AC-3 編碼器篩選器會將身歷聲 PCM 音訊編碼為杜比數位位流。
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: 'Microsoft AC-3 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109180"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="46fad-103">Microsoft AC-3 編碼器</span><span class="sxs-lookup"><span data-stu-id="46fad-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="46fad-104">Microsoft AC-3 編碼器篩選器會將身歷聲 PCM 音訊編碼為杜比數位位流。</span><span class="sxs-lookup"><span data-stu-id="46fad-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="46fad-105">Microsoft 應用程式使用的杜比數位授權方案，會限制 Microsoft 的杜比數位技術。</span><span class="sxs-lookup"><span data-stu-id="46fad-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="46fad-106">以 IA-64 為基礎的平臺不支援此篩選器。</span><span class="sxs-lookup"><span data-stu-id="46fad-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="46fad-107">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="46fad-107">Filter Information</span></span>

<span data-ttu-id="46fad-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="46fad-108">Filter Interfaces</span></span>

[<span data-ttu-id="46fad-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="46fad-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="46fad-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="46fad-110">Input Pin Media Types</span></span>

<span data-ttu-id="46fad-111">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="46fad-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="46fad-112">輸入類型必須是 48-kHz 身歷聲，每個樣本16位。</span><span class="sxs-lookup"><span data-stu-id="46fad-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="46fad-113">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="46fad-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="46fad-114">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="46fad-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="46fad-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="46fad-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="46fad-116">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="46fad-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="46fad-117">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="46fad-117">Output Pin Media Types</span></span>

<span data-ttu-id="46fad-118">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="46fad-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="46fad-119">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ 杜比 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="46fad-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="46fad-120">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="46fad-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="46fad-121">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="46fad-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="46fad-122">**IPin**</span><span class="sxs-lookup"><span data-stu-id="46fad-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="46fad-123">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="46fad-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="46fad-124">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="46fad-124">Filter CLSID</span></span>

<span data-ttu-id="46fad-125">**CLSID \_** 在 wmcodecdsp 中宣告的 CMSAC3Enc () </span><span class="sxs-lookup"><span data-stu-id="46fad-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="46fad-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="46fad-126">Executable</span></span>

<span data-ttu-id="46fad-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="46fad-127">msac3enc.dll</span></span>

[<span data-ttu-id="46fad-128">優點</span><span class="sxs-lookup"><span data-stu-id="46fad-128">Merit</span></span>](merit.md)

<span data-ttu-id="46fad-129">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="46fad-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="46fad-130">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="46fad-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="46fad-131">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="46fad-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="46fad-132">備註</span><span class="sxs-lookup"><span data-stu-id="46fad-132">Remarks</span></span>

<span data-ttu-id="46fad-133">此篩選器無法供協力廠商應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="46fad-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="46fad-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="46fad-134">Requirements</span></span>



| <span data-ttu-id="46fad-135">需求</span><span class="sxs-lookup"><span data-stu-id="46fad-135">Requirement</span></span> | <span data-ttu-id="46fad-136">值</span><span class="sxs-lookup"><span data-stu-id="46fad-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46fad-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46fad-137">Minimum supported client</span></span><br/> | <span data-ttu-id="46fad-138">Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46fad-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="46fad-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46fad-139">Minimum supported server</span></span><br/> | <span data-ttu-id="46fad-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="46fad-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="46fad-141">標頭</span><span class="sxs-lookup"><span data-stu-id="46fad-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="46fad-142"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="46fad-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="46fad-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46fad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fad-144">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="46fad-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




