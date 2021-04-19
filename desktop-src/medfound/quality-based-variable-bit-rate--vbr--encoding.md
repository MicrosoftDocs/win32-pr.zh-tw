---
description: Quality-Based 變數位速率編碼
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Quality-Based 變數位速率編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989926"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="80514-103">Quality-Based 變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="80514-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="80514-104">不同于 [常數的位元速率編碼](constant-bit-rate-encoding.md) (CBR) ，編碼器會致力於維持編碼媒體的特定位元速率，以變數位元速率 (VBR) 模式，而編碼器會致力於達到編碼媒體的最佳品質。</span><span class="sxs-lookup"><span data-stu-id="80514-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="80514-105">CBR 和 VBR 之間的主要差異在於使用的緩衝區視窗大小。</span><span class="sxs-lookup"><span data-stu-id="80514-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="80514-106">相較于 CBR 編碼的資料流程，VBR 編碼的資料流程通常會有大型的緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="80514-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="80514-107">編碼內容的品質取決於壓縮內容時遺失的資料量。</span><span class="sxs-lookup"><span data-stu-id="80514-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="80514-108">許多因素會影響壓縮進程中的資料遺失;但一般而言，原始資料越複雜，壓縮的比率越高，壓縮程式就會遺失更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="80514-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="80514-109">在以品質為基礎的 VBR 模式中，您不會定義位元速率或編碼器必須遵循的緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="80514-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="80514-110">相反地，您可以指定數位媒體串流的品質層級，而不是位元速率。</span><span class="sxs-lookup"><span data-stu-id="80514-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="80514-111">編碼器會壓縮內容，讓所有範例都具有相當的品質;這可確保在整個播放期間的品質都一致，不論產生之資料流程的緩衝區需求為何。</span><span class="sxs-lookup"><span data-stu-id="80514-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="80514-112">以品質為基礎的 VBR 編碼通常會建立大型的壓縮資料流程。</span><span class="sxs-lookup"><span data-stu-id="80514-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="80514-113">一般而言，這種編碼方式非常適合本機播放或高頻寬網路連線， (或下載並播放) 。</span><span class="sxs-lookup"><span data-stu-id="80514-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="80514-114">例如，您可以撰寫應用程式，從 CD 將歌曲複製到電腦上的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="80514-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="80514-115">使用以品質為基礎的 VBR 編碼，可確保複製的所有歌曲都具有相同的品質。</span><span class="sxs-lookup"><span data-stu-id="80514-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="80514-116">在這些情況下，一致的品質將提供更好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="80514-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="80514-117">以品質為基礎之 VBR 編碼的缺點是，在編碼會話之前，沒有任何方法可以得知編碼媒體的大小或頻寬需求，因為編碼器會使用單一編碼階段。</span><span class="sxs-lookup"><span data-stu-id="80514-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="80514-118">這可以讓以品質為基礎的 VBR 編碼檔案不適用於記憶體或頻寬受限的情況，例如在便攜媒體播放機上播放內容，或透過低頻寬網路進行串流處理。</span><span class="sxs-lookup"><span data-stu-id="80514-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="80514-119">設定 Quality-Based VBR 編碼的編碼器</span><span class="sxs-lookup"><span data-stu-id="80514-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="80514-120">編碼器設定會透過屬性值設定。</span><span class="sxs-lookup"><span data-stu-id="80514-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="80514-121">這些屬性是在 wmcodecdsp 中定義。</span><span class="sxs-lookup"><span data-stu-id="80514-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="80514-122">必須先在編碼器上設定設定屬性，才能協商輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="80514-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="80514-123">如需有關如何設定編碼器屬性的詳細資訊，請參閱設定 [編碼器](configuring-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="80514-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="80514-124">下列清單顯示您必須為這種編碼類型設定的屬性：</span><span class="sxs-lookup"><span data-stu-id="80514-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="80514-125">將 **MFPKEY \_ VBRENABLED** 屬性設定為 VARIANT TRUE，以指定 VBR 編碼模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="80514-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="80514-126">將 **MFPKEY \_ PASSESUSED** 設定為1，因為這個 VBR 模式會使用一次編碼。</span><span class="sxs-lookup"><span data-stu-id="80514-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="80514-127">藉由設定 **MFPKEY \_ 所需的 \_ VBRQUALITY** 屬性，將所需的品質層級 (從0到 100) 。</span><span class="sxs-lookup"><span data-stu-id="80514-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="80514-128">以品質為基礎的 VBR 不會將內容編碼為任何預先定義的緩衝區參數。</span><span class="sxs-lookup"><span data-stu-id="80514-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="80514-129">此品質層級會針對整個資料流程進行維護，而不論所產生的位元速率需求為何。</span><span class="sxs-lookup"><span data-stu-id="80514-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="80514-130">若為影片串流，請在編碼器的輸出媒體類型上，將平均位元速率設定為 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性中的非零值。</span><span class="sxs-lookup"><span data-stu-id="80514-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="80514-131">編碼會話完成後，會更新正確的位元速率。</span><span class="sxs-lookup"><span data-stu-id="80514-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="80514-132">下列程式碼範例顯示 SetEncodingProperties 的執行。</span><span class="sxs-lookup"><span data-stu-id="80514-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="80514-133">此函式會設定 CBR 和 VBR 的資料流程層級編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="80514-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="80514-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="80514-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80514-135">ASF 編碼類型</span><span class="sxs-lookup"><span data-stu-id="80514-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



