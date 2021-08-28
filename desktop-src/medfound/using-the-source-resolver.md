---
description: 使用來源解析程式
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: 使用來源解析程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81265f2edeb573ccdfb2b4ea8f2664d08f9bca8a2170459c9c53890ecd3b52cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887141"
---
# <a name="using-the-source-resolver"></a>使用來源解析程式

來源解析程式會接受 URL 或位元組資料流，然後為該內容建立適當的媒體來源。 若要建立來源解析程式，請呼叫 [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)。 此函數會傳回 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面指標。

來源解析程式具有同步和非同步方法。 如果您是從主應用程式執行緒使用來源解析程式，則非同步方法會讓您的使用者介面更具回應性。 同步方法可以封鎖相當長的時間，特別是當來源解析程式必須開啟網路資源時。

同步方法如下：

-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

非同步方法如下：

-   [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

在非同步方法中，每個方法都有對應的 **End ...** 方法來完成非同步要求， **以及解除擱置** 的要求。 如需媒體基礎中非同步方法的詳細資訊，請參閱 [非同步回呼方法](asynchronous-callback-methods.md)。

下列程式碼範例會從 URL 建立媒體來源。 這個範例會使用同步方法。


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源解析程式](source-resolver.md)
</dt> </dl>

 

 



