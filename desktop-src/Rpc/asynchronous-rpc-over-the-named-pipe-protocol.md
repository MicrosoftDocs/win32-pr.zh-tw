---
title: Named-Pipe 通訊協定上的非同步 RPC
description: 如果您使用具名管道 (ncacn \_ np) 做為傳輸通訊協定，您應該避免在伺服器上允許大量閒置暫止的呼叫。
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933537"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="f8393-103">Named-Pipe 通訊協定上的非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="f8393-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="f8393-104">如果您使用具名管道 ([**ncacn \_ Np**](/windows/desktop/Midl/ncacn-np)) 做為傳輸通訊協定，您應該避免在伺服器上允許大量閒置暫止的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f8393-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="f8393-105">使用具名管道時，每個等候回復的用戶端都將在伺服器上讀取暫止的具名管道，而每個用戶端都需要特定數量的核心記憶體。</span><span class="sxs-lookup"><span data-stu-id="f8393-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="f8393-106">例如，您不會想要對具有具名管道傳輸的新電子郵件使用通知呼叫，因為即使用戶端閒置，而且核心記憶體可能會耗盡，這類呼叫仍會維持擱置狀態。</span><span class="sxs-lookup"><span data-stu-id="f8393-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="f8393-107">請注意，這不是其他連接導向通訊協定的問題，例如 [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)。</span><span class="sxs-lookup"><span data-stu-id="f8393-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="f8393-108">由於具名管道是傳輸通訊協定，因此您的應用程式可以藉由指定 [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np) 作為字串系結中的通訊協定來使用它們。</span><span class="sxs-lookup"><span data-stu-id="f8393-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="f8393-109">如需具名管道的詳細資訊，請參閱 [具名管道](/windows/desktop/ipc/named-pipes)。</span><span class="sxs-lookup"><span data-stu-id="f8393-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="f8393-110">如需建立字串系結的詳細資訊，請參閱 [使用字串](finding-server-host-systems.md)系結。</span><span class="sxs-lookup"><span data-stu-id="f8393-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 