---
description: 具現化編碼器 MFT
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: 具現化編碼器 MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193776"
---
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="e5852-103">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="e5852-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="e5852-104">在 Microsoft 媒體基礎中，編碼器會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 。</span><span class="sxs-lookup"><span data-stu-id="e5852-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="e5852-105">建立編碼器之前，您必須先找出最適合您需求的編碼器。</span><span class="sxs-lookup"><span data-stu-id="e5852-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="e5852-106">Windows Media 音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="e5852-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="e5852-107">類別： **MFT \_ 類別 \_ 音訊 \_ 編碼器**</span><span class="sxs-lookup"><span data-stu-id="e5852-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="e5852-108">主要類型： MFMediaType \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="e5852-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="e5852-109">子類型： MFAudioFormat \_ WMAudioV9、MFAudioFormat \_ WMAudioV8、MFAudioFormat \_ WMAudio \_ 無損、MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="e5852-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="e5852-110">Windows Media video 編解碼器</span><span class="sxs-lookup"><span data-stu-id="e5852-110">Windows Media video codecs</span></span>

    <span data-ttu-id="e5852-111">類別： **MFT \_ 類別 \_ 影片 \_ 編碼器**</span><span class="sxs-lookup"><span data-stu-id="e5852-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="e5852-112">主要類型： MFMediaType \_ 影片</span><span class="sxs-lookup"><span data-stu-id="e5852-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="e5852-113">子類型： MFVideoFormat \_ WVC1、MFVideoFormat \_ WMV3、MFVideoFormat \_ WMV2、MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="e5852-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="e5852-114">媒體基礎提供數個函式，可讓您的應用程式呼叫以列舉系統中可用的各種編碼器。</span><span class="sxs-lookup"><span data-stu-id="e5852-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="e5852-115">編碼器會註冊為 COM 物件，且登錄專案會遵循 COM class factory 的標準格式。</span><span class="sxs-lookup"><span data-stu-id="e5852-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="e5852-116">登錄會維護編碼器的 Clsid，以媒體格式 (音訊或影片) 分類。</span><span class="sxs-lookup"><span data-stu-id="e5852-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="e5852-117">Windows Media 編碼器的類別識別碼會定義為 wmcodecdsp .h 標頭檔中的常數。</span><span class="sxs-lookup"><span data-stu-id="e5852-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="e5852-118">在媒體基礎中，您可以藉由指定分類、支援的輸入類型和支援的輸出類型，透過呼叫 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) 或 [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) 來註冊編碼器。</span><span class="sxs-lookup"><span data-stu-id="e5852-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="e5852-119">成功註冊這些函式時，媒體基礎的列舉函數會考慮 MFTs。</span><span class="sxs-lookup"><span data-stu-id="e5852-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="e5852-120">若要建立編碼器 MFT 的實例，應用程式具有下列選項。</span><span class="sxs-lookup"><span data-stu-id="e5852-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="e5852-121">直接建立編碼器 MFT，並接收指向 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e5852-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="e5852-122">如需詳細資訊，請參閱 [使用 CoCreateInstance 建立編碼器](using-an-encoder-s-imftransform--interface.md)。</span><span class="sxs-lookup"><span data-stu-id="e5852-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="e5852-123">為編碼器 MFT 建立啟用物件的實例，並接收 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e5852-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="e5852-124">如需詳細資訊，請參閱 [使用編碼器的啟用物件](using-an-encoder-s-activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e5852-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="e5852-125">如果您的應用程式使用 [管線層 ASF 元件](pipeline-layer-asf-components.md) 將檔案編碼為 ASF 格式，您必須將編碼器 MFT 插入管線中作為轉換節點。</span><span class="sxs-lookup"><span data-stu-id="e5852-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="e5852-126">在編碼拓撲中建立轉換節點時，您可以將物件類型設定為 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面或 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e5852-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="e5852-127">媒體基礎提供 Windows Media 編碼器的啟始物件，以便方便設定為編碼拓撲中的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="e5852-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="e5852-128">當拓撲解決之後，媒體會話會使用啟用物件來建立編碼器 MFT 的實例。</span><span class="sxs-lookup"><span data-stu-id="e5852-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5852-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5852-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5852-130">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="e5852-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



