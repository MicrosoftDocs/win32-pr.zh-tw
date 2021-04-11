---
description: 建立輸出節點
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: 建立輸出節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847639"
---
# <a name="creating-output-nodes"></a><span data-ttu-id="e6c09-103">建立輸出節點</span><span class="sxs-lookup"><span data-stu-id="e6c09-103">Creating Output Nodes</span></span>

<span data-ttu-id="e6c09-104">輸出節點表示媒體接收上的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="e6c09-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="e6c09-105">有兩種方式可以初始化輸出節點：</span><span class="sxs-lookup"><span data-stu-id="e6c09-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="e6c09-106">從資料流程接收的指標。</span><span class="sxs-lookup"><span data-stu-id="e6c09-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="e6c09-107">從媒體接收器的啟用物件指標。</span><span class="sxs-lookup"><span data-stu-id="e6c09-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="e6c09-108">如果您要在受保護的媒體路徑中載入拓撲 (PMP) ，您必須使用啟用物件，才能在受保護的進程內建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e6c09-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="e6c09-109">第一個方法 (使用串流接收器的指標) 無法與 PMP 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e6c09-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="e6c09-110">從資料流程接收建立輸出節點</span><span class="sxs-lookup"><span data-stu-id="e6c09-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="e6c09-111">若要從資料流程接收建立輸出節點，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e6c09-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="e6c09-112">建立媒體接收器的實例。</span><span class="sxs-lookup"><span data-stu-id="e6c09-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="e6c09-113">使用媒體接收器的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面來取得所需資料流程接收的指標。</span><span class="sxs-lookup"><span data-stu-id="e6c09-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="e6c09-114"> (**IMFMediaSink** 介面具有數個傳回資料流程接收指標的方法。 ) </span><span class="sxs-lookup"><span data-stu-id="e6c09-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="e6c09-115">使用 **MF \_ 拓撲 \_ 輸出 \_ 節點** 旗標呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e6c09-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="e6c09-116">呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入串流接收器 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e6c09-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="e6c09-117">將 [移除] 屬性上的 [ [**MF \_ TOPONODE \_ NOSHUTDOWN \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) ] 設定為 [ **FALSE** ] (選擇性，但建議使用) 。</span><span class="sxs-lookup"><span data-stu-id="e6c09-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="e6c09-118">呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。</span><span class="sxs-lookup"><span data-stu-id="e6c09-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="e6c09-119">下列範例會從資料流程接收中建立並初始化輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e6c09-119">The following example creates and initializes an output node from a stream sink.</span></span>


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



<span data-ttu-id="e6c09-120">當應用程式關閉媒體會話時，媒體會話會自動關閉媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e6c09-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="e6c09-121">因此，您無法重複使用媒體接收器與另一個媒體會話實例。</span><span class="sxs-lookup"><span data-stu-id="e6c09-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="e6c09-122">從啟用物件建立輸出節點</span><span class="sxs-lookup"><span data-stu-id="e6c09-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="e6c09-123">任何信任的媒體接收器都必須提供啟用物件，才能在受保護的進程內建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e6c09-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="e6c09-124">如需詳細資訊，請參閱 [啟用物件](activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e6c09-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="e6c09-125">建立啟用物件的特定函式將取決於媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e6c09-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="e6c09-126">若要從啟用物件建立輸出節點，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e6c09-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="e6c09-127">建立啟用物件，並取得啟用物件之 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e6c09-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="e6c09-128">使用 **MF \_ 拓撲 \_ 輸出 \_ 節點** 旗標呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e6c09-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="e6c09-129">（選擇性）在節點上設定 [ [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) ] 屬性，以指定資料流程接收的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6c09-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="e6c09-130">如果您省略此屬性，節點會預設為使用串流接收器0。</span><span class="sxs-lookup"><span data-stu-id="e6c09-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="e6c09-131">將 [移除] 屬性上的 [ [**MF \_ TOPONODE \_ NOSHUTDOWN \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) ] 設定為 [ **TRUE** ] (選擇性，但建議使用) 。</span><span class="sxs-lookup"><span data-stu-id="e6c09-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="e6c09-132">呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。</span><span class="sxs-lookup"><span data-stu-id="e6c09-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="e6c09-133">呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。</span><span class="sxs-lookup"><span data-stu-id="e6c09-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="e6c09-134">下列範例會從啟用物件建立和初始化輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e6c09-134">The following example creates and initializes an output node from an activation object.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
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



## <a name="related-topics"></a><span data-ttu-id="e6c09-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6c09-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6c09-136">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e6c09-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e6c09-137">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="e6c09-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="e6c09-138">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="e6c09-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="e6c09-139">拓撲</span><span class="sxs-lookup"><span data-stu-id="e6c09-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



