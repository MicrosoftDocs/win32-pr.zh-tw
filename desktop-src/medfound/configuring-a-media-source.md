---
description: 設定媒體來源
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: 設定媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981938"
---
# <a name="configuring-a-media-source"></a><span data-ttu-id="ce960-103">設定媒體來源</span><span class="sxs-lookup"><span data-stu-id="ce960-103">Configuring a Media Source</span></span>

<span data-ttu-id="ce960-104">當您使用 [來源解析程式](source-resolver.md) 來建立媒體來源時，您可以指定包含設定屬性的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="ce960-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="ce960-105">這些屬性將用來初始化媒體來源。</span><span class="sxs-lookup"><span data-stu-id="ce960-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="ce960-106">一組支援的屬性取決於媒體來源的執行。</span><span class="sxs-lookup"><span data-stu-id="ce960-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="ce960-107">並非每個媒體來源都定義了設定屬性。</span><span class="sxs-lookup"><span data-stu-id="ce960-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="ce960-108">下表列出媒體基礎中提供之媒體來源的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="ce960-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="ce960-109">協力廠商媒體來源可以定義自己的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="ce960-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce960-110">媒體來源</span><span class="sxs-lookup"><span data-stu-id="ce960-110">Media source</span></span></th>
<th><span data-ttu-id="ce960-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ce960-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce960-112">網路來源</span><span class="sxs-lookup"><span data-stu-id="ce960-112">Network source</span></span></td>
<td><span data-ttu-id="ce960-113">請參閱 <a href="network-source-features.md">網路來源功能</a>。</span><span class="sxs-lookup"><span data-stu-id="ce960-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce960-114">ASF 媒體來源</span><span class="sxs-lookup"><span data-stu-id="ce960-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="ce960-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce960-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="ce960-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="ce960-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="ce960-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="ce960-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="ce960-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="ce960-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce960-119">若要設定來源，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ce960-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="ce960-120">呼叫 **PSCreateMemoryPropertyStore** 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="ce960-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="ce960-121">此函數會傳回 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="ce960-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="ce960-122">呼叫 **IPropertyStore：： SetValue** 可設定一或多個設定屬性。</span><span class="sxs-lookup"><span data-stu-id="ce960-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="ce960-123">呼叫其中一個來源解析程式的建立函數，例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)，然後在 *pProps* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="ce960-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="ce960-124">來源解析程式會將 **IPropertyStore** 指標直接傳遞至配置處理常式或建立來源的位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="ce960-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="ce960-125">來源解析程式不會嘗試驗證屬性。</span><span class="sxs-lookup"><span data-stu-id="ce960-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="ce960-126">一般而言，這些屬性會用於 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="ce960-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="ce960-127">如果您未提供內容存放區，媒體來源仍應正常運作，並使用預設設定。</span><span class="sxs-lookup"><span data-stu-id="ce960-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce960-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce960-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce960-129">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="ce960-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



