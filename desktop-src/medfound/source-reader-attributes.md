---
description: 來源讀取器屬性
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: 來源讀取器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f425710139b2aebf23ff13a2593ba6931c78fe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691608"
---
# <a name="source-reader-attributes"></a><span data-ttu-id="00892-103">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="00892-103">Source Reader Attributes</span></span>

<span data-ttu-id="00892-104">您可以使用下列屬性來初始化 [來源讀取器](source-reader.md)。</span><span class="sxs-lookup"><span data-stu-id="00892-104">The following attributes can be used to initialize the [Source Reader](source-reader.md).</span></span>



| <span data-ttu-id="00892-105">屬性</span><span class="sxs-lookup"><span data-stu-id="00892-105">Attribute</span></span>                                                                                                            | <span data-ttu-id="00892-106">描述</span><span class="sxs-lookup"><span data-stu-id="00892-106">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00892-107">MF \_ 低 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="00892-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                                               | <span data-ttu-id="00892-108">啟用低延遲處理。</span><span class="sxs-lookup"><span data-stu-id="00892-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="00892-109">MF \_ READWRITE \_ 停用 \_ 轉換器</span><span class="sxs-lookup"><span data-stu-id="00892-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                                            | <span data-ttu-id="00892-110">啟用或停用來源讀取器的格式轉換。</span><span class="sxs-lookup"><span data-stu-id="00892-110">Enables or disables format conversions by the source reader.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="00892-111">MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="00892-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md)                           | <span data-ttu-id="00892-112">可讓來源讀取器使用以硬體為基礎的媒體基礎轉換 (MFTs) 。</span><span class="sxs-lookup"><span data-stu-id="00892-112">Enables the source reader to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                |
| [<span data-ttu-id="00892-113">MF \_ 來源 \_ 讀取器 \_ 非同步 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="00892-113">MF\_SOURCE\_READER\_ASYNC\_CALLBACK</span></span>](mf-source-reader-async-callback.md)                                           | <span data-ttu-id="00892-114">包含應用程式的來源讀取器回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="00892-114">Contains a pointer to the application's callback interface for the source reader.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="00892-115">MF \_ 來源 \_ 讀取器 \_ D3D \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="00892-115">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)                                                 | <span data-ttu-id="00892-116">包含指向 Microsoft [Direct3D 裝置管理員](direct3d-device-manager.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="00892-116">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md).</span></span>                                                                                                                                        |
| [<span data-ttu-id="00892-117">MF \_ 來源 \_ 讀取器 \_ 停用 \_ DXVA</span><span class="sxs-lookup"><span data-stu-id="00892-117">MF\_SOURCE\_READER\_DISABLE\_DXVA</span></span>](mf-source-reader-disable-dxva.md)                                               | <span data-ttu-id="00892-118">指定來源讀取器是否啟用 (DXVA) 影片解碼器的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="00892-118">Specifies whether the source reader enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>                                                                                                                                |
| [<span data-ttu-id="00892-119">MF \_ 來源 \_ 讀取 \_ 器 \_ \_ 在關機時中斷 MEDIASOURCE \_ 連線</span><span class="sxs-lookup"><span data-stu-id="00892-119">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN</span></span>](mf-source-reader-disconnect-mediasource-on-shutdown.md) | <span data-ttu-id="00892-120">指定來源讀取器是否關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="00892-120">Specifies whether the source reader shuts down the media source.</span></span><br/> <span data-ttu-id="00892-121">只有當應用程式從現有的媒體來源物件建立來源讀取器時，才適用。</span><span class="sxs-lookup"><span data-stu-id="00892-121">Applies only when the application creates the source reader from an existing media source object.</span></span><br/>                                           |
| [<span data-ttu-id="00892-122">MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 先進的 \_ 影片 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="00892-122">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING</span></span>](mf-source-reader-enable-advanced-video-processing.md)     | <span data-ttu-id="00892-123">啟用 [來源讀取器](source-reader.md)的先進影片處理，包括色彩空間轉換、去交錯、影片調整大小和畫面播放速率轉換。</span><span class="sxs-lookup"><span data-stu-id="00892-123">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>                                                           |
| [<span data-ttu-id="00892-124">MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 影片 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="00892-124">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING</span></span>](mf-source-reader-enable-video-processing.md)                        | <span data-ttu-id="00892-125">可讓來源讀取器進行有限的影片處理。</span><span class="sxs-lookup"><span data-stu-id="00892-125">Enables limited video processing by the source reader.</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="00892-126">MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ CONFIG</span><span class="sxs-lookup"><span data-stu-id="00892-126">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG</span></span>](mf-source-reader-mediasource-config.md)                                   | <span data-ttu-id="00892-127">包含媒體來源的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="00892-127">Contains configuration properties for the media source.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="00892-128">MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="00892-128">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                                            | <span data-ttu-id="00892-129">包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，用來將具有使用規定限制的 MFT 解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="00892-129">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="00892-130">如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="00892-130">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |



 

<span data-ttu-id="00892-131">使用這些屬性搭配下列方法和函數：</span><span class="sxs-lookup"><span data-stu-id="00892-131">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="00892-132">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span><span class="sxs-lookup"><span data-stu-id="00892-132">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="00892-133">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span><span class="sxs-lookup"><span data-stu-id="00892-133">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="00892-134">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="00892-134">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="00892-135">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="00892-135">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="00892-136">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="00892-136">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="00892-137">若要使用這些屬性的任何一項，請先呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="00892-137">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="00892-138">然後使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，在屬性存放區上設定所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="00892-138">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="00892-139">將 **IMFAttributes** 指標傳遞至先前所列之任何方法或函數的 *pAttributes* 參數。</span><span class="sxs-lookup"><span data-stu-id="00892-139">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00892-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="00892-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00892-141">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="00892-141">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00892-142">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="00892-142">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="00892-143">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="00892-143">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




