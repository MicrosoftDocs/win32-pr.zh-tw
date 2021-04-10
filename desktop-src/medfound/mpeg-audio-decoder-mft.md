---
description: Microsoft MPEG 音訊解碼器是一種同步媒體基礎轉換 (MFT) ，可使用媒體基礎 (MF) 管線來解碼 MPEG 音訊基本資料流程格式。
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: MPEG 音訊解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943731"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="95387-103">MPEG 音訊解碼器</span><span class="sxs-lookup"><span data-stu-id="95387-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="95387-104">Microsoft MPEG 音訊解碼器是一種同步 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，可使用媒體基礎 (MF) 管線來解碼 MPEG 音訊基本資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="95387-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="95387-105">此解碼器支援下列 MPEG 基本資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="95387-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="95387-106">MPEG-2 音訊層 I 和 II (ISO/IEC 11172-3) 。</span><span class="sxs-lookup"><span data-stu-id="95387-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="95387-107">2.</span><span class="sxs-lookup"><span data-stu-id="95387-107">2.</span></span> <span data-ttu-id="95387-108">MPEG-2 與舊版相容，第 I 和第二層 (ISO</span><span class="sxs-lookup"><span data-stu-id="95387-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="95387-109">MPEG-2 與舊版相容，第 I 和第二層 (ISO/IEC 13818-3) 、mono 和身歷聲</span><span class="sxs-lookup"><span data-stu-id="95387-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="95387-110">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="95387-110">Class Identifier</span></span>

<span data-ttu-id="95387-111">MPEG 音訊解碼器 (CLSID) 的類別識別碼是 **clsid \_ MSMPEGAudDecMFT**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="95387-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="95387-112">輸入媒體類型</span><span class="sxs-lookup"><span data-stu-id="95387-112">Input Media Types</span></span>

<span data-ttu-id="95387-113">MPEG 音訊解碼器支援下列輸入媒體類型屬性。</span><span class="sxs-lookup"><span data-stu-id="95387-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="95387-114">屬性</span><span class="sxs-lookup"><span data-stu-id="95387-114">Attribute</span></span>                                                                               | <span data-ttu-id="95387-115">值</span><span class="sxs-lookup"><span data-stu-id="95387-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95387-116">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="95387-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="95387-117">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="95387-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="95387-118">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="95387-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="95387-119">**MFAudioFormat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="95387-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="95387-120">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="95387-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="95387-121"> (選擇性的) 通常是1代表 mono 或2，最多可以有6個通道。</span><span class="sxs-lookup"><span data-stu-id="95387-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="95387-122">**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="95387-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="95387-123"> (選擇性的) 通常為 mono 或0x3 （身歷聲），但也可以是與最多6個通道相關聯的任一個通道遮罩 (3/2/1、3/2、3/1、2/2、2/1) 。</span><span class="sxs-lookup"><span data-stu-id="95387-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="95387-124">如果有的話，通道遮罩必須與指定的通道輸入數目一致。</span><span class="sxs-lookup"><span data-stu-id="95387-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="95387-125">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95387-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="95387-126"> (選擇性) 下列其中一項：16000、22050、24000、32000、44100、48000。</span><span class="sxs-lookup"><span data-stu-id="95387-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="95387-127">如果有指定，輸入取樣率必須是有效的 MPEG 取樣率之一。</span><span class="sxs-lookup"><span data-stu-id="95387-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="95387-128">輸出媒體類型</span><span class="sxs-lookup"><span data-stu-id="95387-128">Output Media Types</span></span>

