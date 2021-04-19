---
description: 在以尖峰限制的變數位速率 (VBR) 中，內容會編碼為指定的位元速率和尖峰值：尖峰位元速率和尖峰緩衝區視窗。
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained 變數位速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987428"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="4c16c-103">Peak-Constrained 變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="4c16c-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="4c16c-104">在以尖峰限制的變數位速率 (VBR) 中，內容會編碼為指定的位元速率和尖峰 *值*：尖峰位元速率和尖峰緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="4c16c-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="4c16c-105">這些尖峰值也稱為 *尖峰有漏洞 bucket 值*。</span><span class="sxs-lookup"><span data-stu-id="4c16c-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="4c16c-106">檔案經過編碼，以符合尖峰值所描述的緩衝區，因此資料流程的整體平均位元速率等於或小於您指定的平均位元速率值。</span><span class="sxs-lookup"><span data-stu-id="4c16c-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="4c16c-107">通常，尖峰位速率很高。</span><span class="sxs-lookup"><span data-stu-id="4c16c-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="4c16c-108">編碼器可確保指定的平均位元速率值會在資料流程的持續時間內維持 (平均位元速率 >= (以秒為單位的資料流程大小總計（以秒為單位）) ) 。</span><span class="sxs-lookup"><span data-stu-id="4c16c-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="4c16c-109">請考慮下列範例：您設定的資料流程具有每秒16000位的平均位元速率、每秒48000位的尖峰位速率，以及 3000 (3 秒) 的尖峰緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="4c16c-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="4c16c-110">用於資料流程的緩衝區大小是每秒144000個位 (48000 位， \*) 由尖峰值決定。</span><span class="sxs-lookup"><span data-stu-id="4c16c-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="4c16c-111">編碼器會壓縮資料以符合該緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4c16c-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="4c16c-112">此外，資料流程的平均位元速率必須為16000或更少。</span><span class="sxs-lookup"><span data-stu-id="4c16c-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="4c16c-113">如果編碼器必須建立大型樣本來處理複雜的內容區段，它可以利用大型緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="4c16c-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="4c16c-114">但是資料流程的其他部分必須以較低的位元速率編碼，以將平均值帶到指定的層級。</span><span class="sxs-lookup"><span data-stu-id="4c16c-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="4c16c-115">尖峰限制的 VBR 編碼適用于具有有限緩衝區容量和資料速率條件約束的播放裝置。</span><span class="sxs-lookup"><span data-stu-id="4c16c-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="4c16c-116">其中一個常見的範例是在裝置上的晶片執行解碼時，用於 Dvd 的編碼方式是必須考慮的硬體限制。</span><span class="sxs-lookup"><span data-stu-id="4c16c-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="4c16c-117">設定 Peak-Constrained VBR 的編碼器</span><span class="sxs-lookup"><span data-stu-id="4c16c-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="4c16c-118">尖峰限制的 VBR 就像是不受 [限制的 vbr](unconstrained-variable-bit-rate--vbr--encoding.md) ，因為它會限制為數據流持續時間的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="4c16c-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="4c16c-119">此外，尖峰限制的 VBR 會符合尖峰緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4c16c-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="4c16c-120">此緩衝區是使用尖峰位元速率和尖峰緩衝區視窗來描述。</span><span class="sxs-lookup"><span data-stu-id="4c16c-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="4c16c-121">此模式會使用兩種編碼方式，並提供編碼器在編碼個別樣本的方式時的彈性，同時遵守尖峰限制。</span><span class="sxs-lookup"><span data-stu-id="4c16c-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="4c16c-122">編碼器設定會透過屬性值設定。</span><span class="sxs-lookup"><span data-stu-id="4c16c-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="4c16c-123">這些屬性是在 wmcodecdsp 中定義。</span><span class="sxs-lookup"><span data-stu-id="4c16c-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="4c16c-124">必須先在編碼器上設定設定屬性，才能協商輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4c16c-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="4c16c-125">如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="4c16c-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="4c16c-126">根據指定的屬性值，您可以列舉支援的 VBR 輸出類型，並根據平均位元速率，在編碼器 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="4c16c-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="4c16c-127">您必須設定下列 propertiesfor 這種類型的編碼方式：</span><span class="sxs-lookup"><span data-stu-id="4c16c-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="4c16c-128">將 MFPKEY \_ VBRENABLED 屬性設定為 VARIANT TRUE，以指定 VBR 編碼模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4c16c-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="4c16c-129">將 MFPKEY \_ PASSESUSED 設定為2，因為尖峰限制的 VBR 模式會使用兩個編碼階段。</span><span class="sxs-lookup"><span data-stu-id="4c16c-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="4c16c-130">設定 MFPKEY \_ RMAX 指定尖峰位速率，並設定 MFPKEY \_ BMAX 來指定尖峰緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="4c16c-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="4c16c-131">在列舉輸出媒體類型時，請檢查音訊串流的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 (針對 [音訊串流]) 或 [適用于影片) 串流的 [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (針對可用的輸出媒體類型，並選擇最接近您希望編碼器在編碼內容中維護之平均位元速率的平均位元速率的輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4c16c-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="4c16c-132">如需有關選取輸出媒體類型的詳細資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="4c16c-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="4c16c-133">建議您將尖峰位速率設定為至少兩倍的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="4c16c-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="4c16c-134">將尖峰速率設定為較低的值，可能會導致編碼器將內容編碼為兩次傳遞 CBR，而不是尖峰限制的 VBR。</span><span class="sxs-lookup"><span data-stu-id="4c16c-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="4c16c-135">若要取得由編碼器設定的緩衝區視窗值，請在編碼會話之後，呼叫 **IWMCodecLeakyBucket：： GetBufferSizeBits**（定義于 wmcodecifaces. h，wmcodecdspuuid）中。</span><span class="sxs-lookup"><span data-stu-id="4c16c-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="4c16c-136">若要為數據流新增未受限制的 VBR 支援，您必須在設定 ASF 設定檔時，于串流設定物件上 (尖峰有漏洞值區值) ，在 [ [**MF \_ \_**](mf-asfstreamconfig-leakybucket2-attribute.md) 值區值] 中設定此值。</span><span class="sxs-lookup"><span data-stu-id="4c16c-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="4c16c-137">下列程式碼範例會修改範例類別 CEncoder 的 SetEncodingType 方法，以設定尖峰限制的 VBR 模式。</span><span class="sxs-lookup"><span data-stu-id="4c16c-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="4c16c-138">如需此類別的詳細資訊，請參閱 [編碼器範例程式碼](encoder-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="4c16c-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="4c16c-139">如需此範例中所使用之 helper 宏的詳細資訊，請參閱使用媒體基礎程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="4c16c-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="4c16c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c16c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c16c-141">ASF 編碼類型</span><span class="sxs-lookup"><span data-stu-id="4c16c-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="4c16c-142">有漏洞 Bucket 緩衝區模型</span><span class="sxs-lookup"><span data-stu-id="4c16c-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="4c16c-143">如何建立 Two-Pass Windows Media 編碼的拓撲</span><span class="sxs-lookup"><span data-stu-id="4c16c-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



