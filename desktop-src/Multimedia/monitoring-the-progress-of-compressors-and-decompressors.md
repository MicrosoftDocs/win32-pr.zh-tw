---
title: 監視壓縮機和 Decompressors 的進度
description: 監視壓縮機和 Decompressors 的進度
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，監視
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，監視
- ICSetStatusProc 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965590"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a><span data-ttu-id="cd548-106">監視壓縮機和 Decompressors 的進度</span><span class="sxs-lookup"><span data-stu-id="cd548-106">Monitoring the Progress of Compressors and Decompressors</span></span>

<span data-ttu-id="cd548-107">您的應用程式可以藉由傳送回呼函式的位址，來監視壓縮程式或解壓縮程式所執行的冗長作業進度。</span><span class="sxs-lookup"><span data-stu-id="cd548-107">Your application can monitor the progress of a lengthy operation performed by a compressor or decompressor by sending it the address of a callback function.</span></span> <span data-ttu-id="cd548-108">您可以使用 [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) 函數將位址傳送到壓縮或解壓縮。</span><span class="sxs-lookup"><span data-stu-id="cd548-108">You can use the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function to send the address to the compressor or decompressor.</span></span> <span data-ttu-id="cd548-109">當壓縮或解壓縮接收到此位址時，會將狀態訊息傳送至函式。</span><span class="sxs-lookup"><span data-stu-id="cd548-109">When the compressor or decompressor receives this address, it sends status messages to the function.</span></span> <span data-ttu-id="cd548-110">這些訊息會指出作業是否正在啟動、停止、產生或繼續。</span><span class="sxs-lookup"><span data-stu-id="cd548-110">These messages indicate whether the operation is starting, stopping, yielding, or proceeding.</span></span>

 

 




