---
description: Advanced 拓朴建築
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Advanced 拓朴建築
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318311"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="106ec-103">Advanced 拓朴建築</span><span class="sxs-lookup"><span data-stu-id="106ec-103">Advanced Topology Building</span></span>

<span data-ttu-id="106ec-104">本節說明一些建立拓撲的先進技術。</span><span class="sxs-lookup"><span data-stu-id="106ec-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="106ec-105">如果您想要更充分掌控傳送至媒體會話的拓撲，您可以使用這些技術。</span><span class="sxs-lookup"><span data-stu-id="106ec-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="106ec-106">因為這些技術適用于超越標準拓撲載入器所提供之功能的案例，所以許多詳細資料將取決於您應用程式的特定需求。</span><span class="sxs-lookup"><span data-stu-id="106ec-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="106ec-107">因此，本節會在較小的子工作（而不是完整的端對端案例）上以鬆散的方式組織。</span><span class="sxs-lookup"><span data-stu-id="106ec-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="106ec-108">一般的播放應用程式會遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="106ec-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="106ec-109">應用程式會建立部分拓撲，並在媒體會話上將它排入佇列。</span><span class="sxs-lookup"><span data-stu-id="106ec-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="106ec-110">媒體會話會叫用拓撲載入器來解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="106ec-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="106ec-111">如果您想要超越拓撲載入器的功能，有三種常見的方法：</span><span class="sxs-lookup"><span data-stu-id="106ec-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="106ec-112">建立完整的拓撲。</span><span class="sxs-lookup"><span data-stu-id="106ec-112">Build a complete topology.</span></span> <span data-ttu-id="106ec-113">當您將拓撲排入媒體會話的佇列時，請使用 MFSESSION SetTopology NORESOLUTION 旗標呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="106ec-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="106ec-114">此旗標可防止媒體會話嘗試解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="106ec-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="106ec-115">直接叫用拓撲載入器來解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="106ec-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="106ec-116">然後，您可以修改完整拓撲，然後將它排入媒體會話的佇列。</span><span class="sxs-lookup"><span data-stu-id="106ec-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="106ec-117">執行自訂拓撲載入器。</span><span class="sxs-lookup"><span data-stu-id="106ec-117">Implement a custom topology loader.</span></span> <span data-ttu-id="106ec-118">使用這個方法，您可以將部分拓撲排在佇列中，但是媒體會話會叫用您的自訂載入器，而不是標準媒體基礎的執行。</span><span class="sxs-lookup"><span data-stu-id="106ec-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="106ec-119">這種方法的其中一個優點是您可以在受保護的環境內執行自訂拓撲建立。</span><span class="sxs-lookup"><span data-stu-id="106ec-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="106ec-120">不過，在這種情況下 (，拓撲載入器必須是受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="106ec-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="106ec-121">如需詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="106ec-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="106ec-122">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="106ec-122">This section contains the following topics.</span></span>



| <span data-ttu-id="106ec-123">主題</span><span class="sxs-lookup"><span data-stu-id="106ec-123">Topic</span></span>                                                                          | <span data-ttu-id="106ec-124">描述</span><span class="sxs-lookup"><span data-stu-id="106ec-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="106ec-125">自訂拓撲載入器</span><span class="sxs-lookup"><span data-stu-id="106ec-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="106ec-126">如何針對媒體會話提供 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) 的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="106ec-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="106ec-127">將輸出節點系結至媒體接收</span><span class="sxs-lookup"><span data-stu-id="106ec-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="106ec-128">如果您在媒體會話之外使用拓撲載入器，如何準備拓撲中的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="106ec-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="106ec-129">將解碼器新增至拓撲</span><span class="sxs-lookup"><span data-stu-id="106ec-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="106ec-130">如何手動選取解碼器，然後將它新增至拓撲。</span><span class="sxs-lookup"><span data-stu-id="106ec-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="106ec-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="106ec-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106ec-132">拓撲</span><span class="sxs-lookup"><span data-stu-id="106ec-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



