---
description: 將輸出節點系結至媒體接收
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: 將輸出節點系結至媒體接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514313"
---
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="e8287-103">將輸出節點系結至媒體接收</span><span class="sxs-lookup"><span data-stu-id="e8287-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="e8287-104">本主題描述如何在使用媒體會話之外的拓撲載入器時，初始化拓撲中的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e8287-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="e8287-105">輸出節點一開始會包含下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="e8287-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="e8287-106">[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="e8287-107">[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="e8287-108">在後者的情況下，在拓撲載入器解析拓撲之前， [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標必須轉換成 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="e8287-109">在大部分的情況下，此程式的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="e8287-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="e8287-110">應用程式會將部分拓撲排入媒體會話的佇列。</span><span class="sxs-lookup"><span data-stu-id="e8287-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="e8287-111">針對所有輸出節點，媒體會話會將 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標轉換成 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="e8287-112">此 *進程稱為將* 輸出節點系結至媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e8287-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="e8287-113">媒體會話會將修改過的拓撲傳送至 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法。</span><span class="sxs-lookup"><span data-stu-id="e8287-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="e8287-114">但是，如果您直接使用 (媒體會話) 之外的拓撲載入器，則您的應用程式必須在呼叫 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load)之前系結輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e8287-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="e8287-115">若要系結輸出節點，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e8287-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="e8287-116">呼叫 [**IMFTopologyNode：： GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) 以取得節點的物件指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="e8287-117">查詢 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的物件指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="e8287-118">如果此呼叫成功，則不需要執行任何動作，因此請略過其餘的步驟。</span><span class="sxs-lookup"><span data-stu-id="e8287-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="e8287-119">如果上一個步驟失敗，請查詢 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的物件指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="e8287-120">藉由呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)來建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e8287-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="e8287-121">指定 **IID \_ IMFMediaSink** 來取得媒體接收器的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="e8287-122">查詢適用于 [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) 屬性的節點。</span><span class="sxs-lookup"><span data-stu-id="e8287-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="e8287-123">這個屬性的值是此節點之資料流程接收的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8287-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="e8287-124">如果未設定 **MF \_ TOPONODE \_ STREAMID** 屬性，則預設的資料流程識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="e8287-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="e8287-125">媒體接收上可能已存在適當的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="e8287-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="e8287-126">若要檢查，請在媒體接收器上呼叫 [**IMFMediaSink：： GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) 。</span><span class="sxs-lookup"><span data-stu-id="e8287-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="e8287-127">如果資料流程接收存在，此方法會傳回其 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="e8287-128">如果這個呼叫失敗，請嘗試呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)來加入新的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="e8287-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="e8287-129">如果兩個呼叫都失敗，則表示媒體接收器不支援要求的資料流程識別碼，且此拓撲節點未正確設定。</span><span class="sxs-lookup"><span data-stu-id="e8287-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="e8287-130">傳回錯誤碼，並略過下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="e8287-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="e8287-131">呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject)，並傳入上一個步驟中的 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="e8287-132">此呼叫會取代節點的物件指標，讓節點包含資料流程接收的指標，而不是指向啟用物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="e8287-133">下列程式碼顯示如何系結輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e8287-133">The following code shows how to bind an output node.</span></span>


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="e8287-134">此範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="e8287-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="e8287-135">下一個範例顯示如何在拓撲中系結所有輸出節點。</span><span class="sxs-lookup"><span data-stu-id="e8287-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="e8287-136">這個範例會使用 [**IMFTopology：： GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) 方法，從拓撲中取得輸出節點的集合。</span><span class="sxs-lookup"><span data-stu-id="e8287-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="e8287-137">然後，它會依序呼叫上述範例中的每個節點上所顯示的函式。</span><span class="sxs-lookup"><span data-stu-id="e8287-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e8287-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8287-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8287-139">Advanced 拓朴建築</span><span class="sxs-lookup"><span data-stu-id="e8287-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="e8287-140">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="e8287-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="e8287-141">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="e8287-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



