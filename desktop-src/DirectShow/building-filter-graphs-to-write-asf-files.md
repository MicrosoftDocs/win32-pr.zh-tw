---
description: 建立篩選圖形來寫入 ASF 檔案
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: 建立篩選圖形來寫入 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467829"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="d3dc8-103">建立篩選圖形來寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="d3dc8-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="d3dc8-104">建立以 Windows Media 為基礎的內容時，應用程式通常會使用下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="d3dc8-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="d3dc8-105">將內容從其他格式轉換或轉碼成 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="d3dc8-106">將非 Windows Media 架構 (原生串流格式的內容，) 到 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="d3dc8-107">捕獲即時資料，並立即將其編碼為 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="d3dc8-108">轉碼 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="d3dc8-108">Transcoding ASF Files</span></span>

<span data-ttu-id="d3dc8-109">您可以透過各種方式使用 [WM ASF 寫入器](wm-asf-writer-filter.md) 來建立檔案轉碼篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="d3dc8-110">最簡單的方式是將 WM ASF 寫入器新增至篩選圖形，然後使用 IGraphBuilder：： RenderFile 方法自動建立圖形。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="d3dc8-111">另一種方式是將每個篩選手動新增至圖形並連接釘選。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="d3dc8-112">新增 WM ASF 寫入器之後，如果預設設定檔不適用，請使用 IConfigAsfWriter 方法進行設定，並將 WM ASF 寫入器輸入接點連接到上游篩選器上對應的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="d3dc8-113">下圖顯示典型的 WM ASF 寫入器轉碼篩選圖形設定。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![轉碼篩選圖形](images/asf-transcode.png)

<span data-ttu-id="d3dc8-115">將原生資料流程格式插入至 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="d3dc8-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="d3dc8-116">根據預設，WM ASF 寫入器篩選器預期會在其輸入圖釘上使用未壓縮的音訊和影片串流，並使用 Windows Media 音訊和 Windows Media 視訊編解碼器來壓縮資料流程。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="d3dc8-117">不過，ASF 檔案容器可以用於任何類型的資料。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="d3dc8-118">藉由將數位媒體資料放入 ASF 檔案容器中，您可以新增 ASF 提供的功能，例如中繼資料和數位版權管理 (DRM) ，而不需要轉碼您的內容。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="d3dc8-119">若要建立包含非以 Windows Media 為基礎之內容的 ASF 檔案，應用程式必須在 WM ASF 寫入器的篩選圖形上游中壓縮資料流程，然後藉由呼叫 [**IConfigAsfWriter2：： SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) 來略過 Wm Asf 寫入器的壓縮機制，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d3dc8-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="d3dc8-120">然後使用所需的設定檔來設定篩選。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="d3dc8-121">輸入資料流程的媒體類型必須完全符合設定檔中的格式。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="d3dc8-122">在某些情況下，您可能需要檢查輸入資料流程的格式，並建立自訂設定檔以符合此格式。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="d3dc8-123">當您將 WM ASF 寫入器連線到上游篩選器時，請使用 IGraphBuilder：： ConnectDirect 方法。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="d3dc8-124">請勿使用任何 "智慧型 connect" 方法（例如 IGraphBuilder：： Connect 或 IGraphBuilder：： RenderFile）來連接篩選，因為這樣會停用篩選準則的「略過壓縮」模式。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="d3dc8-125">直接從裝置到 ASF 檔案的捕獲</span><span class="sxs-lookup"><span data-stu-id="d3dc8-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="d3dc8-126">當直接將音訊或影片捕獲到 ASF 檔案時，篩選圖形看起來會如下所示，視所使用的捕獲裝置類型而定。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![windows media 影片捕獲圖形](images/asf-webcam.png)

<span data-ttu-id="d3dc8-128">如需建立影片和音訊捕獲圖形的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="d3dc8-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="d3dc8-129">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="d3dc8-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="d3dc8-130">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="d3dc8-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="d3dc8-131">除非所有的 pin 都已連線，否則不會執行 WM ASF 寫入器。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="d3dc8-132">如果您使用預設系統設定檔來設定 WM ASF 寫入器 (不建議使用) ，或任何包含音訊和影片串流的設定檔，則會為每個串流建立輸入 pin，而且必須連線到每個輸出。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="d3dc8-133">例如，如果您不想要捕獲音訊，請務必使用僅限影片的設定檔來設定篩選，如此就不會建立音訊 pin。</span><span class="sxs-lookup"><span data-stu-id="d3dc8-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3dc8-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3dc8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3dc8-135">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="d3dc8-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



