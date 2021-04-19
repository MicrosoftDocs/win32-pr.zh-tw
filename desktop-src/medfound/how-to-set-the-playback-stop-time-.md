---
description: 本主題說明如何設定在使用媒體會話時播放的停止時間。
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: 如何設定播放停止時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979027"
---
# <a name="how-to-set-the-playback-stop-time"></a>如何設定播放停止時間

本主題說明如何設定在使用 [媒體會話](media-session.md)時播放的停止時間。

## <a name="setting-the-stop-time-before-playback-begins"></a>設定播放開始之前的停止時間

將拓撲排在佇列以供播放之前，您可以使用 [ [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) ] 屬性來指定停止時間。 針對拓撲中的每個輸出節點，將 MF TOPONODE MEDIASTOP 的值設定 \_ \_ 為 100-毫微秒單位的停止時間。

請注意，在播放開始之後設定這個屬性不會有任何作用。 因此，在呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)之前，請先設定屬性。

下列程式碼示範如何設定現有拓撲的停止時間。


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a>在播放開始之後設定停止時間

有一種方法可以使用 [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)介面，在 [媒體會話](media-session.md)開始播放之後設定停止時間。

> [!IMPORTANT]
> 此介面有嚴重的限制，因為停止時間指定為32位值。 這表示您可以使用這個介面設定的最大停止時間為0xFFFFFFFF，或只在7分鐘內。 這項限制是因為結構定義不正確所致。

 

若要使用 [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) 介面設定停止時間，請執行下列步驟。

1.  呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 以從媒體會話取得 [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) 介面。
2.  呼叫 [**IMFTopology：： GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) 來取得播放拓撲的識別碼。
3.  針對拓撲中的每個輸出節點，呼叫 [**IMFTopologyNodeAttributeEditor：： UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes)。 這個方法會接受拓撲識別碼和指向 [**MFTOPONODE \_ 屬性 \_ 更新**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) 結構的指標。 初始化結構，如下所示。

    | 成員               | 值                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | 節點 ID。 若要取得節點識別碼，請呼叫呼叫 [**IMFTopologyNode：： GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid)。 |
    | **guidAttributeKey** | **MF \_ TOPONODE \_ MEDIASTOP**                                                                                         |
    | **attrType**         | **MF \_ 屬性 \_ UINT64**                                                                                           |
    | **u64**              | 停止時間，以 100-毫微秒單位表示。                                                                             |

    

     

請小心設定正確的 **attrType** 值。 雖然 **u64** 是32位類型，但該方法需要將 **AttrType** 設定為 **MF \_ 屬性 \_ UINT64**。

下列程式碼顯示這些步驟。


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> </dl>

 

 



