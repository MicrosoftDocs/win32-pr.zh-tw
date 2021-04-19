---
description: 使用對等圖形時，必須以特定順序呼叫函數。 呼叫的流程取決於您是建立或開啟對等圖形。 本主題指出簡單對等圖形應用程式中函式呼叫的流程。
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: 使用圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975105"
---
# <a name="working-with-graphs"></a><span data-ttu-id="cbe14-105">使用圖形</span><span class="sxs-lookup"><span data-stu-id="cbe14-105">Working with Graphs</span></span>

<span data-ttu-id="cbe14-106">使用對等圖形時，必須以特定順序呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="cbe14-106">When working with peer graphs, functions must be called in a specific order.</span></span> <span data-ttu-id="cbe14-107">呼叫的流程取決於您是建立或開啟對等圖形。</span><span class="sxs-lookup"><span data-stu-id="cbe14-107">The flow of calls depends on whether you are creating or opening a peer graph.</span></span> <span data-ttu-id="cbe14-108">本主題指出簡單對等圖形應用程式中函式呼叫的流程。</span><span class="sxs-lookup"><span data-stu-id="cbe14-108">This topic identifies the flow of function calls in a simple peer graph application.</span></span>

## <a name="starting-up-a-graph"></a><span data-ttu-id="cbe14-109">啟動圖形</span><span class="sxs-lookup"><span data-stu-id="cbe14-109">Starting Up a Graph</span></span>

<span data-ttu-id="cbe14-110">在應用程式呼叫對等圖形 API 中的函式之前，必須先呼叫 [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) 來初始化應用程式的對等圖形 api，然後設定支援的版本。</span><span class="sxs-lookup"><span data-stu-id="cbe14-110">Before an application calls a function in the Peer Graphing API, [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) must be called to initialize the Peer Graphing API for an application, and then set the supported version.</span></span>

## <a name="creating-a-peer-graph"></a><span data-ttu-id="cbe14-111">建立對等圖形</span><span class="sxs-lookup"><span data-stu-id="cbe14-111">Creating a Peer Graph</span></span>

<span data-ttu-id="cbe14-112">下列程式會識別用來建立對等圖形的呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="cbe14-112">The following procedure identifies the flow of calls for creating a peer graph.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbe14-113">只有一個對等應該呼叫 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-113">Only one peer should call [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).</span></span> <span data-ttu-id="cbe14-114">所有其他對等都應該呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-114">All other peers should call [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).</span></span> <span data-ttu-id="cbe14-115">對 **PeerGraphCreate** 的多個呼叫會使圖形失效。</span><span class="sxs-lookup"><span data-stu-id="cbe14-115">Multiple calls to **PeerGraphCreate** invalidate a graph.</span></span>

 

