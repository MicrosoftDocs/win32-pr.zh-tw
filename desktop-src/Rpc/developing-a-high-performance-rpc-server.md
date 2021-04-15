---
title: 開發高效能 RPC 伺服器
description: 本節中的資訊適用于遠端通訊協定序列 ncacn \_ ip \_ tcp、ncacn \_ HTTP、Ncacn \_ np 以及 WINDOWS 2000 和 windows XP。
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- 遠端程序呼叫 RPC、最佳作法、開發高效能伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463581"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="ab7ad-104">開發高效能 RPC 伺服器</span><span class="sxs-lookup"><span data-stu-id="ab7ad-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="ab7ad-105">本節中的資訊適用于遠端通訊協定序列： [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)、 [**ncacn \_ HTTP**](/windows/desktop/Midl/ncacn-http)、 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)以及 windows 2000 和 windows XP。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="ab7ad-106">本節討論 RPC 伺服器效能的三個主要層面：</span><span class="sxs-lookup"><span data-stu-id="ab7ad-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="ab7ad-107">網路延遲和輸送量</span><span class="sxs-lookup"><span data-stu-id="ab7ad-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="ab7ad-108">延展性</span><span class="sxs-lookup"><span data-stu-id="ab7ad-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="ab7ad-109">其他 RPC 效能秘訣</span><span class="sxs-lookup"><span data-stu-id="ab7ad-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="ab7ad-110">程式碼路徑長度是 RPC 的另一個主要效能考慮。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="ab7ad-111">程式碼路徑長度通常很清楚，而且由於該主題的文獻和工具廣泛提供，因此本文無法解決此情況。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="ab7ad-112">考慮 RPC 效能時，要記住的重要且已建立的一般效能規則如下：找出系統中的瓶頸，並解決此問題。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="ab7ad-113">管制瓶頸可能不是 RPC 程式設計，如果是這種情況，則在解決瓶頸之前，RPC 中的效能微調將不會導致效能提高。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="ab7ad-114">例如，因資源爭用而造成的系統不需要更有效率地使用網路。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="ab7ad-115">如果您的系統是部署在不同的環境中，最好是確定它的所有層面都能妥善調整，因為不同的環境可能會產生各種效能瓶頸。</span><span class="sxs-lookup"><span data-stu-id="ab7ad-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 