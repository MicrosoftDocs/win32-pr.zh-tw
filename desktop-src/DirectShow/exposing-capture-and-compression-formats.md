---
description: 公開捕捉和壓縮格式
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: 公開捕捉和壓縮格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688496"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="fabeb-103">公開捕捉和壓縮格式</span><span class="sxs-lookup"><span data-stu-id="fabeb-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="fabeb-104">本文描述如何使用 [**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 方法來傳回捕捉和壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="fabeb-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="fabeb-105">這種方法可以取得所接受媒體類型的詳細資訊，而不是列舉釘選媒體類型的傳統方式，因此通常應該改用。</span><span class="sxs-lookup"><span data-stu-id="fabeb-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="fabeb-106">**GetStreamCaps** 可以傳回音頻或影片允許的格式類型相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fabeb-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="fabeb-107">此外，本文還提供一些範例程式碼，示範如何重新連接轉換篩選的輸入 pin，以確保您的篩選準則可以產生特定的輸出。</span><span class="sxs-lookup"><span data-stu-id="fabeb-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="fabeb-108">**GetStreamCaps** 方法會傳回一組媒體類型和功能結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="fabeb-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="fabeb-109">媒體類型是 [**\_ 媒體 \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) 類型結構，而功能則是以 [**音訊 \_ 串流設定 \_ \_ caps**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) 結構或 [**影片 \_ 串流設定 \_ \_ caps**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) 結構來表示。</span><span class="sxs-lookup"><span data-stu-id="fabeb-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="fabeb-110">本文的第一節提供影片範例，而第二個區段則呈現音訊範例。</span><span class="sxs-lookup"><span data-stu-id="fabeb-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="fabeb-111">本文包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="fabeb-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="fabeb-112">影片功能</span><span class="sxs-lookup"><span data-stu-id="fabeb-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="fabeb-113">音訊功能</span><span class="sxs-lookup"><span data-stu-id="fabeb-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="fabeb-114">重新連接您的輸入，以確保特定的輸出類型</span><span class="sxs-lookup"><span data-stu-id="fabeb-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="fabeb-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="fabeb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fabeb-116">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="fabeb-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



