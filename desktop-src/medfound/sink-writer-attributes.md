---
description: 接收寫入器屬性
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: 接收寫入器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114353"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="32acd-103">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="32acd-103">Sink Writer Attributes</span></span>

<span data-ttu-id="32acd-104">您可以使用下列屬性來初始化接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="32acd-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="32acd-105">屬性</span><span class="sxs-lookup"><span data-stu-id="32acd-105">Attribute</span></span>                                                                                  | <span data-ttu-id="32acd-106">描述</span><span class="sxs-lookup"><span data-stu-id="32acd-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32acd-107">MF \_ 低 \_ 延遲</span><span class="sxs-lookup"><span data-stu-id="32acd-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="32acd-108">啟用低延遲處理。</span><span class="sxs-lookup"><span data-stu-id="32acd-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="32acd-109">MF \_ READWRITE \_ 停用 \_ 轉換器</span><span class="sxs-lookup"><span data-stu-id="32acd-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="32acd-110">啟用或停用接收寫入器的格式轉換。</span><span class="sxs-lookup"><span data-stu-id="32acd-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="32acd-111">MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="32acd-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="32acd-112">可讓接收寫入器使用以硬體為基礎的媒體基礎轉換 (MFTs) 。</span><span class="sxs-lookup"><span data-stu-id="32acd-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="32acd-113">MF \_ 接收 \_ 寫入器 \_ 非同步 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="32acd-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="32acd-114">包含接收器寫入器的應用程式回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="32acd-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="32acd-115">MF \_ 接收 \_ 寫入器 \_ 停用 \_ 節流</span><span class="sxs-lookup"><span data-stu-id="32acd-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="32acd-116">指定接收寫入器是否限制傳入資料的速率。</span><span class="sxs-lookup"><span data-stu-id="32acd-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="32acd-117">MF \_ 轉碼 \_ CONTAINERTYPE</span><span class="sxs-lookup"><span data-stu-id="32acd-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="32acd-118">指定輸出檔的容器類型。</span><span class="sxs-lookup"><span data-stu-id="32acd-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="32acd-119">MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="32acd-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="32acd-120">包含 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 指標，用來將具有使用規定限制的 MFT 解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="32acd-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="32acd-121">如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="32acd-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="32acd-122">MF \_ 接收 \_ 寫入器 \_ D3D \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="32acd-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="32acd-123">使用此屬性可為接收寫入器載入的任何影片編碼器或媒體接收器提供 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="32acd-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="32acd-124">使用這些屬性搭配下列方法和函數：</span><span class="sxs-lookup"><span data-stu-id="32acd-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="32acd-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span><span class="sxs-lookup"><span data-stu-id="32acd-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="32acd-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span><span class="sxs-lookup"><span data-stu-id="32acd-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="32acd-127">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="32acd-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="32acd-128">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="32acd-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="32acd-129">若要使用這些屬性的任何一項，請先呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="32acd-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="32acd-130">然後使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，在屬性存放區上設定所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="32acd-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="32acd-131">將 **IMFAttributes** 指標傳遞至先前所列之任何方法或函數的 *pAttributes* 參數。</span><span class="sxs-lookup"><span data-stu-id="32acd-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32acd-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="32acd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32acd-133">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="32acd-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="32acd-134">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="32acd-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



