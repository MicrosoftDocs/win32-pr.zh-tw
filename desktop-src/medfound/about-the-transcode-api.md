---
description: 關於轉碼 API
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: 關於轉碼 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555148"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="808ad-103">關於轉碼 API</span><span class="sxs-lookup"><span data-stu-id="808ad-103">About the Transcode API</span></span>

<span data-ttu-id="808ad-104">下圖顯示轉碼 API 與媒體基礎編碼管線的其餘部分之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="808ad-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![顯示轉碼 api 的圖表。](images/encoding08.png)

<span data-ttu-id="808ad-106">編碼管線包含下列資料處理物件：</span><span class="sxs-lookup"><span data-stu-id="808ad-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="808ad-107">媒體來源</span><span class="sxs-lookup"><span data-stu-id="808ad-107">Media source</span></span>
-   <span data-ttu-id="808ad-108">解碼器</span><span class="sxs-lookup"><span data-stu-id="808ad-108">Decoder</span></span>
-   <span data-ttu-id="808ad-109">影片尺寸調整或音訊 resampler</span><span class="sxs-lookup"><span data-stu-id="808ad-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="808ad-110">編碼器</span><span class="sxs-lookup"><span data-stu-id="808ad-110">Encoder</span></span>
-   <span data-ttu-id="808ad-111">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="808ad-111">Media sink</span></span>

<span data-ttu-id="808ad-112">只有當輸出影片的大小與來源不同時，才需要影片尺寸調整器。</span><span class="sxs-lookup"><span data-stu-id="808ad-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="808ad-113">只有當音訊需要在編碼之前重新取樣時，才需要音訊 resampler。</span><span class="sxs-lookup"><span data-stu-id="808ad-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="808ad-114">必須要有解碼/編碼器組，才能進行轉碼，但無法用於 remuxing。</span><span class="sxs-lookup"><span data-stu-id="808ad-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="808ad-115">編碼 *拓撲* 是一組管線物件， (來源、解碼器、調整器、resampler、編碼器和媒體接收器) ，以及兩者之間的連接點。</span><span class="sxs-lookup"><span data-stu-id="808ad-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="808ad-116">如需拓撲的詳細資訊，請參閱 [拓撲](topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="808ad-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="808ad-117">不同的元件會負責建立各種管線物件：</span><span class="sxs-lookup"><span data-stu-id="808ad-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="808ad-118">應用程式通常會使用 [來源解析程式](source-resolver.md) 來建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="808ad-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="808ad-119">[媒體會話](media-session.md)會載入並設定「解碼器」、「影片調整」和「音訊 resampler。</span><span class="sxs-lookup"><span data-stu-id="808ad-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="808ad-120">就內部而言，它會使用拓撲載入器來進行這 (請參閱 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)) 。</span><span class="sxs-lookup"><span data-stu-id="808ad-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="808ad-121">轉碼 API 會載入並設定編碼器和媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="808ad-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="808ad-122">Advanced applications 可以直接設定編碼器和媒體接收，而不是使用轉碼 API。</span><span class="sxs-lookup"><span data-stu-id="808ad-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="808ad-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="808ad-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="808ad-124">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="808ad-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="808ad-125">使用轉碼 API</span><span class="sxs-lookup"><span data-stu-id="808ad-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



