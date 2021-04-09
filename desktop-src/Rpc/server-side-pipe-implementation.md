---
title: Server-Side 管道執行
description: 使用管道的分散式應用程式的伺服器程式不需要執行任何發送、提取或配置函式。
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021706"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="98700-103">Server-Side 管道執行</span><span class="sxs-lookup"><span data-stu-id="98700-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="98700-104">使用管道的分散式應用程式的伺服器程式不需要執行任何發送、提取或配置函式。</span><span class="sxs-lookup"><span data-stu-id="98700-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="98700-105">他們必須包含用戶端可以從遠端叫用的程式，以起始資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="98700-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="98700-106">在下列主題中，本節會說明如何執行伺服器的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="98700-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="98700-107">在伺服器上執行輸入管道</span><span class="sxs-lookup"><span data-stu-id="98700-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="98700-108">在伺服器上執行輸出管道</span><span class="sxs-lookup"><span data-stu-id="98700-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




