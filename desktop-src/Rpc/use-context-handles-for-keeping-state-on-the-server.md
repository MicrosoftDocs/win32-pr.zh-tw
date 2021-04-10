---
title: 使用內容控制碼在伺服器上保持狀態
description: 使用內容控制碼在伺服器上保持狀態
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183564"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="76b1d-103">使用內容控制碼在伺服器上保持狀態</span><span class="sxs-lookup"><span data-stu-id="76b1d-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="76b1d-104">**最佳做法：** 每當呼叫之間的狀態保留在伺服器上時，請使用內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="76b1d-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="76b1d-105">內容控制碼通常是針對新的 RPC 程式設計人員所很嚇人，而學習內容控制碼的額外負荷可能不會一開始就需要投入時間。</span><span class="sxs-lookup"><span data-stu-id="76b1d-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="76b1d-106">這是因為內容控制碼有內建的解決方案，可用於網路程式設計中遇到的許多常見陷阱，否則就必須從頭開始執行。</span><span class="sxs-lookup"><span data-stu-id="76b1d-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="76b1d-107">瞭解內容控點會在稍後支付紅利。</span><span class="sxs-lookup"><span data-stu-id="76b1d-107">Understanding context handles pays dividends later.</span></span>

 

 




