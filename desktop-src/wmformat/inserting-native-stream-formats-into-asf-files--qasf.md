---
title: '將原生串流格式插入到 ASF 檔案 (QASF) '
description: '將原生串流格式插入到 ASF 檔案 (QASF) '
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- 'Windows Media Format SDK、原生串流格式 (QASF) '
- 'Windows Media Format SDK，將原生串流格式插入到 ASF 檔案 (QASF) '
- Windows Media Format SDK、DirectShow
- 'Advanced Systems Format (ASF) ， (QASF 插入原生串流格式) '
- 'ASF (Advanced Systems Format) ， (QASF 插入原生串流格式) '
- 'Advanced Systems Format (ASF) 、原生串流格式 (QASF) '
- 'ASF (Advanced Systems Format) ，原生串流格式 (QASF) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow、原生串流格式 (QASF) '
- 'DirectShow，將原生串流格式插入到 ASF 檔案 (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840576"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="dcfc0-118">將原生串流格式插入到 ASF 檔案 (QASF) </span><span class="sxs-lookup"><span data-stu-id="dcfc0-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="dcfc0-119">根據預設， [WM ASF 寫入器](wm-asf-writer-filter.md) 預期會在其輸入 pin 上使用未壓縮的音訊和影片串流，並且會使用 Windows MEDIA 格式 SDK 來存取 Windows Media 音訊，並 Windows Media 視訊可壓縮資料流程的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="dcfc0-120">但是 ASF 檔案容器可以用於任何類型的資料。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="dcfc0-121">藉由將數位媒體資料放入 ASF 檔案容器中，您可以新增 ASF 提供的功能，例如中繼資料和數位版權管理 (DRM) ，而不需要轉碼您的內容。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="dcfc0-122">若要建立包含非以 Windows Media 為基礎之內容的 ASF 檔案，應用程式必須在 WM ASF 寫入器的篩選圖形上游中壓縮資料流程，然後藉由呼叫 [**IConfigAsfWriter2：： SetParam**](iconfigasfwriter2-setparam.md) 來略過 Wm Asf 寫入器的壓縮機制，如下所示：</span><span class="sxs-lookup"><span data-stu-id="dcfc0-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="dcfc0-123">然後使用所需的設定檔來設定篩選。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="dcfc0-124">輸入資料流程的媒體類型必須完全符合設定檔中的格式。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="dcfc0-125">在某些情況下，您可能需要檢查輸入資料流程的格式，並建立自訂設定檔以符合此格式。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="dcfc0-126">如需詳細資訊，請參閱 [使用協力廠商編解碼器建立 ASF](to-create-asf-files-using-third-party-codecs.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="dcfc0-127">當您將 WM ASF 寫入器連線到上游篩選器時，請使用 **IGraphBuilder：： ConnectDirect** 方法。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="dcfc0-128">請勿使用任何 "智慧型 connect" 方法（例如 **IGraphBuilder：： connect** 或 **IGraphBuilder：： RenderFile** ）來連接篩選，因為這樣會停用篩選準則的「略過壓縮」模式。</span><span class="sxs-lookup"><span data-stu-id="dcfc0-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




