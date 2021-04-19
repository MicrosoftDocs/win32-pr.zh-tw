---
description: 數位訊號處理器
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: 數位訊號處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981736"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="ef478-103">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="ef478-103">Digital Signal Processors</span></span>

<span data-ttu-id="ef478-104">本節說明 Windows 所提供的數位訊號處理器 (DSP) 物件。</span><span class="sxs-lookup"><span data-stu-id="ef478-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="ef478-105">Microsoft 使用「 *數位訊號處理器* 」一詞來指定一組 COM 物件，這些物件會在未壓縮的音訊和影片資料上執行轉換。</span><span class="sxs-lookup"><span data-stu-id="ef478-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="ef478-106">此 SDK 中所述的 Dsp 會以各種未壓縮的格式轉換音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="ef478-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="ef478-107">Dsp 可以單獨使用，或結合音訊和視頻編解碼器。</span><span class="sxs-lookup"><span data-stu-id="ef478-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="ef478-108">除了語音捕獲 DSP 之外，此處所列的每個 DSP 都有兩個不同但類似的介面。</span><span class="sxs-lookup"><span data-stu-id="ef478-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="ef478-109">介面</span><span class="sxs-lookup"><span data-stu-id="ef478-109">Interface</span></span>                              | <span data-ttu-id="ef478-110">描述</span><span class="sxs-lookup"><span data-stu-id="ef478-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="ef478-111">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="ef478-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="ef478-112">與 Microsoft 媒體基礎相容。</span><span class="sxs-lookup"><span data-stu-id="ef478-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="ef478-113">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="ef478-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="ef478-114">與 DirectShow 相容。</span><span class="sxs-lookup"><span data-stu-id="ef478-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="ef478-115">您可以使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面設定屬性，以設定 dsp。</span><span class="sxs-lookup"><span data-stu-id="ef478-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="ef478-116">某些 Dsp 具有可設定屬性的額外介面。</span><span class="sxs-lookup"><span data-stu-id="ef478-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="ef478-117">若要使用這些介面，請呼叫 DSP 之任何其他介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法。</span><span class="sxs-lookup"><span data-stu-id="ef478-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="ef478-118">每個 DSP 的參考主題都會列出支援的屬性、介面和其他功能。</span><span class="sxs-lookup"><span data-stu-id="ef478-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="ef478-119">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="ef478-119">This section contains the following topics.</span></span>



| <span data-ttu-id="ef478-120">Dsp</span><span class="sxs-lookup"><span data-stu-id="ef478-120">DSP</span></span>                                                      | <span data-ttu-id="ef478-121">Description</span><span class="sxs-lookup"><span data-stu-id="ef478-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="ef478-122">音訊 Resampler DSP</span><span class="sxs-lookup"><span data-stu-id="ef478-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="ef478-123">轉換音訊串流的取樣率。</span><span class="sxs-lookup"><span data-stu-id="ef478-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="ef478-124">色彩控制轉換 DSP</span><span class="sxs-lookup"><span data-stu-id="ef478-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="ef478-125">調整影片資料流程的色彩特性。</span><span class="sxs-lookup"><span data-stu-id="ef478-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="ef478-126">色彩轉換器 DSP</span><span class="sxs-lookup"><span data-stu-id="ef478-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="ef478-127">在色彩格式之間轉換影片串流。</span><span class="sxs-lookup"><span data-stu-id="ef478-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="ef478-128">畫面播放速率轉換器 DSP</span><span class="sxs-lookup"><span data-stu-id="ef478-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="ef478-129">變更影片串流的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="ef478-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="ef478-130">影片尺寸調整 DSP</span><span class="sxs-lookup"><span data-stu-id="ef478-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="ef478-131">調整影片資料流程的大小。</span><span class="sxs-lookup"><span data-stu-id="ef478-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="ef478-132">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ef478-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="ef478-133">封裝與語音捕捉相關的數個 Dsp。</span><span class="sxs-lookup"><span data-stu-id="ef478-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ef478-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef478-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef478-135">媒體基礎程式設計參考</span><span class="sxs-lookup"><span data-stu-id="ef478-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