<span data-ttu-id="95387-129">MPEG 音訊解碼器會以下列順序支援最多四個輸出媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="95387-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="95387-130">身歷聲、浮點數。</span><span class="sxs-lookup"><span data-stu-id="95387-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="95387-131">身歷聲、16位 PCM。</span><span class="sxs-lookup"><span data-stu-id="95387-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="95387-132">Mono、浮點數 (只有在輸入為 mono 或雙 mono) 時才。</span><span class="sxs-lookup"><span data-stu-id="95387-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="95387-133">只有當輸入為 mono 或雙 mono) 時，才會 (Mono、16位 PCM。</span><span class="sxs-lookup"><span data-stu-id="95387-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="95387-134">此解碼器一律支援身歷聲輸出，並且會列舉為第一個輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="95387-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="95387-135">此解碼器支援下列輸出媒體類型屬性。</span><span class="sxs-lookup"><span data-stu-id="95387-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="95387-136">屬性</span><span class="sxs-lookup"><span data-stu-id="95387-136">Attribute</span></span>                                                                           | <span data-ttu-id="95387-137">值</span><span class="sxs-lookup"><span data-stu-id="95387-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="95387-138">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="95387-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="95387-139">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="95387-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="95387-140">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="95387-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="95387-141">**MFAudioFormat \_ PCM** 或 **MFAudioFormat \_ Float**</span><span class="sxs-lookup"><span data-stu-id="95387-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="95387-142">\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數</span><span class="sxs-lookup"><span data-stu-id="95387-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="95387-143">16或32</span><span class="sxs-lookup"><span data-stu-id="95387-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="95387-144">MF \_ MT \_ 音訊 \_ 數目 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="95387-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="95387-145">1 或 2</span><span class="sxs-lookup"><span data-stu-id="95387-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="95387-146">MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩</span><span class="sxs-lookup"><span data-stu-id="95387-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="95387-147">適用于 mono 的0x4 或0x3 （身歷聲）</span><span class="sxs-lookup"><span data-stu-id="95387-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="95387-148">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_</span><span class="sxs-lookup"><span data-stu-id="95387-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="95387-149">下列其中一項：16000、22050、24000、32000、44100、48000。</span><span class="sxs-lookup"><span data-stu-id="95387-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="95387-150">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="95387-150">Transform Attributes</span></span>

<span data-ttu-id="95387-151">MPEG 音訊解碼器會實行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="95387-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="95387-152">應用程式可以使用這個方法來取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="95387-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="95387-153">屬性</span><span class="sxs-lookup"><span data-stu-id="95387-153">Attribute</span></span>                                                                               | <span data-ttu-id="95387-154">描述</span><span class="sxs-lookup"><span data-stu-id="95387-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95387-155">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="95387-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="95387-156">指定要解碼的雙聲道音訊是否為雙 mono。</span><span class="sxs-lookup"><span data-stu-id="95387-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="95387-157">唯讀。</span><span class="sxs-lookup"><span data-stu-id="95387-157">Read-only.</span></span> <span data-ttu-id="95387-158">由 MFT 設定。</span><span class="sxs-lookup"><span data-stu-id="95387-158">Set by the MFT.</span></span> <span data-ttu-id="95387-159">如需詳細資訊，請參閱 [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono)。</span><span class="sxs-lookup"><span data-stu-id="95387-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="95387-160">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="95387-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="95387-161">指定解碼器如何重現雙重 mono 音訊。</span><span class="sxs-lookup"><span data-stu-id="95387-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="95387-162">預設值為 **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**。</span><span class="sxs-lookup"><span data-stu-id="95387-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="95387-163">讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="95387-163">Read/Write.</span></span> <span data-ttu-id="95387-164">應用程式可以設定此屬性來變更預設行為。</span><span class="sxs-lookup"><span data-stu-id="95387-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="95387-165">如需詳細資訊，請參閱 [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono)。</span><span class="sxs-lookup"><span data-stu-id="95387-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="95387-166">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="95387-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="95387-167">指定壓縮的資料流程位元速率。</span><span class="sxs-lookup"><span data-stu-id="95387-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="95387-168">唯讀。</span><span class="sxs-lookup"><span data-stu-id="95387-168">Read-only.</span></span> <span data-ttu-id="95387-169">由 MFT 設定。</span><span class="sxs-lookup"><span data-stu-id="95387-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="95387-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95387-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95387-171">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="95387-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
