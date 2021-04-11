---
description: ASF 檔案接收是媒體基礎所提供的 IMFMediaSink，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收物件模型和一般使用方式的相關資訊，請參閱 ASF 媒體接收器。
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: 將中繼資料新增至 File 接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bb63a10d935b52e6d048dbc5dcd07370dd2ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026265"
---
# <a name="adding-metadata-to-the-file-sink"></a><span data-ttu-id="fb8ea-104">將中繼資料新增至 File 接收器</span><span class="sxs-lookup"><span data-stu-id="fb8ea-104">Adding Metadata to the File Sink</span></span>

<span data-ttu-id="fb8ea-105">ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="fb8ea-106">如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="fb8ea-107">[建立 ASF 檔案接收](creating-the-asf-file-sink.md)之後，必須使用輸出檔中的資料流程和編碼資訊來設定其相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-107">After [Creating the ASF file sink](creating-the-asf-file-sink.md), it must be configured with information about the streams and encoding information in the output file.</span></span> <span data-ttu-id="fb8ea-108">這些程式會在 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md) ，以及在檔案 [接收中設定屬性](setting-properties-in-the-file-sink.md)時說明。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-108">These procedures are described in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md) and [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span> <span data-ttu-id="fb8ea-109">此外，您也可以加入中繼資料資訊，包括名稱/值組，例如 "Author"、Title "。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-109">In addition, You can also add metadata information includes name/value pairs such as "Author", Title".</span></span> <span data-ttu-id="fb8ea-110">本主題說明將中繼資料資訊新增至檔案接收的程式，使其出現在最後一個 [ASF 標頭物件](asf-file-structure.md)中。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-110">This topic describes the process of adding metadata information to the file sink so that it appears in the final [ASF Header Object](asf-file-structure.md).</span></span>

<span data-ttu-id="fb8ea-111">您可以在建立編碼拓撲之前，將中繼資料資訊新增至 ASF 檔案接收。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-111">You can add metadata information to the ASF file sink before building the encoding topology.</span></span> <span data-ttu-id="fb8ea-112">File 接收的 ASF ContentInfo 物件會追蹤中繼資料屬性，並透過 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-112">The ASF ContentInfo object for the file sink keeps track of the metadata properties and are exposed to the application through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span> <span data-ttu-id="fb8ea-113">其中有些屬性（例如 "IsVBR"）會指出檔案是否包含變數位元速率 (VBR) 資料流程，藉由剖析已設定的資料流程編碼屬性，檔案接收會自動設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-113">Some of these properties, such as "IsVBR" that indicates if the file contains variable bit rate (VBR) streams, are set automatically by the file sink by parsing the stream encoding properties that are set.</span></span>

<span data-ttu-id="fb8ea-114">如需屬性的完整清單，請參閱格式 SDK 檔中的「屬性清單」主題。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-114">For a complete list of properties, see the "Attribute List" topic in the Format SDK documentation.</span></span>

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a><span data-ttu-id="fb8ea-115">在 ASF File 接收器上使用 IMFMetadata 介面</span><span class="sxs-lookup"><span data-stu-id="fb8ea-115">Using the IMFMetadata Interface on the ASF File Sink</span></span>

1.  <span data-ttu-id="fb8ea-116">查詢 ASF 檔接收物件，以取得其 [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) 介面的實作為指標。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-116">Query the ASF file sink object to get a pointer to its implementation of the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span>
2.  <span data-ttu-id="fb8ea-117">呼叫 [**IMFMetadataProvider：： GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) 來取得 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 指標。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-117">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) to get an [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) pointer.</span></span>

    <span data-ttu-id="fb8ea-118">*PPresentationDescriptor* 參數會被忽略，而且應用程式可以傳遞 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-118">The *pPresentationDescriptor* parameter is ignored and the application can pass **NULL**.</span></span> <span data-ttu-id="fb8ea-119">如果應用程式在 *dwStreamIdentifier* 參數中傳遞零做為資料流程識別碼，此方法就會取出適用于整個 ASF 檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-119">If the application passes zero as the stream identifier in the *dwStreamIdentifier* parameter, the method retrieves metadata that applies to the entire ASF file.</span></span> <span data-ttu-id="fb8ea-120">否則，只會取出資料流程的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-120">Otherwise, only the metadata for the stream is retrieved.</span></span>

3.  <span data-ttu-id="fb8ea-121">呼叫 [**IMFMetadata：： GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) ，以取得媒體內容上設定的檔案編碼屬性清單。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-121">Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to retrieve the list of file-encoding properties set on the media content.</span></span>
4.  <span data-ttu-id="fb8ea-122">呼叫 [**IMFMetadata：： GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) 來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get the property values.</span></span>

## <a name="example"></a><span data-ttu-id="fb8ea-123">範例</span><span class="sxs-lookup"><span data-stu-id="fb8ea-123">Example</span></span>

<span data-ttu-id="fb8ea-124">下列範例程式碼顯示如何列舉在 ASF 檔案上設定的屬性名稱和值。</span><span class="sxs-lookup"><span data-stu-id="fb8ea-124">The following example code shows how to enumerate the property names and values that are set on the ASF file.</span></span>


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fb8ea-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb8ea-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb8ea-126">ASF 媒體接收</span><span class="sxs-lookup"><span data-stu-id="fb8ea-126">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="fb8ea-127">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="fb8ea-127">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="fb8ea-128">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="fb8ea-128">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



