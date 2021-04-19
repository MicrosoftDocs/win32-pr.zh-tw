---
title: 存根
description: 存根（如同 proxy）是由一或多個介面片段和管理員所組成。
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "106985999"
---
# <a name="stub"></a><span data-ttu-id="f2646-103">存根</span><span class="sxs-lookup"><span data-stu-id="f2646-103">Stub</span></span>

<span data-ttu-id="f2646-104">存根（如同 proxy）是由一或多個介面片段和管理員所組成。</span><span class="sxs-lookup"><span data-stu-id="f2646-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="f2646-105">每個介面存根都會提供程式碼，以 unmarshal 呼叫其中一個物件支援介面的參數和程式碼。</span><span class="sxs-lookup"><span data-stu-id="f2646-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="f2646-106">每個 stub 也提供內部通訊的介面。</span><span class="sxs-lookup"><span data-stu-id="f2646-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="f2646-107">存根管理員會持續追蹤可用的介面存根。</span><span class="sxs-lookup"><span data-stu-id="f2646-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="f2646-108">不過，存根和 proxy 之間有下列差異：</span><span class="sxs-lookup"><span data-stu-id="f2646-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="f2646-109">最重要的差異在於存根代表物件位址空間中的用戶端。</span><span class="sxs-lookup"><span data-stu-id="f2646-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="f2646-110">存根不會實作為匯總物件，因為不需要將用戶端視為單一單位;存根中的每個部分都是個別的元件。</span><span class="sxs-lookup"><span data-stu-id="f2646-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="f2646-111">介面存根是私用的，而非公用。</span><span class="sxs-lookup"><span data-stu-id="f2646-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="f2646-112">介面存根會執行 [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer)，而不是 [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer)。</span><span class="sxs-lookup"><span data-stu-id="f2646-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="f2646-113">存根不會封裝要封送處理的參數，而是在封送處理之後 unpackages 它們，然後封裝回復。</span><span class="sxs-lookup"><span data-stu-id="f2646-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="f2646-114">存根的結構</span><span class="sxs-lookup"><span data-stu-id="f2646-114">Structure of the Stub</span></span>

<span data-ttu-id="f2646-115">下圖顯示存根的結構。</span><span class="sxs-lookup"><span data-stu-id="f2646-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="f2646-116">每個介面存根都會連接到物件上的介面。</span><span class="sxs-lookup"><span data-stu-id="f2646-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="f2646-117">通道會將傳入訊息分派至適當的介面存根。</span><span class="sxs-lookup"><span data-stu-id="f2646-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="f2646-118">所有元件都會透過 [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer)（可存取 RPC 執行時間程式庫的介面）與通道通訊。</span><span class="sxs-lookup"><span data-stu-id="f2646-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![顯示存根結構的螢幕擷取畫面。](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="f2646-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2646-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2646-121">通道</span><span class="sxs-lookup"><span data-stu-id="f2646-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="f2646-122">物件間通訊</span><span class="sxs-lookup"><span data-stu-id="f2646-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="f2646-123">封送處理詳細資料</span><span class="sxs-lookup"><span data-stu-id="f2646-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="f2646-124">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="f2646-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="f2646-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="f2646-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 