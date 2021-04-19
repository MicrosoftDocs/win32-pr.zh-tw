---
title: '建立篩選圖形來將 ASF 檔案寫入 (QASF) '
description: '建立篩選圖形來將 ASF 檔案寫入 (QASF) '
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- 'Windows Media 格式 SDK，建立篩選圖形 (QASF) '
- Windows Media Format SDK、DirectShow
- 'Windows Media 格式 SDK， (QASF 寫入 ASF 檔案) '
- 'Advanced Systems Format (ASF) 、建立篩選圖形 (QASF) '
- 'ASF (Advanced Systems Format) ，建立篩選圖形 (QASF) '
- 'Advanced Systems Format (ASF) 、撰寫 (QASF) '
- 'ASF (Advanced Systems Format) 、撰寫 (QASF) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- 'DirectShow，建立篩選圖形 (QASF) '
- 'DirectShow，將 ASF 檔案寫入 (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- DirectShow、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106983277"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="32085-118">建立篩選圖形來將 ASF 檔案寫入 (QASF) </span><span class="sxs-lookup"><span data-stu-id="32085-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="32085-119">根據 DirectShow 的應用程式，在建立 Windows Media 內容時，通常會使用三種基本類型的篩選圖形之一：</span><span class="sxs-lookup"><span data-stu-id="32085-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="32085-120">篩選圖形，可將內容從其他格式轉換或轉碼成 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="32085-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="32085-121">用來將非 Windows Media (原生串流格式) 的內容，插入至 ASF 檔案的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="32085-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="32085-122">在將即時資料儲存至磁片之前，先篩選圖形以立即將其編碼，並立即編碼成 Windows Media 格式。</span><span class="sxs-lookup"><span data-stu-id="32085-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="32085-123">下列各節將詳細說明每一種篩選圖形類型。</span><span class="sxs-lookup"><span data-stu-id="32085-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="32085-124">區段</span><span class="sxs-lookup"><span data-stu-id="32085-124">Section</span></span>                                                                                                             | <span data-ttu-id="32085-125">描述</span><span class="sxs-lookup"><span data-stu-id="32085-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32085-126">轉碼檔案 (QASF) </span><span class="sxs-lookup"><span data-stu-id="32085-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="32085-127">描述如何建立檔轉碼篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="32085-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="32085-128">將原生串流格式插入到 ASF 檔案 (QASF) </span><span class="sxs-lookup"><span data-stu-id="32085-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="32085-129">說明如何將任何類型的壓縮或未壓縮的音訊或影片資料放入 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="32085-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="32085-130">將裝置直接從裝置捕獲到 ASF 檔案 (QASF) </span><span class="sxs-lookup"><span data-stu-id="32085-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="32085-131">描述如何建立輸出至 ASF 檔案的捕獲篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="32085-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




