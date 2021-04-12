---
description: 本節說明如何設定 VBR 資料流程。
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: '使用 VBR 編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191746"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="b8c32-103">使用 VBR 編碼 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="b8c32-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b8c32-104">如 [編碼方法](encodingmethods.md) 主題中所述， (VBR) 編碼的變動位元速率，以改善內容品質的一致性。</span><span class="sxs-lookup"><span data-stu-id="b8c32-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="b8c32-105">您可以用相同的方式來設定 VBR 資料流程， (CBR) 資料流程，但緩衝區參數 (位元速率和緩衝區視窗) 。</span><span class="sxs-lookup"><span data-stu-id="b8c32-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="b8c32-106">本節說明如何設定 VBR 資料流程。</span><span class="sxs-lookup"><span data-stu-id="b8c32-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="b8c32-107">設定以品質為基礎的 VBR</span><span class="sxs-lookup"><span data-stu-id="b8c32-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="b8c32-108">使用以品質為基礎的 VBR 方法進行編碼並不需要任何預先定義的緩衝區參數。</span><span class="sxs-lookup"><span data-stu-id="b8c32-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="b8c32-109">相反地，您可以指定品質層級 (從0到 100) ，編碼器會使用此層級來動態判斷適當的緩衝區參數。</span><span class="sxs-lookup"><span data-stu-id="b8c32-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="b8c32-110">此編碼模式只會使用一次編碼。</span><span class="sxs-lookup"><span data-stu-id="b8c32-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="b8c32-111">您可以列舉音訊編解碼器的支援品質型 VBR 輸出類型。</span><span class="sxs-lookup"><span data-stu-id="b8c32-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="b8c32-112">設定輸出型別時，您必須使用 SQL-DMO 所傳回的其中一個類型。</span><span class="sxs-lookup"><span data-stu-id="b8c32-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="b8c32-113">如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="b8c32-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="b8c32-114">若要設定品質型的 VBR 影片資料流程，您必須設定下表所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8c32-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="b8c32-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b8c32-115">Property</span></span>                                            | <span data-ttu-id="b8c32-116">描述</span><span class="sxs-lookup"><span data-stu-id="b8c32-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8c32-117">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="b8c32-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="b8c32-118">設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="b8c32-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="b8c32-119">MFPKEY \_ VBRQUALITY</span><span class="sxs-lookup"><span data-stu-id="b8c32-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="b8c32-120">設定為所需的品質值，從0到100。</span><span class="sxs-lookup"><span data-stu-id="b8c32-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="b8c32-121">並非所有品質值都代表不同的設定。</span><span class="sxs-lookup"><span data-stu-id="b8c32-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="b8c32-122">如需詳細資訊，請參閱屬性描述。</span><span class="sxs-lookup"><span data-stu-id="b8c32-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="b8c32-123">設定未受限制的 VBR</span><span class="sxs-lookup"><span data-stu-id="b8c32-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="b8c32-124">未受限制的 VBR 編碼可讓編碼器在沒有任何明確緩衝區限制的情況下，變更個別樣本的大小。</span><span class="sxs-lookup"><span data-stu-id="b8c32-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="b8c32-125">不過，產生的內容期間的平均位元速率必須小於或等於指定的值。</span><span class="sxs-lookup"><span data-stu-id="b8c32-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="b8c32-126">未受限制的 VBR 需要兩次編碼階段。</span><span class="sxs-lookup"><span data-stu-id="b8c32-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="b8c32-127">您可以列舉音訊編解碼器支援的雙通路 VBR 輸出類型。</span><span class="sxs-lookup"><span data-stu-id="b8c32-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="b8c32-128">設定輸出型別時，您必須使用 SQL-DMO 所傳回的其中一個類型。</span><span class="sxs-lookup"><span data-stu-id="b8c32-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="b8c32-129">如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="b8c32-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="b8c32-130">若要設定未受限制的 VBR 影片資料流程，您必須設定下表所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8c32-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="b8c32-131">屬性</span><span class="sxs-lookup"><span data-stu-id="b8c32-131">Property</span></span>                                            | <span data-ttu-id="b8c32-132">描述</span><span class="sxs-lookup"><span data-stu-id="b8c32-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="b8c32-133">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="b8c32-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="b8c32-134">設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="b8c32-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="b8c32-135">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="b8c32-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="b8c32-136">設定為2。</span><span class="sxs-lookup"><span data-stu-id="b8c32-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="b8c32-137">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="b8c32-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="b8c32-138">設定為所需的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="b8c32-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="b8c32-139">設定 Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="b8c32-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="b8c32-140">尖峰限制的 VBR 就像是不受限制的 VBR，因為它會限制為數據流持續時間的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="b8c32-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="b8c32-141">此外，尖峰限制的 VBR 會符合尖峰緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b8c32-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="b8c32-142">這個緩衝區是使用尖峰位元速率和尖峰緩衝區視窗來描述，就像是平均位元速率和緩衝區視窗描述的 CBR 緩衝區一樣。</span><span class="sxs-lookup"><span data-stu-id="b8c32-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="b8c32-143">這種模式可讓編碼器在編碼個別樣本的方式上有彈性，同時遵守尖峰限制。</span><span class="sxs-lookup"><span data-stu-id="b8c32-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="b8c32-144">當解碼是由裝置中的晶片（例如 DVD 播放機）執行時，這項功能特別有用，其中有必須考慮的硬體限制。</span><span class="sxs-lookup"><span data-stu-id="b8c32-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="b8c32-145">支援的尖峰型、VBR 音訊編碼器輸出類型與針對未受限制的 VBR 列舉的類型相同。</span><span class="sxs-lookup"><span data-stu-id="b8c32-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="b8c32-146">設定此的尖峰值，並使用傳遞的類型。</span><span class="sxs-lookup"><span data-stu-id="b8c32-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="b8c32-147">如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="b8c32-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="b8c32-148">若要設定尖峰限制的 VBR 影片資料流程，您必須使用 **IPropertyBag：： Write** 方法來設定下表中所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8c32-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="b8c32-149">屬性</span><span class="sxs-lookup"><span data-stu-id="b8c32-149">Property</span></span>                                            | <span data-ttu-id="b8c32-150">描述</span><span class="sxs-lookup"><span data-stu-id="b8c32-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="b8c32-151">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="b8c32-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="b8c32-152">設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="b8c32-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="b8c32-153">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="b8c32-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="b8c32-154">設定為2。</span><span class="sxs-lookup"><span data-stu-id="b8c32-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="b8c32-155">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="b8c32-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="b8c32-156">設定為所需的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="b8c32-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="b8c32-157">MFPKEY \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="b8c32-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="b8c32-158">設定為所需的尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="b8c32-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="b8c32-159">MFPKEY \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="b8c32-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="b8c32-160">設定為對應至尖峰位速率的緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="b8c32-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="b8c32-161">建議您將尖峰位速率設定為至少兩倍的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="b8c32-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="b8c32-162">將尖峰速率設定為較低的值，可能會造成編解碼器將內容編碼為雙向 CBR，而不是尖峰限制的 VBR。</span><span class="sxs-lookup"><span data-stu-id="b8c32-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b8c32-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8c32-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c32-164">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="b8c32-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="b8c32-165">使用 Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="b8c32-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="b8c32-166">使用音訊</span><span class="sxs-lookup"><span data-stu-id="b8c32-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="b8c32-167">使用影片</span><span class="sxs-lookup"><span data-stu-id="b8c32-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



