---
description: 變更影片串流的畫面播放速率。
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: '畫面播放速率轉換器 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689292"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="8ee57-103">畫面播放速率轉換器 DSP</span><span class="sxs-lookup"><span data-stu-id="8ee57-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="8ee57-104">變更影片串流的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="8ee57-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="8ee57-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="8ee57-105">CLSID</span></span>

<span data-ttu-id="8ee57-106">CLSID \_ CFrameRateConvertDmo</span><span class="sxs-lookup"><span data-stu-id="8ee57-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="8ee57-107">介面</span><span class="sxs-lookup"><span data-stu-id="8ee57-107">Interfaces</span></span>

-   <span data-ttu-id="8ee57-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="8ee57-108">**IMediaObject**</span></span>
-   <span data-ttu-id="8ee57-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8ee57-109">**IMFTransform**</span></span>
-   <span data-ttu-id="8ee57-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="8ee57-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="8ee57-111">格式</span><span class="sxs-lookup"><span data-stu-id="8ee57-111">Formats</span></span>

-   <span data-ttu-id="8ee57-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="8ee57-112">ARGB 32</span></span>
-   <span data-ttu-id="8ee57-113">RGB 24</span><span class="sxs-lookup"><span data-stu-id="8ee57-113">RGB 24</span></span>
-   <span data-ttu-id="8ee57-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="8ee57-114">RGB 32</span></span>
-   <span data-ttu-id="8ee57-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="8ee57-115">RGB 555</span></span>
-   <span data-ttu-id="8ee57-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="8ee57-116">RGB 565</span></span>
-   <span data-ttu-id="8ee57-117">AYUV</span><span class="sxs-lookup"><span data-stu-id="8ee57-117">AYUV</span></span>
-   <span data-ttu-id="8ee57-118">IYUV</span><span class="sxs-lookup"><span data-stu-id="8ee57-118">IYUV</span></span>
-   <span data-ttu-id="8ee57-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="8ee57-119">UYVY</span></span>
-   <span data-ttu-id="8ee57-120">Y211</span><span class="sxs-lookup"><span data-stu-id="8ee57-120">Y211</span></span>
-   <span data-ttu-id="8ee57-121">Y411</span><span class="sxs-lookup"><span data-stu-id="8ee57-121">Y411</span></span>
-   <span data-ttu-id="8ee57-122">Y41P</span><span class="sxs-lookup"><span data-stu-id="8ee57-122">Y41P</span></span>
-   <span data-ttu-id="8ee57-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="8ee57-123">YUY2</span></span>
-   <span data-ttu-id="8ee57-124">YUYV</span><span class="sxs-lookup"><span data-stu-id="8ee57-124">YUYV</span></span>
-   <span data-ttu-id="8ee57-125">YV12</span><span class="sxs-lookup"><span data-stu-id="8ee57-125">YV12</span></span>
-   <span data-ttu-id="8ee57-126">YVYU</span><span class="sxs-lookup"><span data-stu-id="8ee57-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="8ee57-127">屬性</span><span class="sxs-lookup"><span data-stu-id="8ee57-127">Properties</span></span>

-   [<span data-ttu-id="8ee57-128">MFPKEY \_ 約定 \_ INPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="8ee57-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="8ee57-129">MFPKEY \_ 約定 \_ OUTPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="8ee57-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="8ee57-130">備註</span><span class="sxs-lookup"><span data-stu-id="8ee57-130">Remarks</span></span>

<span data-ttu-id="8ee57-131">這個 DSP 會藉由重複或卸載框架來變更畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="8ee57-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="8ee57-132">根據預設，DSP 會取得媒體類型的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="8ee57-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="8ee57-133">（選擇性）您可以藉由設定 MFPKEY 的 [設定 \_ ] \_ INPUTFRAMERATE 和 [MFPKEY] \_ \_ OUTPUTFRAMERATE 屬性來指定畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="8ee57-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="8ee57-134">這些值會覆寫媒體類型中指定的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="8ee57-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="8ee57-135">但是，如果您在媒體基礎管線內使用這個 DSP，則不應設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8ee57-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee57-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ee57-136">Requirements</span></span>



| <span data-ttu-id="8ee57-137">需求</span><span class="sxs-lookup"><span data-stu-id="8ee57-137">Requirement</span></span> | <span data-ttu-id="8ee57-138">值</span><span class="sxs-lookup"><span data-stu-id="8ee57-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee57-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ee57-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee57-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ee57-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8ee57-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ee57-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee57-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ee57-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ee57-143">標頭</span><span class="sxs-lookup"><span data-stu-id="8ee57-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee57-144"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee57-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="8ee57-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8ee57-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ee57-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee57-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ee57-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ee57-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee57-148">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="8ee57-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




