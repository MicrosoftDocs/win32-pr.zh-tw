---
description: 從 Windows 7 開始，Microsoft 媒體基礎會透過 IPropertyStore 介面公開中繼資料。
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Shell 中繼資料提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998262"
---
# <a name="shell-metadata-providers"></a><span data-ttu-id="9be8c-103">Shell 中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="9be8c-103">Shell Metadata Providers</span></span>

<span data-ttu-id="9be8c-104">從 Windows 7 開始，Microsoft 媒體基礎會透過 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面公開中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9be8c-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="9be8c-105">使用本主題中定義的程式所取得的中繼資料，應該僅用於唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="9be8c-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="9be8c-106">不支援使用此進程寫入資料。</span><span class="sxs-lookup"><span data-stu-id="9be8c-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="9be8c-107">您可以使用) 從 [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid)取得 (CLSID 的類別識別碼，來建立 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)物件以供撰寫之用。</span><span class="sxs-lookup"><span data-stu-id="9be8c-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="9be8c-108">讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="9be8c-108">Reading Metadata</span></span>

<span data-ttu-id="9be8c-109">若要從媒體來源讀取中繼資料，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9be8c-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="9be8c-110">取得媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9be8c-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="9be8c-111">您可以使用 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面來取得 **IMFMediaSource** 指標。</span><span class="sxs-lookup"><span data-stu-id="9be8c-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="9be8c-112">呼叫媒體來源上的 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以取得 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9be8c-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="9be8c-113">在 **MFGetService** 的 *guidService* 參數中，指定值 **MF \_ 屬性 \_ 處理常式 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="9be8c-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="9be8c-114">如果來源不支援 **IPropertyStore** 介面， **MFGetService** 會傳回 **MF \_ E \_ 不受支援的 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="9be8c-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="9be8c-115">呼叫 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 方法來列舉中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="9be8c-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="9be8c-116">下列程式碼顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="9be8c-116">The following code shows these steps.</span></span> <span data-ttu-id="9be8c-117">假設 `DisplayProperty` 是一個會顯示 **PROPVARIANT** 值的函式。</span><span class="sxs-lookup"><span data-stu-id="9be8c-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



<span data-ttu-id="9be8c-118">如需中繼資料屬性索引鍵的清單，請參閱媒體檔案的 [中繼資料屬性](metadata-properties-for-media-files.md)。</span><span class="sxs-lookup"><span data-stu-id="9be8c-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9be8c-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9be8c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9be8c-120">媒體中繼資料</span><span class="sxs-lookup"><span data-stu-id="9be8c-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
