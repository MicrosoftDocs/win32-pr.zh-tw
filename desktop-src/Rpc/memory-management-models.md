---
title: Memory-Management 模型
description: Memory-Management 模型
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932597"
---
# <a name="memory-management-models"></a><span data-ttu-id="3ee53-103">Memory-Management 模型</span><span class="sxs-lookup"><span data-stu-id="3ee53-103">Memory-Management Models</span></span>

<span data-ttu-id="3ee53-104">如果您是開發人員，則有數個選項可供您選擇如何配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ee53-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="3ee53-105">請考慮包含與指標連接之節點（例如連結清單或樹狀結構）所組成的複雜資料結構。</span><span class="sxs-lookup"><span data-stu-id="3ee53-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="3ee53-106">您可以套用屬性，選取下列其中一個模型：</span><span class="sxs-lookup"><span data-stu-id="3ee53-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="3ee53-107">[依節點的配置和解除](node-by-node-allocation-and-deallocation.md)分配。</span><span class="sxs-lookup"><span data-stu-id="3ee53-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="3ee53-108">[存根配置給整個樹狀結構的單一線性緩衝區](stub-allocated-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="3ee53-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="3ee53-109">伺服器 stub 記憶體管理</span><span class="sxs-lookup"><span data-stu-id="3ee53-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="3ee53-110">[用戶端應用程式配置給整個樹狀結構的單一線性緩衝區](application-allocated-buffer.md)。</span><span class="sxs-lookup"><span data-stu-id="3ee53-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="3ee53-111">[伺服器上的持續性儲存體](persistent-storage-on-the-server.md)。</span><span class="sxs-lookup"><span data-stu-id="3ee53-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




