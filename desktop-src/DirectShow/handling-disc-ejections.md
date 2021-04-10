---
description: 處理光碟 Ejections
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: 處理光碟 Ejections
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845700"
---
# <a name="handling-disc-ejections"></a><span data-ttu-id="c39fe-103">處理光碟 Ejections</span><span class="sxs-lookup"><span data-stu-id="c39fe-103">Handling Disc Ejections</span></span>

<span data-ttu-id="c39fe-104">當使用者從磁片磁碟機中取出 DVD 時，DVD 瀏覽器會將您的應用程式傳送給您的應用程式，以顯示 EC \_ DVD \_ 光碟 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c39fe-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="c39fe-105">應用程式可以放心地忽略此訊息，讓 DVD 導覽器管理圖形的狀態。</span><span class="sxs-lookup"><span data-stu-id="c39fe-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="c39fe-106">應用程式也可以處理 EC \_ DVD \_ 光碟取出的 \_ 方法，以在彈出光碟時執行自訂行為。</span><span class="sxs-lookup"><span data-stu-id="c39fe-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="c39fe-107">如果您處理訊息，則必須 \_ 使用 [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)方法將 DVD ResetOnStop 旗標設定為 **TRUE** ，然後在關閉應用程式或播放其他光碟之前呼叫 [**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) 。</span><span class="sxs-lookup"><span data-stu-id="c39fe-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c39fe-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="c39fe-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c39fe-109">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="c39fe-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



