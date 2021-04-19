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
# <a name="uncompressed-audio-media-types"></a>未壓縮的音訊媒體類型

若要建立完整的未壓縮音訊類型，請在 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面指標上至少設定下列屬性。



| 屬性                                                                                    | 描述                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                                    | 主要類型。 設定為 [MFMediaType \_ 音訊]。                                                                                       |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                           | 亞。 請參閱 [音訊子類型 guid](audio-subtype-guids.md)。                                                                 |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                   | 音訊聲道數目。                                                                                                    |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)      | 每秒音訊樣本數。                                                                                          |
| [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)             | 封鎖對齊。                                                                                                             |
| [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 每秒的平均位元組數。                                                                                          |
| [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)            | 每個音訊樣本的位數數目。                                                                                             |
| [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md)         | 指定每個音訊範例是否獨立。 MFAudioFormat  \_ PCM 和 MFAudioFormat Float 格式的設定為 TRUE \_ 。 |



 

此外，某些音訊格式需要下列屬性。



| 屬性                                                                                      | 描述                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊有效位數**](mf-mt-audio-valid-bits-per-sample-attribute.md) | 每個音訊樣本中音訊資料的有效位數。 如果音訊樣本具有填補，請設定此屬性，也就是，如果每個音訊樣本中的有效位數小於樣本大小，則設定此屬性。 |
| [**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**](mf-mt-audio-channel-mask-attribute.md)                     | 將音訊頻道指派給喇叭的位置。 針對多頻道音訊資料流程（例如5.1）設定這個屬性。 Mono 或身歷聲音訊不需要這個屬性。                       |



 

### <a name="example-code"></a>範例程式碼

下列程式碼說明如何建立未壓縮 PCM 音訊的媒體類型。


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



下一個範例會採用編碼的音訊格式作為輸入，並建立相符的 PCM 音訊類型。 例如，此類型適合在編碼器或解碼器上設定。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> </dl>

 

 



