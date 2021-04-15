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
# <a name="creating-transform-nodes"></a>建立轉換節點

轉換節點代表媒體基礎轉換 (MFT) ，例如，解碼器或編碼器。 有幾種不同的方式可以初始化轉換節點：

-   從 MFT 的指標。
-   從 MFT 的 CLSID。
-   從 MFT 的啟用物件指標。

如果您要在受保護的媒體路徑中載入拓撲 (PMP) ，您必須使用 CLSID 或啟始物件，才能在受保護的進程內建立該 MFT。 使用 (的) 指標的第一種方法無法與 PMP 搭配使用。

## <a name="creating-a-transform-node-from-an-mft"></a>從 MFT 建立轉換節點

若要從 MFT 建立轉換節點，請執行下列動作：

1.  建立 MFT 的實例，並取得 MFT [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的指標。
2.  使用 [ **MF \_ 拓撲轉換] \_ \_ 節點** 旗標來呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立 [轉換] 節點。
3.  呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標。
4.  呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。

下列範例會從 MFT 建立和初始化轉換節點。


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



## <a name="creating-a-transform-node-from-a-clsid"></a>從 CLSID 建立轉換節點

若要從 CLSID 建立轉換節點，請執行下列動作：

1.  尋找 MFT 的 CLSID。 您可以使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函式，依類別（例如，解碼器或編碼器）來尋找 MFTs 的 clsid。 您也可以知道您想要使用的特定 MFT 的 CLSID (例如，如果您已執行自己的自訂 MFT) 。
2.  使用 [ **MF \_ 拓撲轉換] \_ \_ 節點** 旗標來呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立 [轉換] 節點。
3.  在節點上設定 [ **MF \_ TOPONODE \_ 轉換 \_ OBJECTID** ] 屬性。 屬性值是 CLSID。
4.  呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。

下列範例會從 CLSID 建立和初始化轉換節點。


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



## <a name="creating-a-transform-node-from-an-activation-object"></a>從啟用物件建立轉換節點

有些 MFTs 會提供啟用物件。 例如， [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 函式會傳回 WINDOWS MEDIA 音訊 (WMA) 編碼器的啟用物件。 確切的函式取決於 MFT。 並非所有的 MFT 都提供啟用物件。 如需詳細資訊，請參閱 [啟用物件](activation-objects.md)。

您也可以藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數來取得 MFT 啟用物件。

若要從啟用物件建立轉換節點，請執行下列動作：

1.  建立啟用物件，並取得啟用物件之 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。
2.  使用 [ **MF \_ 拓撲轉換] \_ \_ 節點** 旗標來呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立 [轉換] 節點。
3.  呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。
4.  呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。

下列範例會從啟用物件建立和初始化轉換節點。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立拓撲](creating-topologies.md)
</dt> <dt>

[拓撲](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



