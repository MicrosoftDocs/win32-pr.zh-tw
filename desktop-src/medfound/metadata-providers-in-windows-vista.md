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
# <a name="metadata-providers-in-windows-vista"></a>Windows Vista 中的中繼資料提供者

在 Windows Vista 中，Microsoft 媒體基礎會透過 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面公開中繼資料。

## <a name="reading-metadata"></a>讀取中繼資料

若要從媒體來源讀取中繼資料，請執行下列步驟：

1.  取得媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。 您可以使用 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面來取得 **IMFMediaSource** 指標。
2.  呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 以取得媒體來源的展示描述項。
3.  呼叫媒體來源上的 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以取得 [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) 介面的指標。 在 **MFGetService** 的 *guidService* 參數中，指定值 **MF \_ 中繼資料 \_ 提供者 \_ 服務**。 如果來源不支援 **IMFMetadataProvider** 介面， **MFGetService** 會傳回 **MF \_ E \_ 不受支援的 \_ 服務**。
4.  呼叫 [**IMFMetadataProvider：： GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) ，並傳入表示描述項的指標。 這個方法會傳回 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) 介面的指標。
    -   若要取得資料流程層級的中繼資料，請先呼叫 [**IMFStreamDescriptor：： GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) 來取得資料流程識別碼。 然後，在 [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata)的 *dwStreamIdentifier* 參數中傳遞資料流程識別碼。
    -   若要取得簡報層級的中繼資料，請將 *dwStreamIdentifier* 設定為零。
5.  \[選擇性 \] 呼叫 [**IMFMetadata：： GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) ，取得可用中繼資料的語言清單。 語言是使用符合 RFC 1766 標準的語言標記來識別。
6.  \[選擇性 \] 呼叫 [**IMFMetadata：： SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) 來選取語言。
7.  \[選擇性 \] 呼叫 [**IMFMetadata：： GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) ，以取得此資料流程或簡報的所有中繼資料屬性名稱清單。
8.  呼叫 [**IMFMetadata：： GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) ，以取得特定的中繼資料屬性值，並傳入屬性的名稱。

下列程式碼顯示步驟2–4：


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



下列程式碼顯示步驟7–8。 假設 `DisplayProperty` 是一個會顯示 **PROPVARIANT** 值的函式。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體中繼資料](media-metadata.md)
</dt> <dt>

[Shell 中繼資料提供者](shell-metadata-providers.md)
</dt> </dl>

 

 



