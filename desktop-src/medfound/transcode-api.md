---
description: 本節說明如何使用轉碼 API 來重新編碼媒體檔案。 轉碼 API 是在 Windows 7 中引進的。
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: 轉碼 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848703"
---
# <a name="transcode-api"></a><span data-ttu-id="7dce8-104">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="7dce8-104">Transcode API</span></span>

<span data-ttu-id="7dce8-105">本節說明如何使用轉碼 API 來重新編碼媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="7dce8-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="7dce8-106">轉碼 API 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="7dce8-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="7dce8-107">*轉碼* 是將數位媒體檔案從一種格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="7dce8-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="7dce8-108">轉碼 API 是設計來搭配 [媒體會話](media-session.md)使用。</span><span class="sxs-lookup"><span data-stu-id="7dce8-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="7dce8-109">它簡化了某些轉碼應用程式類型的媒體會話使用：</span><span class="sxs-lookup"><span data-stu-id="7dce8-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="7dce8-110">固定位元速率 (CBR) 編碼方式，這是預先知道的目標位速率。</span><span class="sxs-lookup"><span data-stu-id="7dce8-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="7dce8-111">最多一個音訊串流和一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="7dce8-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="7dce8-112">從檔案和檔案進行編碼。</span><span class="sxs-lookup"><span data-stu-id="7dce8-112">Encoding from and to a file.</span></span>

<span data-ttu-id="7dce8-113">轉碼 API 不支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="7dce8-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="7dce8-114">變數位元速率 (VBR) 或多重傳遞編碼。</span><span class="sxs-lookup"><span data-stu-id="7dce8-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="7dce8-115">多個音訊串流或多個影片串流。</span><span class="sxs-lookup"><span data-stu-id="7dce8-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="7dce8-116">受 DRM 保護的內容，而不是以 WMDRM 保護的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="7dce8-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="7dce8-117">即時串流，例如即時至檔案串流或即時串流。</span><span class="sxs-lookup"><span data-stu-id="7dce8-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="7dce8-118">如果您的編碼應用程式符合這些條件約束，轉碼 API 會比單獨使用媒體會話更簡單的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="7dce8-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7dce8-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="7dce8-119">In this section</span></span>



| <span data-ttu-id="7dce8-120">主題</span><span class="sxs-lookup"><span data-stu-id="7dce8-120">Topic</span></span>                                                                                          | <span data-ttu-id="7dce8-121">描述</span><span class="sxs-lookup"><span data-stu-id="7dce8-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7dce8-122">關於轉碼 API</span><span class="sxs-lookup"><span data-stu-id="7dce8-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="7dce8-123">提供轉碼 API 的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="7dce8-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="7dce8-124">使用轉碼 API</span><span class="sxs-lookup"><span data-stu-id="7dce8-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="7dce8-125">描述應用程式如何使用轉碼 API。</span><span class="sxs-lookup"><span data-stu-id="7dce8-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="7dce8-126">教學課程：編碼的檔</span><span class="sxs-lookup"><span data-stu-id="7dce8-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="7dce8-127">說明如何使用轉碼 API 來編碼數量檔案的逐步教學課程。</span><span class="sxs-lookup"><span data-stu-id="7dce8-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="7dce8-128">教學課程：編碼 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="7dce8-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="7dce8-129">示範如何使用轉碼 API 將 WMA 檔案編碼。</span><span class="sxs-lookup"><span data-stu-id="7dce8-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="7dce8-130">本教學課程會修改教學課程中所顯示的 [程式碼：編碼的檔](tutorial--encoding-an-mp4-file-.md)，因此您應該先閱讀該教學課程。</span><span class="sxs-lookup"><span data-stu-id="7dce8-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7dce8-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dce8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dce8-132">編碼與檔案編寫</span><span class="sxs-lookup"><span data-stu-id="7dce8-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="7dce8-133">媒體基礎：基本概念</span><span class="sxs-lookup"><span data-stu-id="7dce8-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="7dce8-134">媒體基礎中的編碼總覽</span><span class="sxs-lookup"><span data-stu-id="7dce8-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




