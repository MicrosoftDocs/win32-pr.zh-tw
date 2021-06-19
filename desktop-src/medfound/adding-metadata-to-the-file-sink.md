---
description: 瞭解如何將中繼資料新增至 ASF 檔案接收，應用程式可以使用它將 ASF 媒體資料封存至檔案。
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: 將中繼資料新增至 File 接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ea86a09ff9e3d2a25bbf8d00d46691fd803365
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409961"
---
# <a name="adding-metadata-to-the-file-sink"></a>將中繼資料新增至 File 接收器

ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。 如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。

[建立 ASF 檔案接收](creating-the-asf-file-sink.md)之後，必須使用輸出檔中的資料流程和編碼資訊來設定其相關資訊。 這些程式會在 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md) ，以及在檔案 [接收中設定屬性](setting-properties-in-the-file-sink.md)時說明。 此外，您也可以加入中繼資料資訊，包括名稱/值組，例如 "Author"、Title "。 本主題說明將中繼資料資訊新增至檔案接收的程式，使其出現在最後一個 [ASF 標頭物件](asf-file-structure.md)中。

您可以在建立編碼拓撲之前，將中繼資料資訊新增至 ASF 檔案接收。 File 接收的 ASF ContentInfo 物件會追蹤中繼資料屬性，並透過 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面公開給應用程式。 其中有些屬性（例如 "IsVBR"）會指出檔案是否包含變數位元速率 (VBR) 資料流程，藉由剖析已設定的資料流程編碼屬性，檔案接收會自動設定這些屬性。

如需屬性的完整清單，請參閱格式 SDK 檔中的「屬性清單」主題。

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>在 ASF File 接收器上使用 IMFMetadata 介面

1.  查詢 ASF 檔接收物件，以取得其 [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) 介面的實作為指標。
2.  呼叫 [**IMFMetadataProvider：： GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) 來取得 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 指標。

    *PPresentationDescriptor* 參數會被忽略，而且應用程式可以傳遞 **Null**。 如果應用程式在 *dwStreamIdentifier* 參數中傳遞零做為資料流程識別碼，此方法就會取出適用于整個 ASF 檔案的中繼資料。 否則，只會取出資料流程的中繼資料。

3.  呼叫 [**IMFMetadata：： GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) ，以取得媒體內容上設定的檔案編碼屬性清單。
4.  呼叫 [**IMFMetadata：： GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) 來取得屬性值。

## <a name="example"></a>範例

下列範例程式碼顯示如何列舉在 ASF 檔案上設定的屬性名稱和值。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 媒體接收](asf-media-sinks.md)
</dt> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