-   <span data-ttu-id="cbe14-116">建立對等圖形。</span><span class="sxs-lookup"><span data-stu-id="cbe14-116">Create a peer graph.</span></span> <span data-ttu-id="cbe14-117">呼叫 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-117">Call [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).</span></span>
-   <span data-ttu-id="cbe14-118">註冊對等事件。</span><span class="sxs-lookup"><span data-stu-id="cbe14-118">Register for peer events.</span></span> <span data-ttu-id="cbe14-119">呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-119">Call [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).</span></span>
    > [!Note]  
    > <span data-ttu-id="cbe14-120">如需註冊對等事件的詳細資訊，請參閱 [事件基礎結構](peer-events-infrastructure.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-120">For more information about registering for peer events, see [Events Infrastructure](peer-events-infrastructure.md).</span></span>

     

-   <span data-ttu-id="cbe14-121">接聽對等圖形的連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-121">Listen for connections to a peer graph.</span></span> <span data-ttu-id="cbe14-122">呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-122">Call [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>
-   <span data-ttu-id="cbe14-123">針對其餘的執行時間執行與應用程式相依的函式，例如，處理對等事件並使用連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-123">Perform application-dependent functions for the remainder of the running time, for example, process peer events and work with connections.</span></span>
-   <span data-ttu-id="cbe14-124">關閉對等圖形的連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-124">Close the connection to a peer graph.</span></span> <span data-ttu-id="cbe14-125">呼叫 [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-125">Call [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).</span></span>

## <a name="opening-a-peer-graph"></a><span data-ttu-id="cbe14-126">開啟對等圖形</span><span class="sxs-lookup"><span data-stu-id="cbe14-126">Opening a Peer Graph</span></span>

<span data-ttu-id="cbe14-127">開啟對等圖形的函式呼叫流程，取決於呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)的傳回值。</span><span class="sxs-lookup"><span data-stu-id="cbe14-127">The flow of function calls to open a peer graph depends on the return value of the call to [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).</span></span> <span data-ttu-id="cbe14-128">最重要的值為 **「 \_ 確定** 」和「 **對等」 \_ \_ 資料 \_ 建立**，如本主題的下列各節所述。</span><span class="sxs-lookup"><span data-stu-id="cbe14-128">The most important values are **S\_OK** and **PEER\_S\_DATA\_CREATED**, which are explained in the following sections of this topic.</span></span>

> [!Note]  
> <span data-ttu-id="cbe14-129">如果呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 不會傳回所建立的「 **\_ 確定** 」或「 **對等」 \_ \_ 資料 \_**，請處理此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cbe14-129">If a call to [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) does not return **S\_OK** or **PEER\_S\_DATA\_CREATED**, handle the error.</span></span>

 

## <a name="when-peergraphopen-returns-s_ok"></a><span data-ttu-id="cbe14-130">當 PeerGraphOpen 傳回 S \_ 正常時</span><span class="sxs-lookup"><span data-stu-id="cbe14-130">When PeerGraphOpen Returns S\_OK</span></span>

<span data-ttu-id="cbe14-131">當 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 的呼叫傳回時 **， \_ 對** 等圖形和現有的資料庫也會開啟。</span><span class="sxs-lookup"><span data-stu-id="cbe14-131">When a call to [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) returns **S\_OK**, a peer graph and an existing database have been opened.</span></span> <span data-ttu-id="cbe14-132">下列程式識別當呼叫 **PeerGraphOpen** 時，您可以如何開啟對等圖形。 **\_**</span><span class="sxs-lookup"><span data-stu-id="cbe14-132">The following procedure identifies what you can do to open a peer graph when a call to **PeerGraphOpen** returns **S\_OK**</span></span>

-   <span data-ttu-id="cbe14-133">註冊對等事件。</span><span class="sxs-lookup"><span data-stu-id="cbe14-133">Register for peer events.</span></span> <span data-ttu-id="cbe14-134">呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-134">Call [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).</span></span>
    > [!Note]  
    > <span data-ttu-id="cbe14-135">如需註冊事件的詳細資訊，請參閱 [事件基礎結構](peer-events-infrastructure.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-135">For more information about registering for events, see [Events Infrastructure](peer-events-infrastructure.md).</span></span>

     

-   <span data-ttu-id="cbe14-136">找出節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-136">Locate a node.</span></span> <span data-ttu-id="cbe14-137">這是使用您所識別的方法或應用程式，在對等圖形基礎結構外部執行的進程。</span><span class="sxs-lookup"><span data-stu-id="cbe14-137">This is a process performed outside of the Peer Graphing Infrastructure, by using a method or application that you identify.</span></span> <span data-ttu-id="cbe14-138">對等圖形 API 不會提供特定的機制來尋找要連接的初始圖形節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-138">The Peer Graphing API does not provide a specific mechanism to find an initial graph node to connect to.</span></span> <span data-ttu-id="cbe14-139">應用程式必須使用另一種機制，例如 [ (PNRP) API 的對等名稱解析通訊協定 ](pnrp-namespace-provider-api.md) ，以找出初始節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-139">An application must use another mechanism, such as the [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) API, to locate the initial node.</span></span>
-   <span data-ttu-id="cbe14-140">如果找到節點，請連接到該節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-140">If a node is found, connect to it.</span></span> <span data-ttu-id="cbe14-141">呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)，然後呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) 接聽對等圖形的連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-141">Call [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), then call [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) to listen for connections to the peer graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="cbe14-142">如果找不到節點，請勿呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 和 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-142">If a node is not found, do not call [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) and [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="cbe14-143">針對執行時間的其餘部分執行應用程式相依的函式，例如，處理對等事件和使用連接，視節點是否連接至對等圖形而定。</span><span class="sxs-lookup"><span data-stu-id="cbe14-143">Perform application-dependent functions for the remainder of the running time, for example, process peer events and work with connections, depending on whether the node is connected to the peer graph or not.</span></span> <span data-ttu-id="cbe14-144">例如，應用程式可以選擇為圖形中的作用中節點設定 timeout 或定期執行探索。</span><span class="sxs-lookup"><span data-stu-id="cbe14-144">For example, the application can choose to timeout or periodically perform discovery for an active node in the graph.</span></span>
-   <span data-ttu-id="cbe14-145">關閉對等圖形的連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-145">Close the connection to the peer graph.</span></span> <span data-ttu-id="cbe14-146">呼叫 [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-146">Call [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).</span></span>

## <a name="when-peergraphopen-returns-peer_s_data_created"></a><span data-ttu-id="cbe14-147">當 PeerGraphOpen 傳回所建立的對等 \_ \_ 資料時 \_</span><span class="sxs-lookup"><span data-stu-id="cbe14-147">When PeerGraphOpen Returns PEER\_S\_DATA\_CREATED</span></span>

<span data-ttu-id="cbe14-148">當 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 傳回 **所 \_ \_ \_ 建立的對等資料** 時，表示找不到對等圖形的現有資料庫、建立新的資料庫，這是第一次開啟時。</span><span class="sxs-lookup"><span data-stu-id="cbe14-148">When [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) returns **PEER\_S\_DATA\_CREATED**, it means that an existing database for a peer graph is not found, a new database is created, and this is the first time it is opened.</span></span> <span data-ttu-id="cbe14-149">若要在對等圖形上使用或接聽，對等必須連接至對等圖形並與其同步。</span><span class="sxs-lookup"><span data-stu-id="cbe14-149">To use or listen on a peer graph, a peer must be connected to and synchronized with a peer graph.</span></span>

<span data-ttu-id="cbe14-150">下列程式識別當呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 傳回所 **\_ \_ \_ 建立的對等資料** 時，您可以執行的動作。</span><span class="sxs-lookup"><span data-stu-id="cbe14-150">The following procedure identifies what you can do to open a peer graph when a call to [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) returns **PEER\_S\_DATA\_CREATED**.</span></span>

-   <span data-ttu-id="cbe14-151">開啟對等圖形。</span><span class="sxs-lookup"><span data-stu-id="cbe14-151">Open a peer graph.</span></span> <span data-ttu-id="cbe14-152">呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-152">Call [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).</span></span>
-   <span data-ttu-id="cbe14-153">註冊對等事件。</span><span class="sxs-lookup"><span data-stu-id="cbe14-153">Register for peer events.</span></span> <span data-ttu-id="cbe14-154">呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-154">Call [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).</span></span>
    > [!Note]  
    > <span data-ttu-id="cbe14-155">如需註冊對等事件的詳細資訊，請參閱 [事件基礎結構](peer-events-infrastructure.md)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-155">For more information about registering for peer events, see [Events Infrastructure](peer-events-infrastructure.md).</span></span>

     

-   <span data-ttu-id="cbe14-156">找出節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-156">Locate a node.</span></span> <span data-ttu-id="cbe14-157">這是使用您所識別的方法或應用程式，在對等圖形基礎結構外部執行的進程。</span><span class="sxs-lookup"><span data-stu-id="cbe14-157">This is a process performed outside of the Peer Graphing Infrastructure, by using a method or application that you identify.</span></span> <span data-ttu-id="cbe14-158">對等圖形 API 不會提供特定的機制來尋找要連接的初始圖形節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-158">The Peer Graphing API does not provide a specific mechanism to find an initial graph node to connect to.</span></span> <span data-ttu-id="cbe14-159">應用程式必須使用另一種機制，例如 [ (PNRP) API 的對等名稱解析通訊協定 ](pnrp-namespace-provider-api.md) ，以找出初始節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-159">An application must use another mechanism, such as the [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) API, to locate the initial node.</span></span>
-   <span data-ttu-id="cbe14-160">如果找到節點，請連接到該節點。</span><span class="sxs-lookup"><span data-stu-id="cbe14-160">If a node is found, connect to it.</span></span> <span data-ttu-id="cbe14-161">呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)，然後呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) 接聽對等圖形的連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-161">Call [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), then call [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) to listen for connections to the peer graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="cbe14-162">如果找不到節點，請勿呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 和 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-162">If a node is not found, do not call [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) and [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="cbe14-163">針對執行時間的其餘部分執行應用程式相依的函式，例如，處理對等事件和使用連接，視節點是否連接至對等圖形而定。</span><span class="sxs-lookup"><span data-stu-id="cbe14-163">Perform application-dependent functions for the remainder of the running time, for example, process peer events and work with connections, depending on whether the node is connected to the peer graph or not.</span></span> <span data-ttu-id="cbe14-164">例如，應用程式可以選擇為圖形中的作用中節點設定 timeout 或定期執行探索。</span><span class="sxs-lookup"><span data-stu-id="cbe14-164">For example, the application can choose to timeout or periodically perform discovery for an active node in the graph.</span></span>
-   <span data-ttu-id="cbe14-165">關閉對等圖形的連接。</span><span class="sxs-lookup"><span data-stu-id="cbe14-165">Close the connection to the peer graph.</span></span> <span data-ttu-id="cbe14-166">呼叫 [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)。</span><span class="sxs-lookup"><span data-stu-id="cbe14-166">Call [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).</span></span>

 

 



