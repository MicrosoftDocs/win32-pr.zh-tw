---
description: 在 Windows Vista 中，Microsoft 媒體基礎會透過 IMFMetadata 介面公開中繼資料。
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Windows Vista 中的中繼資料提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970220"
---
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="f2393-103">Windows Vista 中的中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="f2393-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="f2393-104">在 Windows Vista 中，Microsoft 媒體基礎會透過 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面公開中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f2393-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="f2393-105">讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="f2393-105">Reading Metadata</span></span>

<span data-ttu-id="f2393-106">若要從媒體來源讀取中繼資料，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f2393-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="f2393-107">取得媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f2393-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="f2393-108">您可以使用 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面來取得 **IMFMediaSource** 指標。</span><span class="sxs-lookup"><span data-stu-id="f2393-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="f2393-109">呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 以取得媒體來源的展示描述項。</span><span class="sxs-lookup"><span data-stu-id="f2393-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="f2393-110">呼叫媒體來源上的 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以取得 [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f2393-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="f2393-111">在 **MFGetService** 的 *guidService* 參數中，指定值 **MF \_ 中繼資料 \_ 提供者 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="f2393-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="f2393-112">如果來源不支援 **IMFMetadataProvider** 介面， **MFGetService** 會傳回 **MF \_ E \_ 不受支援的 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="f2393-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="f2393-113">呼叫 [**IMFMetadataProvider：： GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) ，並傳入表示描述項的指標。</span><span class="sxs-lookup"><span data-stu-id="f2393-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="f2393-114">這個方法會傳回 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f2393-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="f2393-115">若要取得資料流程層級的中繼資料，請先呼叫 [**IMFStreamDescriptor：： GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) 來取得資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2393-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="f2393-116">然後，在 [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata)的 *dwStreamIdentifier* 參數中傳遞資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2393-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="f2393-117">若要取得簡報層級的中繼資料，請將 *dwStreamIdentifier* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="f2393-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="f2393-118">\[選擇性 \] 呼叫 [**IMFMetadata：： GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) ，取得可用中繼資料的語言清單。</span><span class="sxs-lookup"><span data-stu-id="f2393-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="f2393-119">語言是使用符合 RFC 1766 標準的語言標記來識別。</span><span class="sxs-lookup"><span data-stu-id="f2393-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="f2393-120">\[選擇性 \] 呼叫 [**IMFMetadata：： SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) 來選取語言。</span><span class="sxs-lookup"><span data-stu-id="f2393-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="f2393-121">\[選擇性 \] 呼叫 [**IMFMetadata：： GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) ，以取得此資料流程或簡報的所有中繼資料屬性名稱清單。</span><span class="sxs-lookup"><span data-stu-id="f2393-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="f2393-122">呼叫 [**IMFMetadata：： GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) ，以取得特定的中繼資料屬性值，並傳入屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2393-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="f2393-123">下列程式碼顯示步驟2–4：</span><span class="sxs-lookup"><span data-stu-id="f2393-123">The following code shows steps 2–4:</span></span>


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



<span data-ttu-id="f2393-124">下列程式碼顯示步驟7–8。</span><span class="sxs-lookup"><span data-stu-id="f2393-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="f2393-125">假設 `DisplayProperty` 是一個會顯示 **PROPVARIANT** 值的函式。</span><span class="sxs-lookup"><span data-stu-id="f2393-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f2393-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2393-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2393-127">媒體中繼資料</span><span class="sxs-lookup"><span data-stu-id="f2393-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="f2393-128">Shell 中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="f2393-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



