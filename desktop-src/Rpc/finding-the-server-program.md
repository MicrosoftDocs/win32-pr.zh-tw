---
title: 尋找伺服器程式
description: 在用戶端 RPC 執行時間連接到系結控制碼所要求的伺服器主機系統之後，用戶端 RPC 執行時間程式庫會尋找伺服器進程。
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- 遠端程序呼叫 RPC、工作、尋找伺服器程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967205"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="8eaf3-104">尋找伺服器程式</span><span class="sxs-lookup"><span data-stu-id="8eaf3-104">Finding the Server Program</span></span>

<span data-ttu-id="8eaf3-105">在用戶端 RPC 執行時間連接到系結控制碼所要求的伺服器主機系統之後，用戶端 RPC 執行時間程式庫會尋找伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="8eaf3-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="8eaf3-106">若要這樣做，它會查詢伺服器主機系統上的端點對應。</span><span class="sxs-lookup"><span data-stu-id="8eaf3-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="8eaf3-107">端點對應包含伺服器正在接聽之端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8eaf3-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




