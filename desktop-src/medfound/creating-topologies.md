---
description: 建立拓撲
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: 建立拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386042"
---
# <a name="creating-topologies"></a><span data-ttu-id="88c54-103">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="88c54-103">Creating Topologies</span></span>

<span data-ttu-id="88c54-104">本節說明一些建立拓撲的一般程式。</span><span class="sxs-lookup"><span data-stu-id="88c54-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="88c54-105">建立拓撲的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="88c54-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="88c54-106">藉由呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)來建立新的拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="88c54-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="88c54-107">此函式會傳回拓撲的 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="88c54-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="88c54-108">一開始，拓撲不包含任何節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="88c54-109">若要建立拓撲的節點，請呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode)。</span><span class="sxs-lookup"><span data-stu-id="88c54-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="88c54-110">此函式會傳回節點 [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="88c54-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="88c54-111">您必須在建立節點時指定節點類型：</span><span class="sxs-lookup"><span data-stu-id="88c54-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="88c54-112">來源節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-112">Source node.</span></span>

    -   <span data-ttu-id="88c54-113">轉換節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-113">Transform node.</span></span>

    -   <span data-ttu-id="88c54-114">輸出節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-114">Output node.</span></span>

    -   <span data-ttu-id="88c54-115">T 節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-115">Tee node.</span></span>

3.  <span data-ttu-id="88c54-116">初始化每個節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-116">Initialize each node.</span></span> <span data-ttu-id="88c54-117">初始化程式依節點類型而定，如下列主題所述。</span><span class="sxs-lookup"><span data-stu-id="88c54-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="88c54-118">藉由呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode)，將每個節點新增至拓撲。</span><span class="sxs-lookup"><span data-stu-id="88c54-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="88c54-119">連接節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-119">Connect the nodes.</span></span> <span data-ttu-id="88c54-120">若要連接節點，請在上游節點上呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) ，並傳入下游節點的指標。</span><span class="sxs-lookup"><span data-stu-id="88c54-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="88c54-121">下列主題提供每個節點類型的特定步驟。</span><span class="sxs-lookup"><span data-stu-id="88c54-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="88c54-122">主題</span><span class="sxs-lookup"><span data-stu-id="88c54-122">Topic</span></span>                                                    | <span data-ttu-id="88c54-123">描述</span><span class="sxs-lookup"><span data-stu-id="88c54-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="88c54-124">建立來源節點</span><span class="sxs-lookup"><span data-stu-id="88c54-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="88c54-125">如何建立來源節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="88c54-126">建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="88c54-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="88c54-127">如何建立轉換節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="88c54-128">建立輸出節點</span><span class="sxs-lookup"><span data-stu-id="88c54-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="88c54-129">如何建立輸出節點。</span><span class="sxs-lookup"><span data-stu-id="88c54-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="88c54-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="88c54-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c54-131">拓撲</span><span class="sxs-lookup"><span data-stu-id="88c54-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



