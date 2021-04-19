---
description: 描述如何在使用 Windows Media 編碼器時新增資料單位延伸模組。
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: '使用資料單位延伸模組 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981456"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a><span data-ttu-id="587d1-103">使用資料單位延伸模組 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="587d1-103">Using Data Unit Extensions (Microsoft Media Foundation)</span></span>

<span data-ttu-id="587d1-104">Windows Media 音訊和影片編解碼器是設計來搭配 Advanced Systems Format (ASF) 容器使用。</span><span class="sxs-lookup"><span data-stu-id="587d1-104">The Windows Media Audio and Video codecs are designed to work well with the Advanced Systems Format (ASF) container.</span></span> <span data-ttu-id="587d1-105">ASF 是用來 Windows Media 音訊 (WMA) 檔案和 Windows Media 視訊 (WMV) 檔的結構化格式。</span><span class="sxs-lookup"><span data-stu-id="587d1-105">ASF is the structured format used for Windows Media Audio (WMA) files and Windows Media Video (WMV) files.</span></span> <span data-ttu-id="587d1-106">它是針對串流資料而設計的可擴充格式。</span><span class="sxs-lookup"><span data-stu-id="587d1-106">It is an extensible format designed for streaming data.</span></span> <span data-ttu-id="587d1-107">ASF 結構的其中一個不尋常特性是能夠將中繼資料附加至個別範例，並將該資料與位資料流程中的範例一起內嵌。</span><span class="sxs-lookup"><span data-stu-id="587d1-107">One of the unusual characteristics of the ASF structure is the ability to attach metadata to individual samples, and to embed that data with the samples in the bit stream.</span></span> <span data-ttu-id="587d1-108">以這種方式儲存的中繼資料專案稱為資料 *單位延伸* 模組或 *範例延伸* 模組。</span><span class="sxs-lookup"><span data-stu-id="587d1-108">An item of metadata stored in this way is called a data *unit extension*, or *sample extension*.</span></span>

<span data-ttu-id="587d1-109">資料單位延伸可以包含編碼器、解碼器或播放程式應用程式所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="587d1-109">A data unit extension can contain information that is required by the encoder, the decoder, or the player application.</span></span> <span data-ttu-id="587d1-110">Windows Media 9 系列編解碼器中所執行的大部分資料單位延伸模組類型，都包含用於解碼和轉譯媒體的應用程式所適用的資料。</span><span class="sxs-lookup"><span data-stu-id="587d1-110">Most of the data-unit-extension types that are implemented in the Windows Media 9 Series of codecs contain data intended for the application that decodes and renders the media.</span></span> <span data-ttu-id="587d1-111">例如，您可以藉由將它新增為數據單位延伸，來維護來源資料的 SMPTE 時間代碼。</span><span class="sxs-lookup"><span data-stu-id="587d1-111">For example, you can maintain SMPTE time codes from source data by adding them as data unit extensions.</span></span> <span data-ttu-id="587d1-112">但是，下列編解碼器功能需要資料單位延伸：</span><span class="sxs-lookup"><span data-stu-id="587d1-112">However, the following codec features require data unit extensions:</span></span>

-   [<span data-ttu-id="587d1-113">強制插入主要畫面格</span><span class="sxs-lookup"><span data-stu-id="587d1-113">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)
-   [<span data-ttu-id="587d1-114">交錯式影片編碼</span><span class="sxs-lookup"><span data-stu-id="587d1-114">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)
-   <span data-ttu-id="587d1-115">直接存取編解碼器時使用資料單位延伸的困難之處，就是物件接收延伸資料的機制。</span><span class="sxs-lookup"><span data-stu-id="587d1-115">The difficulty in using data unit extensions when accessing the codec directly is the mechanism by which the object receives the extension data.</span></span> <span data-ttu-id="587d1-116">這是由 Windows Media Format SDK 的物件使用設計來支援此功能的緩衝區物件來達成。</span><span class="sxs-lookup"><span data-stu-id="587d1-116">This is achieved by the objects of the Windows Media Format SDK by using buffer objects designed to support this feature.</span></span> <span data-ttu-id="587d1-117">建議您使用 Windows Media Format SDK 來啟用需要資料單位延伸的編解碼器功能，但您可以將這些功能與獨立的編解碼器物件搭配使用。</span><span class="sxs-lookup"><span data-stu-id="587d1-117">It is recommended that you use the Windows Media Format SDK to activate the codec features that require data unit extensions, but you can make these features work with the standalone codec objects.</span></span>

## <a name="passing-extended-samples-to-the-codec-objects"></a><span data-ttu-id="587d1-118">將延伸範例傳遞給編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="587d1-118">Passing Extended Samples to the Codec Objects</span></span>

<span data-ttu-id="587d1-119">Windows Media 格式 SDK 會使用公開 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) 介面的緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="587d1-119">The Windows Media Format SDK uses buffer objects that expose [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interfaces.</span></span> <span data-ttu-id="587d1-120">最新的介面為 [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4)。</span><span class="sxs-lookup"><span data-stu-id="587d1-120">The latest interface is [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4).</span></span> <span data-ttu-id="587d1-121">若要使用資料單位延伸將範例傳遞給編解碼器物件，您必須使用可實 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 或 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面和 **INSSBuffer** 介面的緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="587d1-121">To pass samples to a codec object with data unit extensions, you must use a buffer object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) or [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface and the **INSSBuffer** interface.</span></span> <span data-ttu-id="587d1-122">您可以使用 Windows Media Format SDK 或 Microsoft 媒體基礎所建立的緩衝區物件來完成這項工作，或者您可以自行建立符合需求的緩衝區類別。</span><span class="sxs-lookup"><span data-stu-id="587d1-122">You can use buffer objects created by the Windows Media Format SDK or Microsoft Media Foundation to accomplish this, or you can make your own buffer class that meets the requirements.</span></span> <span data-ttu-id="587d1-123">若要建立您自己的緩衝區類別，您必須符合 **INSSBuffer** 介面的方法原型。</span><span class="sxs-lookup"><span data-stu-id="587d1-123">To create your own buffer class, you must conform to the method prototypes for the **INSSBuffer** interfaces.</span></span> <span data-ttu-id="587d1-124">這些介面定義可以在隨 Windows Media Format SDK 安裝的 wmsbuffer .h 標頭檔中找到。</span><span class="sxs-lookup"><span data-stu-id="587d1-124">These interface definitions can be found in the wmsbuffer.h header file that is installed with the Windows Media Format SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="587d1-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="587d1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="587d1-126">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="587d1-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
