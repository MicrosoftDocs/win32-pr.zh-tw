---
title: 新增資訊區塊
description: 新增資訊區塊
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183649"
---
# <a name="adding-an-information-chunk"></a><span data-ttu-id="cbf7f-104">新增資訊區塊</span><span class="sxs-lookup"><span data-stu-id="cbf7f-104">Adding an Information Chunk</span></span>

<span data-ttu-id="cbf7f-105">如果您的應用程式除了音訊和影片之外，還需要包含其他資訊，您可以建立資訊區塊，並將其插入至 capture 檔。</span><span class="sxs-lookup"><span data-stu-id="cbf7f-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="cbf7f-106">資訊區塊可以包含數種類型的資訊，包括著作權聲明的詳細資料、影片來源的識別，或外部時間資訊。</span><span class="sxs-lookup"><span data-stu-id="cbf7f-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="cbf7f-107">下列範例會在資訊區塊中儲存一個 SMPTE (社會（運動圖片和電視工程師）) 時間碼的外部時間資訊，並使用 [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) 宏將區塊新增至 capture 檔案。</span><span class="sxs-lookup"><span data-stu-id="cbf7f-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a><span data-ttu-id="cbf7f-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbf7f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbf7f-109">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="cbf7f-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




