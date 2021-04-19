---
description: 連接和中斷連線拓撲節點
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: 連接和中斷連線拓撲節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991663"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="c15a7-103">連接和中斷連線拓撲節點</span><span class="sxs-lookup"><span data-stu-id="c15a7-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="c15a7-104">若要讓拓撲正常運作，必須連接來源節點和輸出節點。</span><span class="sxs-lookup"><span data-stu-id="c15a7-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="c15a7-105">若要連接兩個拓撲節點，請將一個節點的節點輸出拖曳至另一個節點的節點輸入。</span><span class="sxs-lookup"><span data-stu-id="c15a7-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="c15a7-106">TopoEdit 會以黑線顯示節點連接。</span><span class="sxs-lookup"><span data-stu-id="c15a7-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="c15a7-107">這相當於藉由呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) 方法來連接拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="c15a7-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="c15a7-108">只有當節點連接有效時，才可以解析拓撲;亦即，如果兩個節點的媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="c15a7-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="c15a7-109">如需有關解決拓撲的詳細資訊，請參閱 [使用 TopoEdit 解析拓撲](resolving-a-topology-with-topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="c15a7-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="c15a7-110">如果您嘗試從已經連接的節點建立連線，新的節點連接會取代舊的節點連接。</span><span class="sxs-lookup"><span data-stu-id="c15a7-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="c15a7-111">若要刪除連線，請選取節點連接，然後按下 DELETE 鍵，或從 [**拓撲**] 功能表中選取 [**刪除**]。</span><span class="sxs-lookup"><span data-stu-id="c15a7-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c15a7-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="c15a7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c15a7-113">使用 TopoEdit 建立拓撲</span><span class="sxs-lookup"><span data-stu-id="c15a7-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="c15a7-114">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c15a7-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



