---
title: RPC 和網路
description: 本節討論如何在使用 RPC 時處理網路程度，並說明 RPC 層級 Api 如何轉譯成網路活動。 區段只會參考 ncacn 的 \_ ip \_ tcp 和 ncacn \_ HTTP 通訊協定序列。
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- 遠端程序呼叫 RPC、最佳作法、RPC 和網路
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093055"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="3445d-105">RPC 和網路</span><span class="sxs-lookup"><span data-stu-id="3445d-105">RPC and the Network</span></span>

<span data-ttu-id="3445d-106">本節討論如何在使用 RPC 時處理網路程度，並說明 RPC 層級 Api 如何轉譯成網路活動。</span><span class="sxs-lookup"><span data-stu-id="3445d-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="3445d-107">區段只會參考 ncacn 的 [**\_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp) 和 [**ncacn \_ HTTP**](/windows/desktop/Midl/ncacn-http) 通訊協定序列。</span><span class="sxs-lookup"><span data-stu-id="3445d-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="3445d-108">本節分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="3445d-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="3445d-109">在網路中開發與部署</span><span class="sxs-lookup"><span data-stu-id="3445d-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="3445d-110">防止 Client-Side 停止回應</span><span class="sxs-lookup"><span data-stu-id="3445d-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="3445d-111">管理 (關聯) 的網路連接集 </span><span class="sxs-lookup"><span data-stu-id="3445d-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="3445d-112">閒置連接清除</span><span class="sxs-lookup"><span data-stu-id="3445d-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="3445d-113">處理連接中斷</span><span class="sxs-lookup"><span data-stu-id="3445d-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="3445d-114">伺服器端清除</span><span class="sxs-lookup"><span data-stu-id="3445d-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 