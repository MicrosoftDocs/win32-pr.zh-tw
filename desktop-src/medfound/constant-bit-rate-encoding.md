---
description: 常數位元速率編碼
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: 常數位元速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936560"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="12e34-103">常數位元速率編碼</span><span class="sxs-lookup"><span data-stu-id="12e34-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="12e34-104">以固定位元速率 (CBR) 編碼方式，編碼器會在編碼會話開始之前，知道輸出媒體範例的位元速率，以及緩衝區視窗 (有漏洞 bucket 參數) 。</span><span class="sxs-lookup"><span data-stu-id="12e34-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="12e34-105">編碼器會使用相同數目的位數來編碼整個檔案期間的每秒樣本，以達到資料流程的目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="12e34-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="12e34-106">這會限制資料流程範例大小的變化。</span><span class="sxs-lookup"><span data-stu-id="12e34-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="12e34-107">此外，編碼會話期間的位元速率不會完全符合指定的值，但會保持接近目標位速率。</span><span class="sxs-lookup"><span data-stu-id="12e34-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="12e34-108">CBR 編碼在您想要在不剖析完整檔案的情況下，想知道位元速率或檔案的約略長度時十分好用。</span><span class="sxs-lookup"><span data-stu-id="12e34-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="12e34-109">這在即時資料流中是必要的，因為媒體內容需要以可預測的位元速率以及固定的頻寬用量來進行串流。</span><span class="sxs-lookup"><span data-stu-id="12e34-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="12e34-110">CBR 編碼的缺點是編碼內容的品質不會是常數。</span><span class="sxs-lookup"><span data-stu-id="12e34-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="12e34-111">因為有些內容較難壓縮，所以 CBR 串流的部分會比其他部分的品質低。</span><span class="sxs-lookup"><span data-stu-id="12e34-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="12e34-112">例如，典型的電影有一些相當靜態的場景，以及一些完全行動的場景。</span><span class="sxs-lookup"><span data-stu-id="12e34-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="12e34-113">如果您使用 CBR 將電影編碼、靜態的場景，因此可以有效率地編碼，則其品質會比動作場景高，但需要較高的取樣大小才能維持相同的品質。</span><span class="sxs-lookup"><span data-stu-id="12e34-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="12e34-114">一般而言，CBR 檔案品質的變化會以較低的位元速率更明顯。</span><span class="sxs-lookup"><span data-stu-id="12e34-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="12e34-115">以較高的位元速率來說，CBR 編碼檔案的品質仍會有所不同，但對使用者而言，品質問題將會比較不明顯。</span><span class="sxs-lookup"><span data-stu-id="12e34-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="12e34-116">使用 CBR 編碼時，您應該在傳遞案例允許的情況下設定最高的頻寬。</span><span class="sxs-lookup"><span data-stu-id="12e34-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="12e34-117">CBR 設定</span><span class="sxs-lookup"><span data-stu-id="12e34-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="12e34-118">有漏洞 Bucket 設定</span><span class="sxs-lookup"><span data-stu-id="12e34-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="12e34-119">CBR 設定</span><span class="sxs-lookup"><span data-stu-id="12e34-119">CBR Configuration Settings</span></span>

<span data-ttu-id="12e34-120">您必須在編碼會話之前，指定編碼類型和各種資料流程特定設定，以設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="12e34-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="12e34-121">**設定用於 CBR 編碼的編碼器**</span><span class="sxs-lookup"><span data-stu-id="12e34-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="12e34-122">指定 CBR 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="12e34-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="12e34-123">根據預設，編碼器會設定為使用 CBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="12e34-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="12e34-124">編碼器設定會透過屬性值設定。</span><span class="sxs-lookup"><span data-stu-id="12e34-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="12e34-125">這些屬性是在 wmcodecdsp 中定義。</span><span class="sxs-lookup"><span data-stu-id="12e34-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="12e34-126">您可以將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性設定為 VARIANT FALSE，以明確指定此模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="12e34-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="12e34-127">如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="12e34-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="12e34-128">選擇編碼位元速率。</span><span class="sxs-lookup"><span data-stu-id="12e34-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="12e34-129">針對 CBR 編碼，您必須在編碼會話開始之前，知道您想要對資料流程進行編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="12e34-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="12e34-130">您必須在設定編碼器的期間設定位元速率。</span><span class="sxs-lookup"><span data-stu-id="12e34-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="12e34-131">若要執行這項操作，請在執行媒體類型協商時，檢查音訊串流的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 () 或 [適用于影片) 串流的 [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (針對可用的輸出媒體類型，並選擇最接近您要達到的目標位速率的輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="12e34-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="12e34-132">如需詳細資訊，請參閱 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="12e34-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="12e34-133">下列程式碼範例顯示 SetEncodingProperties 的執行。</span><span class="sxs-lookup"><span data-stu-id="12e34-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="12e34-134">此函式會設定 CBR 和 VBR 的資料流程層級編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="12e34-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="12e34-135">有漏洞 Bucket 設定</span><span class="sxs-lookup"><span data-stu-id="12e34-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="12e34-136">針對 CBR 編碼，資料流程的平均和最大有漏洞 bucket 值相同。</span><span class="sxs-lookup"><span data-stu-id="12e34-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="12e34-137">如需這些參數的詳細資訊，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。</span><span class="sxs-lookup"><span data-stu-id="12e34-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="12e34-138">若要對音訊串流進行 CBR 編碼，您必須在在編碼器上協商輸出媒體類型之後，設定有漏洞值區的值。</span><span class="sxs-lookup"><span data-stu-id="12e34-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="12e34-139">編碼器會根據輸出媒體類型上設定的平均位元速率，在內部計算緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="12e34-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="12e34-140">若要設定有漏洞值區值，請建立 Dword 陣列，以便在媒體接收器的屬性存放區中，于 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性中設定下列值。</span><span class="sxs-lookup"><span data-stu-id="12e34-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="12e34-141">如需詳細資訊，請參閱 [設定 File 接收中的屬性](setting-properties-in-the-file-sink.md)。</span><span class="sxs-lookup"><span data-stu-id="12e34-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="12e34-142">平均位元速率：從媒體類型協商期間選取的輸出媒體類型取得平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="12e34-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="12e34-143">使用「 [**\_ 每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) 」屬性。</span><span class="sxs-lookup"><span data-stu-id="12e34-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="12e34-144">緩衝區視窗：查詢 [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) 介面的編碼器，然後呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces .h，wmcodecdspuuid .lib) 。</span><span class="sxs-lookup"><span data-stu-id="12e34-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="12e34-145">初始緩衝區大小：設定為0。</span><span class="sxs-lookup"><span data-stu-id="12e34-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12e34-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="12e34-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12e34-147">ASF 編碼類型</span><span class="sxs-lookup"><span data-stu-id="12e34-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="12e34-148">教學課程： 1-傳遞 Windows Media 編碼</span><span class="sxs-lookup"><span data-stu-id="12e34-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="12e34-149">教學課程：使用 CBR 編碼方式撰寫 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="12e34-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
