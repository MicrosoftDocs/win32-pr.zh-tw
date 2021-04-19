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
# <a name="creating-source-nodes"></a>建立來源節點

來源節點代表來自媒體來源的一個資料流程。 來源節點必須包含媒體來源、簡報描述元和資料流程描述項的指標。

若要將來源節點新增至拓撲，請執行下列動作：

1.  使用 **MF \_ 拓撲 \_ SOURCESTREAM \_ 節點** 旗標呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立來源節點。
2.  使用媒體來源的指標，在節點上設定 [ [**MF \_ TOPONODE \_ 來源**](mf-toponode-source-attribute.md) ] 屬性。
3.  使用媒體來源之呈現描述項的指標，在節點上設定 [ [**MF \_ TOPONODE \_ 展示 \_ 描述**](mf-toponode-presentation-descriptor-attribute.md) 項] 屬性。
4.  使用資料流程的資料流程描述元指標，在節點上設定 [ [**MF \_ TOPONODE \_ 資料流程 \_ 描述**](mf-toponode-stream-descriptor-attribute.md) 元] 屬性。
5.  呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。

下列範例會建立並初始化來源節點。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立拓撲](creating-topologies.md)
</dt> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[拓撲](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



