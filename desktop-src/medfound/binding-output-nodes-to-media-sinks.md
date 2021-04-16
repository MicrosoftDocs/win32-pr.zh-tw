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
# <a name="binding-output-nodes-to-media-sinks"></a>將輸出節點系結至媒體接收

本主題描述如何在使用媒體會話之外的拓撲載入器時，初始化拓撲中的輸出節點。 輸出節點一開始會包含下列其中一項：

-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)指標。
-   [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標。

在後者的情況下，在拓撲載入器解析拓撲之前， [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標必須轉換成 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標。 在大部分的情況下，此程式的運作方式如下：

1.  應用程式會將部分拓撲排入媒體會話的佇列。
2.  針對所有輸出節點，媒體會話會將 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標轉換成 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標。 此 *進程稱為將* 輸出節點系結至媒體接收器。
3.  媒體會話會將修改過的拓撲傳送至 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法。

但是，如果您直接使用 (媒體會話) 之外的拓撲載入器，則您的應用程式必須在呼叫 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load)之前系結輸出節點。 若要系結輸出節點，請執行下列動作：

1.  呼叫 [**IMFTopologyNode：： GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) 以取得節點的物件指標。
2.  查詢 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的物件指標。 如果此呼叫成功，則不需要執行任何動作，因此請略過其餘的步驟。
3.  如果上一個步驟失敗，請查詢 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的物件指標。
4.  藉由呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)來建立媒體接收器。 指定 **IID \_ IMFMediaSink** 來取得媒體接收器的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面指標。
5.  查詢適用于 [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) 屬性的節點。 這個屬性的值是此節點之資料流程接收的識別碼。 如果未設定 **MF \_ TOPONODE \_ STREAMID** 屬性，則預設的資料流程識別碼為零。
6.  媒體接收上可能已存在適當的資料流程接收。 若要檢查，請在媒體接收器上呼叫 [**IMFMediaSink：： GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) 。 如果資料流程接收存在，此方法會傳回其 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的指標。 如果這個呼叫失敗，請嘗試呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink)來加入新的資料流程接收。 如果兩個呼叫都失敗，則表示媒體接收器不支援要求的資料流程識別碼，且此拓撲節點未正確設定。 傳回錯誤碼，並略過下一個步驟。
7.  呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject)，並傳入上一個步驟中的 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標。 此呼叫會取代節點的物件指標，讓節點包含資料流程接收的指標，而不是指向啟用物件的指標。

下列程式碼顯示如何系結輸出節點。


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
> 此範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。

 

下一個範例顯示如何在拓撲中系結所有輸出節點。 這個範例會使用 [**IMFTopology：： GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) 方法，從拓撲中取得輸出節點的集合。 然後，它會依序呼叫上述範例中的每個節點上所顯示的函式。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 拓朴建築](advanced-topology-building.md)
</dt> <dt>

[媒體接收器](media-sinks.md)
</dt> <dt>

[**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



