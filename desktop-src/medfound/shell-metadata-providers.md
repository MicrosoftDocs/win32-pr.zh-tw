---
description: 從 Windows 7 開始，Microsoft 媒體基礎會透過 IPropertyStore 介面公開中繼資料。
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Shell 中繼資料提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31960ed41743a86b62b63555236d2876166a14b098f0692f3d6cb22b051e338e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713358"
---
# <a name="shell-metadata-providers"></a>Shell 中繼資料提供者

從 Windows 7 開始，Microsoft 媒體基礎會透過 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)介面公開中繼資料。

使用本主題中定義的程式所取得的中繼資料，應該僅用於唯讀存取。 不支援使用此進程寫入資料。 您可以使用) 從 [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid)取得 (CLSID 的類別識別碼，來建立 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)物件以供撰寫之用。

## <a name="reading-metadata"></a>讀取中繼資料

若要從媒體來源讀取中繼資料，請執行下列步驟：

1.  取得媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。 您可以使用 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面來取得 **IMFMediaSource** 指標。
2.  呼叫媒體來源上的 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以取得 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的指標。 在 **MFGetService** 的 *guidService* 參數中，指定值 **MF \_ 屬性 \_ 處理常式 \_ 服務**。 如果來源不支援 **IPropertyStore** 介面， **MFGetService** 會傳回 **MF \_ E \_ 不受支援的 \_ 服務**。
3.  呼叫 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 方法來列舉中繼資料屬性。

下列程式碼顯示這些步驟。 假設 `DisplayProperty` 是一個會顯示 **PROPVARIANT** 值的函式。


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



如需中繼資料屬性索引鍵的清單，請參閱媒體檔案的 [中繼資料屬性](metadata-properties-for-media-files.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體中繼資料](media-metadata.md)
</dt> </dl>

 

 
