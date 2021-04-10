---
description: 關於 WM ASF Reader 篩選器
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: 關於 WM ASF Reader 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846631"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="37bc4-103">關於 WM ASF Reader 篩選器</span><span class="sxs-lookup"><span data-stu-id="37bc4-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="37bc4-104">ASF 檔案的播放是由 [WM Asf 讀取](wm-asf-reader-filter.md) 器篩選器所處理。</span><span class="sxs-lookup"><span data-stu-id="37bc4-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="37bc4-105">當 WM ASF 讀取器讀取檔案時，它會自動建立每個資料流程的輸出針腳，包括 web 資料流程、指令碼命令資料流程，以及任何其他類型的任意資料流程。</span><span class="sxs-lookup"><span data-stu-id="37bc4-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="37bc4-106">如果是多位元率檔案，則只會針對目前選取的資料流程建立 pin。</span><span class="sxs-lookup"><span data-stu-id="37bc4-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="37bc4-107">若要使用 WM ASF 讀取器篩選器來播放 ASF 檔案，請呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 或 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)。</span><span class="sxs-lookup"><span data-stu-id="37bc4-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="37bc4-108">WM ASF 讀取器支援 DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面，可讓應用程式在檔案內執行時態搜尋。</span><span class="sxs-lookup"><span data-stu-id="37bc4-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="37bc4-109">但是，不支援以 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) 中所指定的 1.0 (速度來播放。</span><span class="sxs-lookup"><span data-stu-id="37bc4-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="37bc4-110">WM ASF 讀取器篩選器也會公開數個 Windows Media 格式 SDK 介面，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="37bc4-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="37bc4-111">這些介面記載于 Windows Media Format SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="37bc4-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="37bc4-112">介面</span><span class="sxs-lookup"><span data-stu-id="37bc4-112">Interface</span></span>                                             | <span data-ttu-id="37bc4-113">公開的方式</span><span class="sxs-lookup"><span data-stu-id="37bc4-113">How exposed</span></span>                                 | <span data-ttu-id="37bc4-114">註解</span><span class="sxs-lookup"><span data-stu-id="37bc4-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37bc4-115">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="37bc4-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="37bc4-116">透過篩選器上的 **IServiceProvider** 。</span><span class="sxs-lookup"><span data-stu-id="37bc4-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="37bc4-117">針對需要播放由數位 Rights Management (DRM) 所保護之內容的應用程式提供。</span><span class="sxs-lookup"><span data-stu-id="37bc4-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="37bc4-118">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="37bc4-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="37bc4-119">篩選上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="37bc4-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="37bc4-120">提供讓應用程式可以讀取檔案和內容屬性，以及標記和腳本資訊和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="37bc4-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="37bc4-121">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="37bc4-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="37bc4-122">篩選上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="37bc4-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="37bc4-123">部分實作為篩選準則，讓應用程式可以存取 WM 讀取器物件上的資訊方法。</span><span class="sxs-lookup"><span data-stu-id="37bc4-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="37bc4-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="37bc4-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="37bc4-125">篩選上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="37bc4-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="37bc4-126">部分實作為篩選器，讓應用程式可以存取格式 SDK 讀取器物件上的參考方法。</span><span class="sxs-lookup"><span data-stu-id="37bc4-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="37bc4-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="37bc4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37bc4-128">在 DirectShow 中讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="37bc4-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



