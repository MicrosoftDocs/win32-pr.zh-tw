---
description: 使用 TopoEdit 建立拓撲
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: 使用 TopoEdit 建立拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111884"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="1004e-103">使用 TopoEdit 建立拓撲</span><span class="sxs-lookup"><span data-stu-id="1004e-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="1004e-104">拓撲必須具有下列三個節點：</span><span class="sxs-lookup"><span data-stu-id="1004e-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="1004e-105">來源節點：來自媒體檔案的資料流程，用來做為拓撲的來源。</span><span class="sxs-lookup"><span data-stu-id="1004e-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="1004e-106">轉換節點：媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="1004e-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="1004e-107">這些節點通常是針對拓撲的編碼器、解碼器和效果。</span><span class="sxs-lookup"><span data-stu-id="1004e-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="1004e-108">輸出節點：將媒體資料、影片畫面或音訊串流傳遞給媒體會話以進行播放的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="1004e-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="1004e-109">如需拓撲結構的詳細資訊，請參閱 [關於](about-topologies.md)拓撲。</span><span class="sxs-lookup"><span data-stu-id="1004e-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="1004e-110">若要建立拓撲，您必須加入節點、連接節點，並解析拓撲，以便可以播放。</span><span class="sxs-lookup"><span data-stu-id="1004e-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="1004e-111">拓撲節點會顯示為方塊，顯示節點名稱的文字。</span><span class="sxs-lookup"><span data-stu-id="1004e-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="1004e-112">綠色方塊代表使用者新增的節點。</span><span class="sxs-lookup"><span data-stu-id="1004e-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="1004e-113">解決拓撲時，TopoEdit 可以自動將轉換節點新增至拓撲。</span><span class="sxs-lookup"><span data-stu-id="1004e-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="1004e-114">這些會顯示為 [ **拓撲] 窗格** 上的藍色方塊。</span><span class="sxs-lookup"><span data-stu-id="1004e-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="1004e-115">拓撲輸入和輸出在節點邊緣以黑色方塊表示。</span><span class="sxs-lookup"><span data-stu-id="1004e-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="1004e-116">節點的 *輸入* 會顯示在節點的左側，而 *節點的輸出* 則位於節點的右側。</span><span class="sxs-lookup"><span data-stu-id="1004e-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="1004e-117">拓撲節點是透過節點連線來連接，此 *連接* 會以黑色線條的形式出現，將一個節點的節點輸入連接到另一個節點的節點輸出。</span><span class="sxs-lookup"><span data-stu-id="1004e-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="1004e-118">下圖顯示音訊來源的連線拓撲。</span><span class="sxs-lookup"><span data-stu-id="1004e-118">The following illustration shows a connected topology for an audio source.</span></span>

![顯示從來源節點到兩個轉換節點，然後再到輸出節點之連接的圖例](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="1004e-120">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="1004e-120">This section contains the following topics:</span></span>



| <span data-ttu-id="1004e-121">主題</span><span class="sxs-lookup"><span data-stu-id="1004e-121">Topic</span></span>                                                                                          | <span data-ttu-id="1004e-122">描述</span><span class="sxs-lookup"><span data-stu-id="1004e-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="1004e-123">使用 TopoEdit 新增來源節點</span><span class="sxs-lookup"><span data-stu-id="1004e-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="1004e-124">描述將來源節點新增至拓撲的程式。</span><span class="sxs-lookup"><span data-stu-id="1004e-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="1004e-125">使用 TopoEdit 新增轉換節點</span><span class="sxs-lookup"><span data-stu-id="1004e-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="1004e-126">描述將「轉換」節點新增至拓撲的流程。</span><span class="sxs-lookup"><span data-stu-id="1004e-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="1004e-127">使用 TopoEdit 新增輸出節點</span><span class="sxs-lookup"><span data-stu-id="1004e-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="1004e-128">描述將輸出節點加入拓撲的程式。</span><span class="sxs-lookup"><span data-stu-id="1004e-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="1004e-129">連接和中斷連線拓撲節點</span><span class="sxs-lookup"><span data-stu-id="1004e-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="1004e-130">描述連接兩個節點的進程。</span><span class="sxs-lookup"><span data-stu-id="1004e-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="1004e-131">使用 TopoEdit 解析拓撲</span><span class="sxs-lookup"><span data-stu-id="1004e-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="1004e-132">描述拓撲解析的流程。</span><span class="sxs-lookup"><span data-stu-id="1004e-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="1004e-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="1004e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1004e-134">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="1004e-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



