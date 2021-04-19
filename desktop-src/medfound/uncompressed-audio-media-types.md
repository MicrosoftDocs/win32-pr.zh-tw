---
description: 未壓縮的音訊媒體類型
ms.assetid: 130a18a9-1c86-4d16-a8ae-ed57bf50f9bb
title: 未壓縮的音訊媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d15f7211ef16d4280476f93744650b88742073
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981738"
---
# <a name="uncompressed-audio-media-types"></a><span data-ttu-id="de8dd-103">未壓縮的音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="de8dd-103">Uncompressed Audio Media Types</span></span>

<span data-ttu-id="de8dd-104">若要建立完整的未壓縮音訊類型，請在 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面指標上至少設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="de8dd-104">To create a complete uncompressed audio type, set at least the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="de8dd-105">屬性</span><span class="sxs-lookup"><span data-stu-id="de8dd-105">Attribute</span></span>                                                                                    | <span data-ttu-id="de8dd-106">描述</span><span class="sxs-lookup"><span data-stu-id="de8dd-106">Description</span></span>                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de8dd-107">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="de8dd-107">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="de8dd-108">主要類型。</span><span class="sxs-lookup"><span data-stu-id="de8dd-108">Major type.</span></span> <span data-ttu-id="de8dd-109">設定為 [MFMediaType \_ 音訊]。</span><span class="sxs-lookup"><span data-stu-id="de8dd-109">Set to MFMediaType\_Audio.</span></span>                                                                                       |
| [<span data-ttu-id="de8dd-110">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="de8dd-110">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="de8dd-111">亞。</span><span class="sxs-lookup"><span data-stu-id="de8dd-111">Subtype.</span></span> <span data-ttu-id="de8dd-112">請參閱 [音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="de8dd-112">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>                                                                 |
| [<span data-ttu-id="de8dd-113">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="de8dd-113">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="de8dd-114">音訊聲道數目。</span><span class="sxs-lookup"><span data-stu-id="de8dd-114">Number of audio channels.</span></span>                                                                                                    |
| [<span data-ttu-id="de8dd-115">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="de8dd-115">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="de8dd-116">每秒音訊樣本數。</span><span class="sxs-lookup"><span data-stu-id="de8dd-116">Number of audio samples per second.</span></span>                                                                                          |
| [<span data-ttu-id="de8dd-117">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="de8dd-117">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="de8dd-118">封鎖對齊。</span><span class="sxs-lookup"><span data-stu-id="de8dd-118">Block alignment.</span></span>                                                                                                             |
| [<span data-ttu-id="de8dd-119">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="de8dd-119">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="de8dd-120">每秒的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="de8dd-120">Average number of bytes per second.</span></span>                                                                                          |
| [<span data-ttu-id="de8dd-121">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="de8dd-121">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="de8dd-122">每個音訊樣本的位數數目。</span><span class="sxs-lookup"><span data-stu-id="de8dd-122">Number of bits per audio sample.</span></span>                                                                                             |
| [<span data-ttu-id="de8dd-123">**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="de8dd-123">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="de8dd-124">指定每個音訊範例是否獨立。</span><span class="sxs-lookup"><span data-stu-id="de8dd-124">Specifies whether each audio sample is independent.</span></span> <span data-ttu-id="de8dd-125">MFAudioFormat  \_ PCM 和 MFAudioFormat Float 格式的設定為 TRUE \_ 。</span><span class="sxs-lookup"><span data-stu-id="de8dd-125">Set to **TRUE** for MFAudioFormat\_PCM and MFAudioFormat\_Float formats.</span></span> |



 

<span data-ttu-id="de8dd-126">此外，某些音訊格式需要下列屬性。</span><span class="sxs-lookup"><span data-stu-id="de8dd-126">In addition, the following attributes are required for some audio formats.</span></span>



| <span data-ttu-id="de8dd-127">屬性</span><span class="sxs-lookup"><span data-stu-id="de8dd-127">Attribute</span></span>                                                                                      | <span data-ttu-id="de8dd-128">描述</span><span class="sxs-lookup"><span data-stu-id="de8dd-128">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de8dd-129">**\_ \_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊有效位數**</span><span class="sxs-lookup"><span data-stu-id="de8dd-129">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md) | <span data-ttu-id="de8dd-130">每個音訊樣本中音訊資料的有效位數。</span><span class="sxs-lookup"><span data-stu-id="de8dd-130">Number of valid bits of audio data in each audio sample.</span></span> <span data-ttu-id="de8dd-131">如果音訊樣本具有填補，請設定此屬性，也就是，如果每個音訊樣本中的有效位數小於樣本大小，則設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="de8dd-131">Set this attribute if the audio samples have padding—that is, if the number of valid bits in each audio sample is less than the sample size.</span></span> |
| [<span data-ttu-id="de8dd-132">**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="de8dd-132">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                     | <span data-ttu-id="de8dd-133">將音訊頻道指派給喇叭的位置。</span><span class="sxs-lookup"><span data-stu-id="de8dd-133">The assignment of audio channels to speaker positions.</span></span> <span data-ttu-id="de8dd-134">針對多頻道音訊資料流程（例如5.1）設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="de8dd-134">Set this attribute for multichannel audio streams, such as 5.1.</span></span> <span data-ttu-id="de8dd-135">Mono 或身歷聲音訊不需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="de8dd-135">This attribute is not required for mono or stereo audio.</span></span>                       |



 

### <a name="example-code"></a><span data-ttu-id="de8dd-136">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="de8dd-136">Example Code</span></span>

<span data-ttu-id="de8dd-137">下列程式碼說明如何建立未壓縮 PCM 音訊的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="de8dd-137">The following code shows how to create a media type for uncompressed PCM audio.</span></span>


```C++
HRESULT CreatePCMAudioType(
    UINT32 sampleRate,        // Samples per second
    UINT32 bitsPerSample,     // Bits per sample
    UINT32 cChannels,         // Number of channels
    IMFMediaType **ppType     // Receives a pointer to the media type.
    )
{
    HRESULT hr = S_OK;

    IMFMediaType *pType = NULL;

    // Calculate derived values.
    UINT32 blockAlign = cChannels * (bitsPerSample / 8);
    UINT32 bytesPerSecond = blockAlign * sampleRate;

    // Create the empty media type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set attributes on the type.
    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_NUM_CHANNELS, cChannels);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_SAMPLES_PER_SECOND, sampleRate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, blockAlign);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_AVG_BYTES_PER_SECOND, bytesPerSecond);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BITS_PER_SAMPLE, bitsPerSample);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the type to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="de8dd-138">下一個範例會採用編碼的音訊格式作為輸入，並建立相符的 PCM 音訊類型。</span><span class="sxs-lookup"><span data-stu-id="de8dd-138">The next example takes an encoded audio format as input, and creates a matching PCM audio type.</span></span> <span data-ttu-id="de8dd-139">例如，此類型適合在編碼器或解碼器上設定。</span><span class="sxs-lookup"><span data-stu-id="de8dd-139">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
//-------------------------------------------------------------------
// ConvertAudioTypeToPCM
//
// Given an audio media type (which might describe a compressed audio
// format), returns a media type that describes the equivalent
// uncompressed PCM format.
//-------------------------------------------------------------------

HRESULT ConvertAudioTypeToPCM(
    IMFMediaType *pType,        // Pointer to an encoded audio type.
    IMFMediaType **ppType       // Receives a matching PCM audio type.
    )
{
    HRESULT hr = S_OK;

    GUID majortype = { 0 };
    GUID subtype = { 0 };

    UINT32 cChannels = 0;
    UINT32 samplesPerSec = 0;
    UINT32 bitsPerSample = 0;

    hr = pType->GetMajorType(&majortype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (majortype != MFMediaType_Audio)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Get the audio subtype.
    hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (subtype == MFAudioFormat_PCM)
    {
        // This is already a PCM audio type. Return the same pointer.

        *ppType = pType;
        (*ppType)->AddRef();

        return S_OK;
    }

    // Get the sample rate and other information from the audio format.

    cChannels = MFGetAttributeUINT32(pType, MF_MT_AUDIO_NUM_CHANNELS, 0);
    samplesPerSec = MFGetAttributeUINT32(pType, MF_MT_AUDIO_SAMPLES_PER_SECOND, 0);
    bitsPerSample = MFGetAttributeUINT32(pType, MF_MT_AUDIO_BITS_PER_SAMPLE, 16);

    // Note: Some encoded audio formats do not contain a value for bits/sample.
    // In that case, use a default value of 16. Most codecs will accept this value.

    if (cChannels == 0 || samplesPerSec == 0)
    {
        return MF_E_INVALIDTYPE;
    }

    // Create the corresponding PCM audio type.
    hr = CreatePCMAudioType(samplesPerSec, bitsPerSample, cChannels, ppType);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="de8dd-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="de8dd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de8dd-141">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="de8dd-141">Audio Media Types</span></span>](audio-media-types.md)
</dt> </dl>

 

 



