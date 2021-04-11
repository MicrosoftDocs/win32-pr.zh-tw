---
description: 使用 High-Definition 音訊
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: '使用 High-Definition 音訊 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692296"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="4734f-103">使用 High-Definition 音訊 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="4734f-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4734f-104">高定義音訊在 Windows Media 音訊編解碼器的內容中，是具有兩個以上頻道或每個樣本超過16個位的任何音訊類型。</span><span class="sxs-lookup"><span data-stu-id="4734f-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="4734f-105">[Windows Media 音訊編碼器](windowsmediaaudioencoder.md)的 Professional 和無損類別支援高定義音訊。</span><span class="sxs-lookup"><span data-stu-id="4734f-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="4734f-106">未壓縮的高定義音訊類型會使用 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構來定義。</span><span class="sxs-lookup"><span data-stu-id="4734f-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="4734f-107">**WAVEFORMATEXTENSIBLE** 是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構的結構化延伸。</span><span class="sxs-lookup"><span data-stu-id="4734f-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="4734f-108">當您使用 DMOs 時， **formattype** 成員（描述高 [**定義 \_ \_ 音訊類型）**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 必須設定為 WMCFORMAT \_ WaveFormatEx，就如同一般音訊一樣， **WAVEFORMATEXTENSIBLE** 沒有特殊的格式識別碼。</span><span class="sxs-lookup"><span data-stu-id="4734f-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="4734f-109">如果格式使用 **WAVEFORMATEXTENSIBLE** ，您必須將 **WAVEFORMATEX** 結構的 **cbSize** 成員設定為22。</span><span class="sxs-lookup"><span data-stu-id="4734f-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="4734f-110">使用媒體基礎時，您可以使用函數 [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)，從 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))結構建立正確的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4734f-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="4734f-111">Windows Media 音訊10專業版編解碼器所支援的多通道輸出類型不會使用 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))，但會在 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構中報告每個樣本的正確通道數目和位數。</span><span class="sxs-lookup"><span data-stu-id="4734f-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="4734f-112">如同所有會描述壓縮 Windows Media 音訊內容的音訊類型，額外的資訊會附加至 **WAVEFORMATEX** 結構，以供解碼器用於解壓縮。</span><span class="sxs-lookup"><span data-stu-id="4734f-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="4734f-113">解碼 High-Definition 音訊</span><span class="sxs-lookup"><span data-stu-id="4734f-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="4734f-114">若要解碼高定義音訊，您必須將 [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="4734f-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="4734f-115">如果未設定此屬性，則不論壓縮格式為何，此解碼器都會傳遞最多每個樣本16位的身歷聲內容。</span><span class="sxs-lookup"><span data-stu-id="4734f-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="4734f-116">只有 Windows XP、Windows Vista 及更新版本才支援高定義音訊。</span><span class="sxs-lookup"><span data-stu-id="4734f-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="4734f-117">在舊版的 Windows 上，使用 high 定義編碼的 Windows Media 音訊內容會轉譯為雙聲道音訊，每個樣本最多16個位。</span><span class="sxs-lookup"><span data-stu-id="4734f-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4734f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="4734f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4734f-119">使用音訊</span><span class="sxs-lookup"><span data-stu-id="4734f-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
