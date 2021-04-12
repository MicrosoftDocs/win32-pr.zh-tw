---
description: 使用 TopoEdit 解析拓撲
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: 使用 TopoEdit 解析拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191757"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="c8a0e-103">使用 TopoEdit 解析拓撲</span><span class="sxs-lookup"><span data-stu-id="c8a0e-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="c8a0e-104">拓撲有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="c8a0e-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="c8a0e-105">部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-105">Partial Topology.</span></span> <span data-ttu-id="c8a0e-106">來源節點會直接連接至輸出節點。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="c8a0e-107">在某些情況下，部分拓撲可以有一些中繼轉換節點（例如效果），但並非全部。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="c8a0e-108">略過的轉換節點通常是「解碼器」或「格式轉換 MFTs，例如「色彩轉換器」和「音訊 resamplers」。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="c8a0e-109">完整拓撲。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-109">Full Topology.</span></span> <span data-ttu-id="c8a0e-110">來源節點會透過轉換節點連接至輸出節點。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="c8a0e-111">此類型的拓撲必須具有每個節點，才能處理資料。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="c8a0e-112">TopoEdit 只能播放完整的拓撲。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="c8a0e-113">TopoEdit 會使用媒體基礎所提供的拓撲載入器物件，藉由插入必要的轉換，將部分拓撲轉換成完整拓撲。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="c8a0e-114">建立完整拓撲的程式稱為解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="c8a0e-115">如需拓撲類型的詳細資訊，請參閱 [關於](about-topologies.md)拓撲的「部分拓撲」一節。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="c8a0e-116">在您解決拓撲之前，請確定：</span><span class="sxs-lookup"><span data-stu-id="c8a0e-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="c8a0e-117">拓撲包含來源節點和輸出節點。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="c8a0e-118">來源和輸出節點是由有效的節點連接所連接。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="c8a0e-119">在拓撲解析期間，拓撲載入器會檢查節點的媒體類型是否相容。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="c8a0e-120">如果有不正確節點連接，則處理常式會失敗，並顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="c8a0e-121">若要解決拓撲，請在 [ **拓撲** ] 功能表中，按一下 [ **解析拓撲**]。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="c8a0e-122">工具列會指出拓撲狀態： **\[ 已解決 \]** 或 **\[ 未解決 \]**。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="c8a0e-123">如果 TopoEdit 成功解析拓撲，**拓撲狀態** 會設為 [ **\[ 已 \] 解決**]，並啟用播放控制項。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="c8a0e-124">每次您對拓撲進行變更時，**拓撲狀態** 都會設定為 [ **\[ 未 \] 解決**]，這表示它必須重新解析。</span><span class="sxs-lookup"><span data-stu-id="c8a0e-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8a0e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8a0e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a0e-126">使用 TopoEdit 建立拓撲</span><span class="sxs-lookup"><span data-stu-id="c8a0e-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="c8a0e-127">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="c8a0e-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



