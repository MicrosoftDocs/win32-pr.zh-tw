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
# <a name="creating-output-nodes"></a>建立輸出節點

輸出節點表示媒體接收上的資料流程接收。 有兩種方式可以初始化輸出節點：

-   從資料流程接收的指標。
-   從媒體接收器的啟用物件指標。

如果您要在受保護的媒體路徑中載入拓撲 (PMP) ，您必須使用啟用物件，才能在受保護的進程內建立媒體接收器。 第一個方法 (使用串流接收器的指標) 無法與 PMP 搭配使用。

## <a name="creating-an-output-node-from-a-stream-sink"></a>從資料流程接收建立輸出節點

若要從資料流程接收建立輸出節點，請執行下列動作：

1.  建立媒體接收器的實例。
2.  使用媒體接收器的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面來取得所需資料流程接收的指標。  (**IMFMediaSink** 介面具有數個傳回資料流程接收指標的方法。 ) 
3.  使用 **MF \_ 拓撲 \_ 輸出 \_ 節點** 旗標呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立輸出節點。
4.  呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入串流接收器 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的指標。
5.  將 [移除] 屬性上的 [ [**MF \_ TOPONODE \_ NOSHUTDOWN \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) ] 設定為 [ **FALSE** ] (選擇性，但建議使用) 。
6.  呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。

下列範例會從資料流程接收中建立並初始化輸出節點。


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



當應用程式關閉媒體會話時，媒體會話會自動關閉媒體接收器。 因此，您無法重複使用媒體接收器與另一個媒體會話實例。

## <a name="creating-an-output-node-from-an-activation-object"></a>從啟用物件建立輸出節點

任何信任的媒體接收器都必須提供啟用物件，才能在受保護的進程內建立媒體接收器。 如需詳細資訊，請參閱 [啟用物件](activation-objects.md)。 建立啟用物件的特定函式將取決於媒體接收器。

若要從啟用物件建立輸出節點，請執行下列動作：

1.  建立啟用物件，並取得啟用物件之 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。
2.  使用 **MF \_ 拓撲 \_ 輸出 \_ 節點** 旗標呼叫 [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) ，以建立輸出節點。
3.  （選擇性）在節點上設定 [ [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) ] 屬性，以指定資料流程接收的資料流程識別碼。 如果您省略此屬性，節點會預設為使用串流接收器0。
4.  將 [移除] 屬性上的 [ [**MF \_ TOPONODE \_ NOSHUTDOWN \_ \_**](mf-toponode-noshutdown-on-remove-attribute.md) ] 設定為 [ **TRUE** ] (選擇性，但建議使用) 。
5.  呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) ，並傳入 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。
6.  呼叫 [**IMFTopology：： AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) ，將節點加入至拓撲。

下列範例會從啟用物件建立和初始化輸出節點。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[建立拓撲](creating-topologies.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> <dt>

[拓撲](topologies.md)
</dt> </dl>

 

 



