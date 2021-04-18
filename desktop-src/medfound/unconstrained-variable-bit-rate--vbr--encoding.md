---
description: 不受限制的變數位速率編碼
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: 不受限制的變數位速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983419"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="d047d-103">不受限制的變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="d047d-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="d047d-104">在不受限制的變數位速率 (VBR) 編碼模式中，內容會編碼為可能的最高品質，同時維持指定的位元速率。</span><span class="sxs-lookup"><span data-stu-id="d047d-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="d047d-105">未受限制的 VBR 編碼會使用兩種編碼階段。</span><span class="sxs-lookup"><span data-stu-id="d047d-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="d047d-106">使用不受限制的 VBR 編碼時，您可以指定資料流程的位元速率，如同使用 [常數的位元速率編碼](constant-bit-rate-encoding.md)一樣。</span><span class="sxs-lookup"><span data-stu-id="d047d-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="d047d-107">不過，編碼器只會使用此值做為資料流程的平均位元速率，並進行編碼，讓品質盡可能高，同時維持平均。</span><span class="sxs-lookup"><span data-stu-id="d047d-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="d047d-108">編碼器所產生的個別樣本會因大小而異，而不會有任何明確的緩衝區限制。</span><span class="sxs-lookup"><span data-stu-id="d047d-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="d047d-109">不過，編碼會話期間的平均位元速率與資料流程的持續時間必須不超過您所指定的值。</span><span class="sxs-lookup"><span data-stu-id="d047d-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="d047d-110">編碼資料流程中任何時間點的實際位元速率可能會有極大的差異。</span><span class="sxs-lookup"><span data-stu-id="d047d-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="d047d-111">您未針對未受限制的 VBR 編碼設定緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="d047d-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="d047d-112">相反地，編碼器會根據編碼範例的需求，計算所需緩衝區視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="d047d-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="d047d-113">這表示，只要平均位元速率小於或等於您設定的值，資料流程中個別樣本的大小就沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="d047d-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="d047d-114">未受限制的 VBR 編碼的優點在於壓縮的資料流程具有最高的可能品質，同時維持在可預測的平均頻寬內。</span><span class="sxs-lookup"><span data-stu-id="d047d-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="d047d-115">當您需要指定頻寬，但可接受指定頻寬的波動時，請使用此值;例如，針對本機檔案或僅限下載。</span><span class="sxs-lookup"><span data-stu-id="d047d-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="d047d-116">這種編碼模式的缺點是，編碼器可以在編碼之後將緩衝區視窗設定為任何需要的值，讓您無法控制緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d047d-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="d047d-117">在大部分情況下，如果您不在意緩衝區大小或頻寬使用量的一致性，您應該使用 [品質型變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)</span><span class="sxs-lookup"><span data-stu-id="d047d-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="d047d-118">設定未受限制 VBR 的編碼器</span><span class="sxs-lookup"><span data-stu-id="d047d-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="d047d-119">編碼器設定會透過屬性值設定。</span><span class="sxs-lookup"><span data-stu-id="d047d-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="d047d-120">這些屬性是在 wmcodecdsp 中定義。</span><span class="sxs-lookup"><span data-stu-id="d047d-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="d047d-121">必須先在編碼器上設定設定屬性，才能協商輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d047d-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="d047d-122">如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="d047d-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="d047d-123">根據指定的屬性值，您可以列舉支援的 VBR 輸出類型，並根據平均位元速率，在編碼器 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="d047d-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="d047d-124">下列清單顯示您必須為這種編碼類型設定的屬性：</span><span class="sxs-lookup"><span data-stu-id="d047d-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="d047d-125">將 MFPKEY \_ VBRENABLED 屬性設定為 VARIANT TRUE，以指定 VBR 編碼模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d047d-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="d047d-126">將 MFPKEY \_ PASSESUSED 設定為2，因為未受限制的 VBR 模式會使用兩個編碼階段。</span><span class="sxs-lookup"><span data-stu-id="d047d-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="d047d-127">列舉輸出媒體類型時，請檢查音訊串流的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 () 或 [ [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (適用于可用輸出媒體類型的影片資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="d047d-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="d047d-128">選擇輸出媒體類型，其平均位元速率最接近您希望編碼器在編碼內容中維護的所需平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="d047d-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="d047d-129">如需有關選取輸出媒體類型的詳細資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="d047d-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="d047d-130">若要取得緩衝區視窗值，請在編碼會話之後，呼叫 **IWMCodecLeakyBucket：： GetBufferSizeBits**（定義于 wmcodecifaces .h 和 wmcodecdspuuid 中）。</span><span class="sxs-lookup"><span data-stu-id="d047d-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="d047d-131">若要為數據流新增不受限制的 VBR 支援，您必須在設定 ASF 設定檔時，于串流設定物件上 (平均有漏洞值區值) ，在 [ [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) ] 屬性中設定這個值。</span><span class="sxs-lookup"><span data-stu-id="d047d-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="d047d-132">下列範例會修改範例類別 CEncoder 的 SetEncodingType 方法，以設定未受限制的 VBR 模式。</span><span class="sxs-lookup"><span data-stu-id="d047d-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="d047d-133">如需此類別的詳細資訊，請參閱 [編碼器範例程式碼](encoder-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="d047d-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="d047d-134">如需此範例中所使用之 helper 宏的詳細資訊，請參閱使用媒體基礎程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="d047d-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="d047d-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d047d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d047d-136">ASF 編碼類型</span><span class="sxs-lookup"><span data-stu-id="d047d-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="d047d-137">有漏洞 Bucket 緩衝區模型</span><span class="sxs-lookup"><span data-stu-id="d047d-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="d047d-138">如何建立 Two-Pass Windows Media 編碼的拓撲</span><span class="sxs-lookup"><span data-stu-id="d047d-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



