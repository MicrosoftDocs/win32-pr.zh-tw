---
description: 本主題提供一些指導方針，以將解碼器或編碼器作為媒體基礎轉換 (MFT) 。
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: 執行編解碼器 MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194988"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="e7c27-103">執行編解碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="e7c27-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="e7c27-104">本主題提供一些指導方針，以將解碼器或編碼器作為媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="e7c27-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="e7c27-105">編碼器</span><span class="sxs-lookup"><span data-stu-id="e7c27-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="e7c27-106">編碼器格式的協商</span><span class="sxs-lookup"><span data-stu-id="e7c27-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="e7c27-107">解碼器</span><span class="sxs-lookup"><span data-stu-id="e7c27-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="e7c27-108">僅限轉碼的解碼器</span><span class="sxs-lookup"><span data-stu-id="e7c27-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="e7c27-109">電影屬性</span><span class="sxs-lookup"><span data-stu-id="e7c27-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="e7c27-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7c27-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="e7c27-111">編碼器</span><span class="sxs-lookup"><span data-stu-id="e7c27-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="e7c27-112">編碼器格式的協商</span><span class="sxs-lookup"><span data-stu-id="e7c27-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="e7c27-113">下列程式是用來初始化編碼器：</span><span class="sxs-lookup"><span data-stu-id="e7c27-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="e7c27-114">查詢 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面的 MFT。</span><span class="sxs-lookup"><span data-stu-id="e7c27-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="e7c27-115">呼叫 [**ICodecAPI：： SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) 以設定編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="e7c27-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="e7c27-116">呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼格式。</span><span class="sxs-lookup"><span data-stu-id="e7c27-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="e7c27-117">呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) ，以取得相容輸入類型的清單。</span><span class="sxs-lookup"><span data-stu-id="e7c27-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="e7c27-118"> (可能會略過此步驟。 ) </span><span class="sxs-lookup"><span data-stu-id="e7c27-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="e7c27-119">呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) ，以設定未壓縮的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="e7c27-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="e7c27-120">在步驟3中設定輸出類型之後， [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 方法必須傳回與目前輸出類型相容的輸入類型清單。</span><span class="sxs-lookup"><span data-stu-id="e7c27-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="e7c27-121">換句話說， **GetInputAvailableType** 在此點傳回的任何類型都必須是有效的 [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)。</span><span class="sxs-lookup"><span data-stu-id="e7c27-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="e7c27-122">對於解碼器，會反轉型別設定順序：先設定輸入型別，後面接著輸出型別。</span><span class="sxs-lookup"><span data-stu-id="e7c27-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="e7c27-123">設定輸入類型之後， [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法必須傳回可傳遞至 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法的類型清單。</span><span class="sxs-lookup"><span data-stu-id="e7c27-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="e7c27-124">編碼器和解碼器應支援 NV12 為常見的未壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="e7c27-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="e7c27-125">這可確保管線元件可與基本的 colorspace 轉換交互操作。</span><span class="sxs-lookup"><span data-stu-id="e7c27-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="e7c27-126">當然，也可以支援其他格式。</span><span class="sxs-lookup"><span data-stu-id="e7c27-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="e7c27-127">解碼器</span><span class="sxs-lookup"><span data-stu-id="e7c27-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="e7c27-128">Transcode-Only 的解碼器</span><span class="sxs-lookup"><span data-stu-id="e7c27-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="e7c27-129">某些解碼器會針對轉碼 (解碼，然後重新編碼串流) ，因此不適合在播放期間使用。</span><span class="sxs-lookup"><span data-stu-id="e7c27-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="e7c27-130">如果解碼器 MFT 僅供轉碼使用，則在您註冊 MFT 時，請設定 [ **\_ \_ \_ \_ 僅限轉碼旗標的 MFT 列舉旗** 標] 旗標。</span><span class="sxs-lookup"><span data-stu-id="e7c27-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="e7c27-131"> (參閱 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)。 ) </span><span class="sxs-lookup"><span data-stu-id="e7c27-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="e7c27-132">依預設， [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函式不會傳回轉碼的解碼器。</span><span class="sxs-lookup"><span data-stu-id="e7c27-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="e7c27-133">若要列舉轉碼的解碼器，請呼叫 **MFTEnumEx** ，然後在 *旗標* 參數中將 **MFT \_ 列舉 \_ 旗標轉碼為 \_ \_ ONLY** 旗標。</span><span class="sxs-lookup"><span data-stu-id="e7c27-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="e7c27-134">在 **MFTEnumEx** 函式中使用時，此旗標會列舉轉碼的解碼器和其他的解碼器。</span><span class="sxs-lookup"><span data-stu-id="e7c27-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="e7c27-135">**\_ \_ \_ \_ 僅限 MFTRegister MFT 列舉旗標轉碼**</span><span class="sxs-lookup"><span data-stu-id="e7c27-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="e7c27-136">**\_ \_ \_ \_ 僅限 MFTEnumEx MFT 列舉旗標轉碼**</span><span class="sxs-lookup"><span data-stu-id="e7c27-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="e7c27-137">是否列舉了 MFT？</span><span class="sxs-lookup"><span data-stu-id="e7c27-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="e7c27-138">1</span><span class="sxs-lookup"><span data-stu-id="e7c27-138">1</span></span>                                                | <span data-ttu-id="e7c27-139">1</span><span class="sxs-lookup"><span data-stu-id="e7c27-139">1</span></span>                                              | <span data-ttu-id="e7c27-140">是</span><span class="sxs-lookup"><span data-stu-id="e7c27-140">Yes</span></span>                |
| <span data-ttu-id="e7c27-141">1</span><span class="sxs-lookup"><span data-stu-id="e7c27-141">1</span></span>                                                | <span data-ttu-id="e7c27-142">0</span><span class="sxs-lookup"><span data-stu-id="e7c27-142">0</span></span>                                              | <span data-ttu-id="e7c27-143">否</span><span class="sxs-lookup"><span data-stu-id="e7c27-143">No</span></span>                 |
| <span data-ttu-id="e7c27-144">0</span><span class="sxs-lookup"><span data-stu-id="e7c27-144">0</span></span>                                                | <span data-ttu-id="e7c27-145">1</span><span class="sxs-lookup"><span data-stu-id="e7c27-145">1</span></span>                                              | <span data-ttu-id="e7c27-146">是</span><span class="sxs-lookup"><span data-stu-id="e7c27-146">Yes</span></span>                |
| <span data-ttu-id="e7c27-147">0</span><span class="sxs-lookup"><span data-stu-id="e7c27-147">0</span></span>                                                | <span data-ttu-id="e7c27-148">0</span><span class="sxs-lookup"><span data-stu-id="e7c27-148">0</span></span>                                              | <span data-ttu-id="e7c27-149">是</span><span class="sxs-lookup"><span data-stu-id="e7c27-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="e7c27-150">電影屬性</span><span class="sxs-lookup"><span data-stu-id="e7c27-150">Telecine Attributes</span></span>

<span data-ttu-id="e7c27-151">媒體來源可能會將下列電影屬性附加至它所提供的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="e7c27-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="e7c27-152">屬性</span><span class="sxs-lookup"><span data-stu-id="e7c27-152">Attribute</span></span>                                                                                   | <span data-ttu-id="e7c27-153">描述</span><span class="sxs-lookup"><span data-stu-id="e7c27-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="e7c27-154">**MFSampleExtension \_ RepeatFirstField**</span><span class="sxs-lookup"><span data-stu-id="e7c27-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="e7c27-155">相當於 "repeat first field" (RFF) 旗標。</span><span class="sxs-lookup"><span data-stu-id="e7c27-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="e7c27-156">**MFSampleExtension \_ BottomFieldFirst**</span><span class="sxs-lookup"><span data-stu-id="e7c27-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="e7c27-157">"Top field first" (TFF) 旗標的反向。</span><span class="sxs-lookup"><span data-stu-id="e7c27-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="e7c27-158">這些旗標會在執行去交錯時，提供提示給增強型影片轉譯器 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="e7c27-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="e7c27-159">解碼器應該將這些旗標複製到輸出範例，使其到達 EVR，以將這些旗標傳播至輸出範例。</span><span class="sxs-lookup"><span data-stu-id="e7c27-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7c27-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="e7c27-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c27-161">撰寫自訂的 MFT</span><span class="sxs-lookup"><span data-stu-id="e7c27-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
