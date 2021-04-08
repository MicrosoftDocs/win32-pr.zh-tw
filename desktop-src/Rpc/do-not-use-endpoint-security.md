---
title: 請勿使用端點安全性
description: 端點安全性是一種安全性模型，在使用 RPC 函式的 RpcServerUseProtseq \ 群組建立端點時，會提供安全描述項。
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672840"
---
# <a name="do-not-use-endpoint-security"></a><span data-ttu-id="525ae-103">請勿使用端點安全性</span><span class="sxs-lookup"><span data-stu-id="525ae-103">Do Not Use Endpoint Security</span></span>

<span data-ttu-id="525ae-104">端點安全性是一種安全性模型，在使用 RPC 函式的 [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)群組建立端點時，會提供安全描述項 \* 。</span><span class="sxs-lookup"><span data-stu-id="525ae-104">Endpoint security is a security model in which a security descriptor is given when an endpoint is created with the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* group of RPC functions.</span></span> <span data-ttu-id="525ae-105">請勿使用此安全性模型。</span><span class="sxs-lookup"><span data-stu-id="525ae-105">Do not use this security model.</span></span> <span data-ttu-id="525ae-106">請勿將安全描述項提供給這些函式。</span><span class="sxs-lookup"><span data-stu-id="525ae-106">Do not give security descriptors to those functions.</span></span> <span data-ttu-id="525ae-107">最棒的是，此方法會浪費 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="525ae-107">At best, this method is a waste of CPU resources.</span></span> <span data-ttu-id="525ae-108">最糟的是，在許多環境中，您可以規避安全描述項，因為在相同的進程區段中執行的 [其他 RPC 端點](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) 」舉例說明。</span><span class="sxs-lookup"><span data-stu-id="525ae-108">At worst, in many environments it is possible to circumvent the security descriptor, as the [Be Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) section exemplifies.</span></span>

<span data-ttu-id="525ae-109">端點安全性僅為了回溯相容性而存在。</span><span class="sxs-lookup"><span data-stu-id="525ae-109">Endpoint security exists only for backward compatibility.</span></span>

 

 




