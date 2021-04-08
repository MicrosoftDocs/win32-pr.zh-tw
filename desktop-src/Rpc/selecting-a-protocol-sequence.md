---
title: 選取通訊協定順序
description: 通訊協定序列是網路作業系統用來透過網路與其他電腦交談的語言。
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021900"
---
# <a name="selecting-a-protocol-sequence"></a><span data-ttu-id="3b822-103">選取通訊協定順序</span><span class="sxs-lookup"><span data-stu-id="3b822-103">Selecting a Protocol Sequence</span></span>

<span data-ttu-id="3b822-104">通訊協定序列是網路作業系統用來透過網路與其他電腦交談的語言。</span><span class="sxs-lookup"><span data-stu-id="3b822-104">A protocol sequence is the language that a network operating system uses to talk over the network to other computers.</span></span> <span data-ttu-id="3b822-105">更具體來說，RPC 應用程式必須指定代表 RPC 通訊協定、傳輸通訊協定和網路通訊協定組合的字串。</span><span class="sxs-lookup"><span data-stu-id="3b822-105">In more specific terms, RPC applications must specify a string that represents a combination of an RPC protocol, a transport protocol, and a network protocol.</span></span>

<span data-ttu-id="3b822-106">Microsoft RPC 支援三種 RPC 通訊協定：</span><span class="sxs-lookup"><span data-stu-id="3b822-106">Microsoft RPC supports three RPC protocols:</span></span>

-   <span data-ttu-id="3b822-107">網路運算架構連接導向的通訊協定 (NCACN) </span><span class="sxs-lookup"><span data-stu-id="3b822-107">Network Computing Architecture connection-oriented protocol (NCACN)</span></span>
-   <span data-ttu-id="3b822-108">網路運算架構資料包協定 (NCADG) </span><span class="sxs-lookup"><span data-stu-id="3b822-108">Network Computing Architecture datagram protocol (NCADG)</span></span>
-   <span data-ttu-id="3b822-109">網路運算架構本機遠端程序呼叫 (NCALRPC) </span><span class="sxs-lookup"><span data-stu-id="3b822-109">Network Computing Architecture local remote procedure call (NCALRPC)</span></span>

<span data-ttu-id="3b822-110">RPC 應用程式可以使用 NCALRPC 通訊協定來叫用在執行用戶端程式的同一部電腦上執行的伺服器程式所提供的程式。</span><span class="sxs-lookup"><span data-stu-id="3b822-110">RPC applications can use the NCALRPC protocol to invoke procedures offered by server programs running on the same computer that the client program runs on.</span></span> <span data-ttu-id="3b822-111">目前這是在同一部電腦上，以不同的進程呼叫功能最有效率的方法。</span><span class="sxs-lookup"><span data-stu-id="3b822-111">This is, by far, the most efficient method for calling functionality in a different process on the same computer.</span></span>

<span data-ttu-id="3b822-112">您的應用程式所使用的傳輸和網路通訊協定，取決於網路支援的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3b822-112">The transport and network protocols that your application uses depend on which protocols the network supports.</span></span> <span data-ttu-id="3b822-113">現今許多網路（包括網際網路）都支援 TCP/IP。</span><span class="sxs-lookup"><span data-stu-id="3b822-113">Many networks today, including the Internet, support TCP/IP.</span></span> <span data-ttu-id="3b822-114">其他常見的傳輸和網路通訊協定是 IPX/SPX、NetBIOS 和 AppleTalk DSP。</span><span class="sxs-lookup"><span data-stu-id="3b822-114">Other common transport and network protocols are IPX/SPX, NetBIOS, and AppleTalk DSP.</span></span> <span data-ttu-id="3b822-115">Microsoft RPC 支援這些和其他傳輸和網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3b822-115">Microsoft RPC supports these and other transport and network protocols.</span></span> <span data-ttu-id="3b822-116">如需完整清單，請參閱 [通訊協定順序常數](protocol-sequence-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="3b822-116">For a complete list, see [Protocol Sequence Constants](protocol-sequence-constants.md).</span></span>

<span data-ttu-id="3b822-117">當您的應用程式使用自動系結控制碼時，不需要指定通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="3b822-117">When your application uses automatic binding handles, it does not need to specify the protocol sequence.</span></span> <span data-ttu-id="3b822-118">如果它使用隱含或明確的控制碼，則必須取得或指定通訊協定順序。</span><span class="sxs-lookup"><span data-stu-id="3b822-118">If it uses implicit or explicit handles, it must obtain or specify the protocol sequence.</span></span> <span data-ttu-id="3b822-119">每個分散式系統都必須檢查將部署的環境，以判斷哪一個通訊協定序列最適合該環境。</span><span class="sxs-lookup"><span data-stu-id="3b822-119">Each distributed system must examine the environment in which it will be deployed to determine which protocol sequence is best suited for that environment.</span></span>

<span data-ttu-id="3b822-120">並非所有的通訊協定順序都有對等的功能。</span><span class="sxs-lookup"><span data-stu-id="3b822-120">Not all protocol sequences have equivalent functionality.</span></span> <span data-ttu-id="3b822-121">開發人員應確認所選的通訊協定順序是否支援必要的功能。</span><span class="sxs-lookup"><span data-stu-id="3b822-121">Developers should verify that the chosen protocol sequence supports the required features.</span></span> <span data-ttu-id="3b822-122">一般情況下，建議使用 **ncalrpc** 進行本機通訊，並使用 **ncacn \_ ip \_ tcp** 或 **ncacn \_ HTTP** 進行遠端通訊; 它們可在所有環境中運作，且具有最佳效能，而且支援所有必要的最佳作法功能。</span><span class="sxs-lookup"><span data-stu-id="3b822-122">In general, **ncalrpc** for local communications and **ncacn\_ip\_tcp** or **ncacn\_http** for remote communications are recommended; they work in all environments, they have optimal performance, and they support all necessary, best-practice features.</span></span>

<span data-ttu-id="3b822-123">用戶端也可以指定它們從 Active Directory、登錄、安裝程式所建立及初始化的環境變數、應用程式特定的設定檔，或程式原始程式碼中的常值字串所取得的通訊協定順序資訊。</span><span class="sxs-lookup"><span data-stu-id="3b822-123">Clients can also specify protocol sequence information that they obtain from Active Directory, the registry, environment variables created and initialized by the setup program, application-specific configuration files, or from literal strings in the program source code.</span></span>

<span data-ttu-id="3b822-124">當您的用戶端程式具有有效的通訊協定順序字串之後，就可以將該資訊傳遞給 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 和 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 函式，以建立系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b822-124">After your client program has a valid protocol sequence string, it can pass that information to the [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) and [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) functions to create the binding handle.</span></span>

 

 




