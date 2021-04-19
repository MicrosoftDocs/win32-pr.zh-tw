---
description: 建立來源節點
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: 建立來源節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973989"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="8eb44-103">建立來源節點</span><span class="sxs-lookup"><span data-stu-id="8eb44-103">Creating Source Nodes</span></span>

<span data-ttu-id="8eb44-104">來源節點代表來自媒體來源的一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="8eb44-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="8eb44-105">來源節點必須包含媒體來源、簡報描述元和資料流程描述項的指標。</span><span class="sxs-lookup"><span data-stu-id="8eb44-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="8eb44-106">若要將來源節點新增至拓撲，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="8eb44-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="8eb44-107">使用 **MF \_ 拓撲 \_ SOURCESTREAM \_ 節點** 旗標呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立來源節點。</span><span class="sxs-lookup"><span data-stu-id="8eb44-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="8eb44-108">使用媒體來源的指標，在節點上設定 [ [**MF \_ TOPONODE \_ 來源**](mf-toponode-source-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8eb44-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="8eb44-109">使用媒體來源之呈現描述項的指標，在節點上設定 [ [**MF \_ TOPONODE \_ 展示 \_ 描述**](mf-toponode-presentation-descriptor-attribute.md) 項] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8eb44-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="8eb44-110">使用資料流程的資料流程描述元指標，在節點上設定 [ [**MF \_ TOPONODE \_ 資料流程 \_ 描述**](mf-toponode-stream-descriptor-attribute.md) 元] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8eb44-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="8eb44-111">呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。</span><span class="sxs-lookup"><span data-stu-id="8eb44-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="8eb44-112">下列範例會建立並初始化來源節點。</span><span class="sxs-lookup"><span data-stu-id="8eb44-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8eb44-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8eb44-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb44-114">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="8eb44-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="8eb44-115">媒體來源</span><span class="sxs-lookup"><span data-stu-id="8eb44-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="8eb44-116">拓撲</span><span class="sxs-lookup"><span data-stu-id="8eb44-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="8eb44-117">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8eb44-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



