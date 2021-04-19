---
title: 不使用磁碟儲存體來捕捉
description: 不使用磁碟儲存體來捕捉
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE 訊息
- capCaptureSequenceNoFile 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984502"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="5433f-105">不使用磁碟儲存體來捕捉</span><span class="sxs-lookup"><span data-stu-id="5433f-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="5433f-106">您可以使用 [ [**WM \_ CAP \_ 序列 \_ NOFILE**](wm-cap-sequence-nofile.md) 訊息 (或 [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) 宏) ，在不將資料寫入磁片檔案的情況下使用 capture service。</span><span class="sxs-lookup"><span data-stu-id="5433f-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="5433f-107">此訊息只適用于搭配可讓您的應用程式直接使用影片和音訊資料的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="5433f-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="5433f-108">例如，視訊會議應用程式可能會使用這個訊息來取得串流的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="5433f-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="5433f-109">回呼函式會將已捕獲的映射傳送至遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="5433f-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




