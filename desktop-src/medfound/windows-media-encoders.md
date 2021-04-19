---
description: 編碼器會使用應用程式所指定的格式，將未壓縮的音訊或影片轉換成壓縮的封包。 若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 音訊和影片編解碼器。
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Media 編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106989114"
---
# <a name="windows-media-encoders"></a><span data-ttu-id="c5322-104">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="c5322-104">Windows Media Encoders</span></span>

<span data-ttu-id="c5322-105">編碼器會使用應用程式所指定的格式，將未壓縮的音訊或影片轉換成壓縮的封包。</span><span class="sxs-lookup"><span data-stu-id="c5322-105">An encoder converts uncompressed audio or video into compressed packets in the format specified by the application.</span></span> <span data-ttu-id="c5322-106">若要將媒體檔案轉換成 ASF 格式，您可以使用 Windows Media 音訊和影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="c5322-106">For converting media files into ASF format, you can use the Windows Media audio and video codecs.</span></span>

<span data-ttu-id="c5322-107">編碼器是由代表類別：音訊或影片的 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="c5322-107">An encoder is identified by the GUID that represents the category: audio or video.</span></span> <span data-ttu-id="c5322-108">編碼器的輸出類型是以媒體類型的主要和子類型 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="c5322-108">The encoder's output type is represented by a media type's major and the sub type GUID.</span></span>

-   <span data-ttu-id="c5322-109">Windows Media 音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="c5322-109">Windows Media audio codecs</span></span>

    <span data-ttu-id="c5322-110">類別： **MFT \_ 類別 \_ 音訊 \_ 編碼器**</span><span class="sxs-lookup"><span data-stu-id="c5322-110">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="c5322-111">主要類型： MFMediaType \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="c5322-111">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="c5322-112">子類型： MFAudioFormat \_ WMAudioV9、MFAudioFormat \_ WMAudioV8、MFAudioFormat \_ WMAudio \_ 無損、MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="c5322-112">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="c5322-113">Windows Media video 編解碼器</span><span class="sxs-lookup"><span data-stu-id="c5322-113">Windows Media video codecs</span></span>

    <span data-ttu-id="c5322-114">類別： **MFT \_ 類別 \_ 影片 \_ 編碼器**</span><span class="sxs-lookup"><span data-stu-id="c5322-114">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="c5322-115">主要類型： MFMediaType \_ 影片</span><span class="sxs-lookup"><span data-stu-id="c5322-115">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="c5322-116">子類型： MFVideoFormat \_ WVC1、MFVideoFormat \_ WMV3、MFVideoFormat \_ WMV2、MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="c5322-116">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="c5322-117">這些編碼器會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，媒體基礎可透過編碼器的 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面來提供應用程式的存取權。</span><span class="sxs-lookup"><span data-stu-id="c5322-117">These encoders are implemented as [Media Foundation transform](media-foundation-transforms.md) (MFT) and Media Foundation provides access to the application through the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the encoder.</span></span> <span data-ttu-id="c5322-118">如果您使用管線層元件進行 ASF 編碼，則編碼器 MFT 會以轉換節點的形式插入管線中，因為它負責將流經來源的媒體資料轉換為接收。</span><span class="sxs-lookup"><span data-stu-id="c5322-118">If you are using pipeline layer components for ASF encoding, the encoder MFT is inserted into the pipeline as a transform node because it is responsible for transforming media data that flows through the source to the sink.</span></span> <span data-ttu-id="c5322-119">如果來源是壓縮型別，則管線會新增必要的解碼器，以將來源轉換成未壓縮的型別。</span><span class="sxs-lookup"><span data-stu-id="c5322-119">If the source is a compressed type, then the pipeline adds the required decoders to convert the source into an uncompressed type.</span></span> <span data-ttu-id="c5322-120">編碼器有一個輸入資料流程和一個輸出資料流程。</span><span class="sxs-lookup"><span data-stu-id="c5322-120">An encoder has one input stream and one output stream.</span></span> <span data-ttu-id="c5322-121">編碼器會根據應用程式在編碼會話之前所設定的設定和格式，接收輸入資料並產生編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="c5322-121">The encoder receives input data and produces encoded data according to the configuration and format set by the application prior to the encoding session.</span></span> <span data-ttu-id="c5322-122">輸出資料流程的格式是由媒體類型所描述。</span><span class="sxs-lookup"><span data-stu-id="c5322-122">The format of the output stream is described by a media type.</span></span>

<span data-ttu-id="c5322-123">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="c5322-123">This section contains the following topics.</span></span>



| <span data-ttu-id="c5322-124">主題</span><span class="sxs-lookup"><span data-stu-id="c5322-124">Topic</span></span>                                                                              | <span data-ttu-id="c5322-125">描述</span><span class="sxs-lookup"><span data-stu-id="c5322-125">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5322-126">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="c5322-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)                  | <span data-ttu-id="c5322-127">說明如何建立編碼器。</span><span class="sxs-lookup"><span data-stu-id="c5322-127">Explains how to create the encoder.</span></span>                                                         |
| [<span data-ttu-id="c5322-128">編碼屬性</span><span class="sxs-lookup"><span data-stu-id="c5322-128">Encoding Properties</span></span>](configuring-the-encoder.md)                                 | <span data-ttu-id="c5322-129">說明如何藉由在編碼器 MFT 上設定適當的屬性來設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="c5322-129">Explains how to configure the encoder by setting appropriate properties on the encoder MFT.</span></span> |
| [<span data-ttu-id="c5322-130">編碼器上的媒體類型協商</span><span class="sxs-lookup"><span data-stu-id="c5322-130">Media Type Negotiation on the Encoder</span></span>](media-type-negotiation-on-the-encoder.md) | <span data-ttu-id="c5322-131">說明如何設定編碼器上的輸入和輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c5322-131">Explains how to set input and output media types on the encoder.</span></span>                            |
| [<span data-ttu-id="c5322-132">設定 WMV 編碼器</span><span class="sxs-lookup"><span data-stu-id="c5322-132">Configuring a WMV Encoder</span></span>](configuring-a-wmv-encoder.md)                         | <span data-ttu-id="c5322-133">說明如何設定 Windows Media 視訊 (WMV) 編碼器。</span><span class="sxs-lookup"><span data-stu-id="c5322-133">Explains how to configure a Windows Media Video (WMV) encoder.</span></span>                              |
| [<span data-ttu-id="c5322-134">設定 WMA 編碼器的輸出類型</span><span class="sxs-lookup"><span data-stu-id="c5322-134">Setting an Output Type for a WMA Encoder</span></span>](configuring-a-wma-encoder.md)          | <span data-ttu-id="c5322-135">說明如何設定 Windows Media 音訊 (WMA) 編碼器的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="c5322-135">Explains how to set an output type on a Windows Media Audio (WMA) encoder.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="c5322-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5322-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5322-137">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="c5322-137">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



