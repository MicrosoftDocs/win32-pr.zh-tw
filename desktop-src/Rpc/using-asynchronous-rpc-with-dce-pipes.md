---
title: 使用具有 DCE 管道的非同步 RPC
description: Microsoft RPC 支援使用 DCE 管道。 雖然它們共用類似的名稱，但 DCE 管道與具名管道無關。 具名管道是傳輸通訊協定。 DCE 管道是與通訊協定無關的用戶端/伺服器通訊方法。
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021402"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="a3664-106">使用具有 DCE 管道的非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="a3664-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="a3664-107">Microsoft RPC 支援使用 DCE 管道。</span><span class="sxs-lookup"><span data-stu-id="a3664-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="a3664-108">雖然它們共用類似的名稱，但 DCE 管道與 [具名管道](asynchronous-rpc-over-the-named-pipe-protocol.md)無關。</span><span class="sxs-lookup"><span data-stu-id="a3664-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="a3664-109">具名管道是傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a3664-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="a3664-110">DCE 管道是與通訊協定無關的用戶端/伺服器通訊方法。</span><span class="sxs-lookup"><span data-stu-id="a3664-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="a3664-111">本節提供使用非同步 DCE 管道的 RPC 討論。</span><span class="sxs-lookup"><span data-stu-id="a3664-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="a3664-112">它分成下列主題：</span><span class="sxs-lookup"><span data-stu-id="a3664-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="a3664-113">非同步管道</span><span class="sxs-lookup"><span data-stu-id="a3664-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="a3664-114">宣告非同步管道</span><span class="sxs-lookup"><span data-stu-id="a3664-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="a3664-115">用戶端非同步管道處理</span><span class="sxs-lookup"><span data-stu-id="a3664-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="a3664-116">伺服器端非同步管道處理</span><span class="sxs-lookup"><span data-stu-id="a3664-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="a3664-117">如需非同步管道 RPC 應用程式範例，請參閱平臺軟體發展工具組中的 FileRep 範例 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="a3664-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




