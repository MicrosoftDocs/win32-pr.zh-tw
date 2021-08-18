---
description: 選擇壓縮篩選
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: 選擇壓縮篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf964aa3647086efe569263e5fb36b4e0db60ebfad73c9d2fe9dcb14f3bcf125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999218"
---
# <a name="choosing-a-compression-filter"></a>選擇壓縮篩選

有數種類型的軟體元件可以執行影片或音訊壓縮，例如：

-   原生 DirectShow 篩選
-   影片壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器
-   音訊壓縮管理員 (的) 編解碼器
-   DirectX 媒體物件 (DMOs) 

在 DirectShow 中，bc-vcm-lvm-hyperv 編解碼器是由[AVI 壓縮程式篩選器](avi-compressor-filter.md)包裝，而使用的編解碼器會由「通過」包裝函式[篩選器](acm-wrapper-filter.md)包裝。 DMOs 是以[DMO 包裝函式篩選器](dmo-wrapper-filter.md)包裝。 系統裝置列舉值可提供一致的方式來列舉和建立任何這些壓縮程式類型，而不需擔心基礎模型。

如需系統裝置列舉值的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。 簡單地說，所有 DirectShow 篩選準則都會依類別分類，而且每個類別都是由 GUID 所識別。 針對影片壓縮機，類別目錄 GUID 是 CLSID \_ VideoCompressorCategory。 針對音訊壓縮機，它是 CLSID \_ AudioCompressorCategory。 為了列舉特定的類別，系統裝置列舉值會建立支援 [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker)介面的 *列舉* 值物件。 應用程式會使用此介面來抓取裝置的名字標記，其中每個裝置的標記都代表 DirectShow 篩選準則的實例。 您可以使用「標記」來建立篩選，或在不建立篩選的情況下取得裝置的易記名稱。

若要列舉使用者系統上的可用影片或音訊壓縮機，請執行下列動作：

1.  呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立具有 CLSID SYSTEMDEVICEENUM 類別識別碼的系統裝置枚舉器 \_ 。
2.  使用篩選準則分類 GUID 呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 。 方法會傳回 **IEnumMoniker** 介面指標。
3.  使用 IEnumMoniker：： Next 方法來列舉裝置的名字標記。 這個方法會傳回代表標記的 [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) 介面。

若要從標記取得易記名稱，請執行下列動作：

1.  呼叫 **IMoniker：： BindToStorage** 方法。 這個方法會傳回 **IPropertyBag** 介面指標。
2.  使用 **IPropertyBag：： read** 方法讀取 **FriendlyName** 屬性。

一般而言，應用程式會顯示壓縮機清單，讓使用者可以選擇一個。 例如，下列程式碼會在清單方塊中填入可用影片壓縮機的名稱。


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



若要從標記建立篩選準則實例，請呼叫 **IMoniker：： BindToObject** 方法。 方法會傳回 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



針對 BC-VCM-LVM-HYPERV 編解碼器，每個標記都代表一個特定的編解碼器，即使所有編解碼器都是由相同的 AVI 壓縮篩選器所包裝也一樣。 呼叫 **BindToObject** 會建立此篩選準則的實例，並針對該編解碼器進行初始化。 基於這個理由，您無法直接在 AVI 壓縮篩選器上呼叫 **CoCreateInstance** 。 您必須經過系統裝置枚舉器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Recompressing AVI 檔案](recompressing-an-avi-file.md)
</dt> </dl>

 

 
