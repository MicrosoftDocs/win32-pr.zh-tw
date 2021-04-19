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
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="85be2-103">如何設定播放停止時間</span><span class="sxs-lookup"><span data-stu-id="85be2-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="85be2-104">本主題說明如何設定在使用 [媒體會話](media-session.md)時播放的停止時間。</span><span class="sxs-lookup"><span data-stu-id="85be2-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="85be2-105">設定播放開始之前的停止時間</span><span class="sxs-lookup"><span data-stu-id="85be2-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="85be2-106">將拓撲排在佇列以供播放之前，您可以使用 [ [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) ] 屬性來指定停止時間。</span><span class="sxs-lookup"><span data-stu-id="85be2-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="85be2-107">針對拓撲中的每個輸出節點，將 MF TOPONODE MEDIASTOP 的值設定 \_ \_ 為 100-毫微秒單位的停止時間。</span><span class="sxs-lookup"><span data-stu-id="85be2-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="85be2-108">請注意，在播放開始之後設定這個屬性不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="85be2-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="85be2-109">因此，在呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="85be2-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="85be2-110">下列程式碼示範如何設定現有拓撲的停止時間。</span><span class="sxs-lookup"><span data-stu-id="85be2-110">The following code shows how to set the stop time on an existing topology.</span></span>


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



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="85be2-111">在播放開始之後設定停止時間</span><span class="sxs-lookup"><span data-stu-id="85be2-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="85be2-112">有一種方法可以使用 [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)介面，在 [媒體會話](media-session.md)開始播放之後設定停止時間。</span><span class="sxs-lookup"><span data-stu-id="85be2-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85be2-113">此介面有嚴重的限制，因為停止時間指定為32位值。</span><span class="sxs-lookup"><span data-stu-id="85be2-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="85be2-114">這表示您可以使用這個介面設定的最大停止時間為0xFFFFFFFF，或只在7分鐘內。</span><span class="sxs-lookup"><span data-stu-id="85be2-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="85be2-115">這項限制是因為結構定義不正確所致。</span><span class="sxs-lookup"><span data-stu-id="85be2-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="85be2-116">若要使用 [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) 介面設定停止時間，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="85be2-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="85be2-117">呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 以從媒體會話取得 [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) 介面。</span><span class="sxs-lookup"><span data-stu-id="85be2-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="85be2-118">呼叫 [**IMFTopology：： GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) 來取得播放拓撲的識別碼。</span><span class="sxs-lookup"><span data-stu-id="85be2-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="85be2-119">針對拓撲中的每個輸出節點，呼叫 [**IMFTopologyNodeAttributeEditor：： UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes)。</span><span class="sxs-lookup"><span data-stu-id="85be2-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="85be2-120">這個方法會接受拓撲識別碼和指向 [**MFTOPONODE \_ 屬性 \_ 更新**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="85be2-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="85be2-121">初始化結構，如下所示。</span><span class="sxs-lookup"><span data-stu-id="85be2-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="85be2-122">成員</span><span class="sxs-lookup"><span data-stu-id="85be2-122">Member</span></span>               | <span data-ttu-id="85be2-123">值</span><span class="sxs-lookup"><span data-stu-id="85be2-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="85be2-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="85be2-124">**NodeId**</span></span>           | <span data-ttu-id="85be2-125">節點 ID。</span><span class="sxs-lookup"><span data-stu-id="85be2-125">The node ID.</span></span> <span data-ttu-id="85be2-126">若要取得節點識別碼，請呼叫呼叫 [**IMFTopologyNode：： GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid)。</span><span class="sxs-lookup"><span data-stu-id="85be2-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="85be2-127">**guidAttributeKey**</span><span class="sxs-lookup"><span data-stu-id="85be2-127">**guidAttributeKey**</span></span> | <span data-ttu-id="85be2-128">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="85be2-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="85be2-129">**attrType**</span><span class="sxs-lookup"><span data-stu-id="85be2-129">**attrType**</span></span>         | <span data-ttu-id="85be2-130">**MF \_ 屬性 \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="85be2-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="85be2-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="85be2-131">**u64**</span></span>              | <span data-ttu-id="85be2-132">停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="85be2-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="85be2-133">請小心設定正確的 **attrType** 值。</span><span class="sxs-lookup"><span data-stu-id="85be2-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="85be2-134">雖然 **u64** 是32位類型，但該方法需要將 **AttrType** 設定為 **MF \_ 屬性 \_ UINT64**。</span><span class="sxs-lookup"><span data-stu-id="85be2-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="85be2-135">下列程式碼顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="85be2-135">The following code shows these steps.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="85be2-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="85be2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85be2-137">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="85be2-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



