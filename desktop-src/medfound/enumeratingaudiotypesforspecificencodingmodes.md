---
description: 列舉特定編碼模式的音訊類型
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: '列舉特定編碼模式的音訊類型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386029"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="d0106-103">列舉特定編碼模式的音訊類型 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="d0106-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="d0106-104">音訊編碼器所接受的輸入和輸出媒體類型都是結構化的。</span><span class="sxs-lookup"><span data-stu-id="d0106-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="d0106-105">您必須藉由呼叫 **IMediaObject：： GetOutputType** 方法或 **IMFTransform：： GetOutputType** 來取得支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d0106-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="d0106-106">取得輸出型別之後，您就不能修改它。</span><span class="sxs-lookup"><span data-stu-id="d0106-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="d0106-107">如果您想要使用非單向 CBR 的編碼模式，您必須設定模式，然後列舉該模式的輸出類型。編碼器會根據設定的模式變更支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d0106-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="d0106-108">控制編碼模式的屬性為 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 和 [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="d0106-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="d0106-109">當您在編碼器中設定模式時，您必須使用它來列舉和選取輸出類型，而不需要變更，就像使用 CBR 一樣。</span><span class="sxs-lookup"><span data-stu-id="d0106-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="d0106-110">識別以品質為基礎的 VBR 類型</span><span class="sxs-lookup"><span data-stu-id="d0106-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="d0106-111">識別品質型 VBR 類型的程式，取決於編碼器是否作為 DirectX 媒體物件 (的) 或作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="d0106-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="d0106-112">如需編碼器作為一或 MFT 的詳細資訊，請參閱 [編解碼器物件](codecobjects.md)底下的個別編解碼器參考頁面。</span><span class="sxs-lookup"><span data-stu-id="d0106-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="d0106-113">當音訊編碼器作為一，且您將編碼器設定為使用一次的 VBR 時，它會列舉所有支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d0106-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="d0106-114">不過，您通常會想要根據 quality 參數選取一次傳遞的 VBR 型別。</span><span class="sxs-lookup"><span data-stu-id="d0106-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="d0106-115">編碼器會在 WAVEFORMATEX 結構的 NAvgBytesPerSec 成員中，將單一傳遞的 VBR 輸出類型的品質值放在結構的成員中 **\_ \_ 。 pbFormat**。</span><span class="sxs-lookup"><span data-stu-id="d0106-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="d0106-116">此值會以下列格式儲存：0x7FFFFFXX，其中 XX 是從0到 100)  (的品質值。</span><span class="sxs-lookup"><span data-stu-id="d0106-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="d0106-117">例如，0x7FFFFF62 的 **nAvgBytesPerSec** 值會指定品質層級 98 (0x62 = 98) 。</span><span class="sxs-lookup"><span data-stu-id="d0106-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="d0106-118">下列範例將示範如何在編碼器作為的時候，檢查格式的品質等級。</span><span class="sxs-lookup"><span data-stu-id="d0106-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="d0106-119">當編碼器做為 MFT 時，它會在呼叫 **GetAvailableOutputType** 時列舉輸出型別，您可以針對 **MFPKEY 最近列舉的 \_ \_ \_ \_ VBRQUALITY** 屬性查詢 MFT。</span><span class="sxs-lookup"><span data-stu-id="d0106-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="d0106-120">傳回的值表示最近傳回之輸出媒體類型的 VBR 品質。</span><span class="sxs-lookup"><span data-stu-id="d0106-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="d0106-121">然後您可以使用該值來設定編碼器的 [**MFPKEY \_ 所需 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0106-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="d0106-122">設定尖峰條件約束</span><span class="sxs-lookup"><span data-stu-id="d0106-122">Setting Peak Constraints</span></span>

<span data-ttu-id="d0106-123">針對以品質為基礎的 VBR (一次傳遞) 和未受限制的雙向 VBR，在抓取輸出類型之後，不需要其他設定。</span><span class="sxs-lookup"><span data-stu-id="d0106-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="d0106-124">若要使用尖峰限制的 VBR，請取出啟用 VBR 的輸出類型，並設定兩個階段。</span><span class="sxs-lookup"><span data-stu-id="d0106-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="d0106-125">此類型（沒有變更）描述未受限制的 VBR 設定。</span><span class="sxs-lookup"><span data-stu-id="d0106-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="d0106-126">若要設定尖峰條件約束，請設定 [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) 和 [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0106-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0106-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0106-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0106-128">設定音訊編碼</span><span class="sxs-lookup"><span data-stu-id="d0106-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="d0106-129">尋找音訊編碼器輸出類型</span><span class="sxs-lookup"><span data-stu-id="d0106-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="d0106-130">使用 Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="d0106-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="d0106-131">使用 VBR 編碼</span><span class="sxs-lookup"><span data-stu-id="d0106-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



