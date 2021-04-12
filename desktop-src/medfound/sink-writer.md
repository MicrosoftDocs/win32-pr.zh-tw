---
description: 接收寫入器是編碼音訊或影片檔案的元件。
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: 接收寫入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318731"
---
# <a name="sink-writer"></a><span data-ttu-id="4df3f-103">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="4df3f-103">Sink Writer</span></span>

<span data-ttu-id="4df3f-104">接收寫入器是編碼音訊或影片檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="4df3f-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="4df3f-105">下圖顯示概要說明應用程式如何使用接收寫入器來編碼和音訊/影片檔案。</span><span class="sxs-lookup"><span data-stu-id="4df3f-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![顯示接收寫入器的圖表。](images/encoding09.png)

<span data-ttu-id="4df3f-107">接收寫入器會裝載媒體接收，以及選擇性地裝載一或多個編碼器。</span><span class="sxs-lookup"><span data-stu-id="4df3f-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="4df3f-108">編碼器會將未壓縮的音訊或影片資料轉換成編碼 bitstreams。</span><span class="sxs-lookup"><span data-stu-id="4df3f-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="4df3f-109">媒體接收器會將 bitstreams 輸出至檔案。</span><span class="sxs-lookup"><span data-stu-id="4df3f-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="4df3f-110">接收寫入器會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="4df3f-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="4df3f-111">載入媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="4df3f-111">Loads the media sink.</span></span>
-   <span data-ttu-id="4df3f-112">尋找並載入編碼器。</span><span class="sxs-lookup"><span data-stu-id="4df3f-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="4df3f-113">管理編碼器和媒體接收器的資料流程。</span><span class="sxs-lookup"><span data-stu-id="4df3f-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="4df3f-114">應用程式會將音訊/影片資料傳遞給接收寫入器作為輸入。</span><span class="sxs-lookup"><span data-stu-id="4df3f-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="4df3f-115">應用程式如何取得或產生輸入資料並不重要。</span><span class="sxs-lookup"><span data-stu-id="4df3f-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="4df3f-116">其中一個選項是使用 [來源讀取器](source-reader.md)，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="4df3f-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="4df3f-117">不過，接收寫入器不需要使用來源讀取器。</span><span class="sxs-lookup"><span data-stu-id="4df3f-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="4df3f-118">這兩個元件是獨立的。</span><span class="sxs-lookup"><span data-stu-id="4df3f-118">These two components are independent.</span></span>

![顯示來源讀取器和接收寫入器的圖表。](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="4df3f-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="4df3f-120">In this section</span></span>

-   [<span data-ttu-id="4df3f-121">使用接收寫入器</span><span class="sxs-lookup"><span data-stu-id="4df3f-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="4df3f-122">教學課程：使用接收寫入器編碼影片</span><span class="sxs-lookup"><span data-stu-id="4df3f-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="4df3f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="4df3f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4df3f-124">編碼與檔案編寫</span><span class="sxs-lookup"><span data-stu-id="4df3f-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="4df3f-125">媒體基礎中的編碼總覽</span><span class="sxs-lookup"><span data-stu-id="4df3f-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



