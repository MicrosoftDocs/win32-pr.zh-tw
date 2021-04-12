---
description: 使用來源解析程式
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: 使用來源解析程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192151"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="82456-103">使用來源解析程式</span><span class="sxs-lookup"><span data-stu-id="82456-103">Using the Source Resolver</span></span>

<span data-ttu-id="82456-104">來源解析程式會接受 URL 或位元組資料流，然後為該內容建立適當的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="82456-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="82456-105">若要建立來源解析程式，請呼叫 [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)。</span><span class="sxs-lookup"><span data-stu-id="82456-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="82456-106">此函數會傳回 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="82456-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="82456-107">來源解析程式具有同步和非同步方法。</span><span class="sxs-lookup"><span data-stu-id="82456-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="82456-108">如果您是從主應用程式執行緒使用來源解析程式，則非同步方法會讓您的使用者介面更具回應性。</span><span class="sxs-lookup"><span data-stu-id="82456-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="82456-109">同步方法可以封鎖相當長的時間，特別是當來源解析程式必須開啟網路資源時。</span><span class="sxs-lookup"><span data-stu-id="82456-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="82456-110">同步方法如下：</span><span class="sxs-lookup"><span data-stu-id="82456-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="82456-111">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="82456-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="82456-112">**IMFSourceResolver::CreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="82456-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="82456-113">非同步方法如下：</span><span class="sxs-lookup"><span data-stu-id="82456-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="82456-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="82456-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="82456-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="82456-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="82456-116">在非同步方法中，每個方法都有對應的 **End ...** 方法來完成非同步要求， **以及解除擱置** 的要求。</span><span class="sxs-lookup"><span data-stu-id="82456-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="82456-117">如需媒體基礎中非同步方法的詳細資訊，請參閱 [非同步回呼方法](asynchronous-callback-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="82456-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="82456-118">下列程式碼範例會從 URL 建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="82456-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="82456-119">這個範例會使用同步方法。</span><span class="sxs-lookup"><span data-stu-id="82456-119">This example uses the synchronous method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="82456-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="82456-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82456-121">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="82456-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



