---
description: 建立轉換節點
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: 建立轉換節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510814"
---
# <a name="creating-transform-nodes"></a><span data-ttu-id="497f5-103">建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="497f5-103">Creating Transform Nodes</span></span>

<span data-ttu-id="497f5-104">轉換節點代表媒體基礎轉換 (MFT) ，例如，解碼器或編碼器。</span><span class="sxs-lookup"><span data-stu-id="497f5-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="497f5-105">有幾種不同的方式可以初始化轉換節點：</span><span class="sxs-lookup"><span data-stu-id="497f5-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="497f5-106">從 MFT 的指標。</span><span class="sxs-lookup"><span data-stu-id="497f5-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="497f5-107">從 MFT 的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="497f5-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="497f5-108">從 MFT 的啟用物件指標。</span><span class="sxs-lookup"><span data-stu-id="497f5-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="497f5-109">如果您要在受保護的媒體路徑中載入拓撲 (PMP) ，您必須使用 CLSID 或啟始物件，才能在受保護的進程內建立該 MFT。</span><span class="sxs-lookup"><span data-stu-id="497f5-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="497f5-110">使用 (的) 指標的第一種方法無法與 PMP 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="497f5-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="497f5-111">從 MFT 建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="497f5-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="497f5-112">若要從 MFT 建立轉換節點，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="497f5-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="497f5-113">建立 MFT 的實例，並取得 MFT [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="497f5-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="497f5-114">使用 [ **MF \_ 拓撲轉換] \_ \_ 節點** 旗標來呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立 [轉換] 節點。</span><span class="sxs-lookup"><span data-stu-id="497f5-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="497f5-115">呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標。</span><span class="sxs-lookup"><span data-stu-id="497f5-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="497f5-116">呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。</span><span class="sxs-lookup"><span data-stu-id="497f5-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="497f5-117">下列範例會從 MFT 建立和初始化轉換節點。</span><span class="sxs-lookup"><span data-stu-id="497f5-117">The following example creates and initializes a transform node from an MFT.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="497f5-118">從 CLSID 建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="497f5-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="497f5-119">若要從 CLSID 建立轉換節點，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="497f5-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="497f5-120">尋找 MFT 的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="497f5-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="497f5-121">您可以使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函式，依類別（例如，解碼器或編碼器）來尋找 MFTs 的 clsid。</span><span class="sxs-lookup"><span data-stu-id="497f5-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="497f5-122">您也可以知道您想要使用的特定 MFT 的 CLSID (例如，如果您已執行自己的自訂 MFT) 。</span><span class="sxs-lookup"><span data-stu-id="497f5-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="497f5-123">使用 [ **MF \_ 拓撲轉換] \_ \_ 節點** 旗標來呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立 [轉換] 節點。</span><span class="sxs-lookup"><span data-stu-id="497f5-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="497f5-124">在節點上設定 [ **MF \_ TOPONODE \_ 轉換 \_ OBJECTID** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="497f5-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="497f5-125">屬性值是 CLSID。</span><span class="sxs-lookup"><span data-stu-id="497f5-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="497f5-126">呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。</span><span class="sxs-lookup"><span data-stu-id="497f5-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="497f5-127">下列範例會從 CLSID 建立和初始化轉換節點。</span><span class="sxs-lookup"><span data-stu-id="497f5-127">The following example creates and initializes a transform node from a CLSID.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="497f5-128">從啟用物件建立轉換節點</span><span class="sxs-lookup"><span data-stu-id="497f5-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="497f5-129">有些 MFTs 會提供啟用物件。</span><span class="sxs-lookup"><span data-stu-id="497f5-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="497f5-130">例如， [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 函式會傳回 WINDOWS MEDIA 音訊 (WMA) 編碼器的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="497f5-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="497f5-131">確切的函式取決於 MFT。</span><span class="sxs-lookup"><span data-stu-id="497f5-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="497f5-132">並非所有的 MFT 都提供啟用物件。</span><span class="sxs-lookup"><span data-stu-id="497f5-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="497f5-133">如需詳細資訊，請參閱 [啟用物件](activation-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="497f5-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="497f5-134">您也可以藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數來取得 MFT 啟用物件。</span><span class="sxs-lookup"><span data-stu-id="497f5-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="497f5-135">若要從啟用物件建立轉換節點，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="497f5-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="497f5-136">建立啟用物件，並取得啟用物件之 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="497f5-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="497f5-137">使用 [ **MF \_ 拓撲轉換] \_ \_ 節點** 旗標來呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立 [轉換] 節點。</span><span class="sxs-lookup"><span data-stu-id="497f5-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="497f5-138">呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。</span><span class="sxs-lookup"><span data-stu-id="497f5-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="497f5-139">呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。</span><span class="sxs-lookup"><span data-stu-id="497f5-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="497f5-140">下列範例會從啟用物件建立和初始化轉換節點。</span><span class="sxs-lookup"><span data-stu-id="497f5-140">The following example creates and initializes a transform node from an activation object.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="497f5-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="497f5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="497f5-142">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="497f5-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="497f5-143">拓撲</span><span class="sxs-lookup"><span data-stu-id="497f5-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="497f5-144">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="497f5-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



