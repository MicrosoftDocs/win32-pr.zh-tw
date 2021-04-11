---
description: 使用 SQL-DMO 媒體類型
ms.assetid: 1aaf7554-1a5f-439a-afb1-a031607e1a1e
title: 使用 SQL-DMO 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db172538280a5dcdc6f4ffe91c19ac1d51e91ef9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945621"
---
# <a name="working-with-dmo-media-types"></a><span data-ttu-id="41759-103">使用 SQL-DMO 媒體類型</span><span class="sxs-lookup"><span data-stu-id="41759-103">Working with DMO Media Types</span></span>

<span data-ttu-id="41759-104">編解碼器 DMOs 所使用的輸入和輸出媒體類型是使用 [**Sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 結構來定義。</span><span class="sxs-lookup"><span data-stu-id="41759-104">The input and output media types that are used by the codec DMOs are defined using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="41759-105">此結構等同于在 Windows Media 格式 SDK 中定義的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)，以及在 Microsoft DirectShow®中定義的 [**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)。</span><span class="sxs-lookup"><span data-stu-id="41759-105">This structure is identical to both [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type), which is defined in the Windows Media Format SDK, and [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), which is defined in Microsoft DirectShow®.</span></span> <span data-ttu-id="41759-106">視您的應用程式而定，您可以使用定義為這三種類型之一的變數。</span><span class="sxs-lookup"><span data-stu-id="41759-106">Depending upon your application, you may use variables defined as any one of these three types.</span></span> <span data-ttu-id="41759-107">將指標轉換成另一個媒體類型結構的指標是安全的。</span><span class="sxs-lookup"><span data-stu-id="41759-107">It is safe to cast a pointer to one of the media type structures as another.</span></span> <span data-ttu-id="41759-108">例如：</span><span class="sxs-lookup"><span data-stu-id="41759-108">For example:</span></span>


```
    DMO_MEDIA_TYPE MediaType;
    WM_MEDIA_TYPE* pMedia = NULL;
    pMedia = (WM_MEDIA_TYPE*)&MediaType;
```



<span data-ttu-id="41759-109">編解碼器所使用的格式類型通常會限制為 **VIDEOINFOHEADER** 和 **WAVEFORMATEX** 結構所描述的格式類型。</span><span class="sxs-lookup"><span data-stu-id="41759-109">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span> <span data-ttu-id="41759-110">為了方便起見，這些格式類型的常數會包含在 wmcodecconst 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="41759-110">For convenience, constants for these format types are included in the wmcodecconst.h header file.</span></span> <span data-ttu-id="41759-111">常數名稱分別為 WMCFORMAT \_ VideoInfo 和 WMCFORMAT \_ WaveFormatEx。</span><span class="sxs-lookup"><span data-stu-id="41759-111">The constant names are WMCFORMAT\_VideoInfo and WMCFORMAT\_WaveFormatEx respectively.</span></span> <span data-ttu-id="41759-112">音訊編解碼器在某些情況下可以使用 **WAVEFORMATEXTENSIBLE** 結構，而且必須在其他環境中使用。</span><span class="sxs-lookup"><span data-stu-id="41759-112">The audio codecs can work with the **WAVEFORMATEXTENSIBLE** structure in some circumstances, and must use it in others.</span></span> <span data-ttu-id="41759-113">不過， **\_ \_ formattype** 會設定為與 **WAVEFORMATEX** 相同的值。</span><span class="sxs-lookup"><span data-stu-id="41759-113">However, **DMO\_MEDIA\_TYPE.formattype** is set to the same value as it is for **WAVEFORMATEX**.</span></span> <span data-ttu-id="41759-114">如需使用 **WAVEFORMATEXTENSIBLE** 的詳細資訊，請參閱 [使用 High-Definition 音訊](usinghighdefinitionaudio.md)。</span><span class="sxs-lookup"><span data-stu-id="41759-114">For more information about using **WAVEFORMATEXTENSIBLE**, see [Using High-Definition Audio](usinghighdefinitionaudio.md).</span></span>

> [!Note]  
>    <span data-ttu-id="41759-115">您必須在用來儲存壓縮資料的任何容器中包含用來當做編碼器輸出的格式類型結構。</span><span class="sxs-lookup"><span data-stu-id="41759-115">You must include the format type structure used as the encoder output in whatever container you use to store the compressed data.</span></span> <span data-ttu-id="41759-116">這些解碼器需要原始格式結構才能將內容解壓縮。</span><span class="sxs-lookup"><span data-stu-id="41759-116">The decoders require the original format structure to decompress the content.</span></span> <span data-ttu-id="41759-117">除了結構的成員之外，壓縮的 Windows Media 音訊和影片類型還需要額外的格式資訊，這些資訊會附加至結構。</span><span class="sxs-lookup"><span data-stu-id="41759-117">In addition to the members of the structure, compressed Windows Media Audio and Video types require additional format information, which is appended to the structure.</span></span> <span data-ttu-id="41759-118">如需詳細資訊，請參閱使用 [音訊](workingwithaudio.md) 和使用 [影片](workingwithvideo.md)。</span><span class="sxs-lookup"><span data-stu-id="41759-118">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="41759-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="41759-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41759-120">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="41759-120">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
