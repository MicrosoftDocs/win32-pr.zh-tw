---
description: 選取捕獲裝置
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: 選取捕獲裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970885"
---
# <a name="selecting-a-capture-device"></a>選取捕獲裝置

若要選取音訊或影片捕獲裝置，請使用 [系統裝置列舉](system-device-enumerator.md)值，如 [使用系統裝置列舉](using-the-system-device-enumerator.md)值的主題所述。 系統裝置列舉值會傳回裝置類別目錄的集合，該集合是由裝置類別所選取。 *標記* 是包含另一個物件相關資訊的 COM 物件。 標記可讓應用程式取得物件的相關資訊，而不需要實際建立物件。 之後，應用程式可以使用此標記來建立物件。 如需有關別名的詳細資訊，請參閱 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)的檔。

若要使用系統裝置列舉值，請執行下列步驟。

1.  呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立系統裝置列舉值的實例。
2.  呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) ，並將裝置類別指定為 GUID。 針對 capture 裝置，下列類別是相關的。 

    | 類別 GUID                       | Description           |
    |-------------------------------------|-----------------------|
    | **CLSID \_ AudioInputDeviceCategory** | 音訊捕獲裝置 |
    | **CLSID \_ VideoInputDeviceCategory** | 影片捕獲裝置 |

    

     

    如果攝影機有整合式麥克風，則會同時出現在這兩個類別中。 不過，系統會將相機和麥克風視為個別的裝置，以供列舉、裝置建立和資料串流之用。

3.  [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator)方法會傳回 [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker)介面的指標。 若要列舉名字，請呼叫 [**IEnumMoniker：： Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next)。

下列程式碼會建立指定裝置類別的列舉值。


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



[**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker)介面會列舉 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)介面的清單，每個介面都代表一個裝置的標記。 應用程式可以從標記讀取屬性，或使用此標記來建立裝置的 DirectShow 捕獲篩選。 會以 **變異** 值的形式傳回「標記」屬性。 裝置的名字標記支援下列屬性。



| 屬性       | 描述                                                               | VARIANT 型別 |
|----------------|---------------------------------------------------------------------------|--------------|
| 友好 | 裝置的名稱。                                                   | **VT \_ BSTR** |
| 產品介紹  | 裝置的描述。                                              | **VT \_ BSTR** |
| DevicePath   | 識別裝置的唯一字串。 僅 (影片捕獲裝置。 )  | **VT \_ BSTR** |
| "WaveInID"     | 音訊捕獲裝置的識別碼。 僅 (音訊捕獲裝置。 )  | **VT \_ I4**   |



 

"FriendlyName" 和 "Description" 屬性適用于在 UI 中顯示。

-   每個裝置都可以使用「FriendlyName」屬性。 它包含人們看得懂的裝置名稱。
-   [描述] 屬性僅適用于 DV 和 D VHS/MPEG 攝像機裝置。 如需詳細資訊，請參閱 [MSDV 驅動程式](msdv-driver.md) 和 [MSTape 驅動程式](mstape-driver.md)。 如果有的話，它會包含裝置的描述，而該裝置的描述比 "FriendlyName" 屬性更明確。 通常會包含廠商名稱。
-   "DevicePath" 屬性不是人們可讀取的字串，但在系統上的每個影片捕獲裝置保證都是唯一的。 您可以使用這個屬性來區別相同裝置模型的兩個或多個實例。
-   如果出現 "WaveInID" 屬性，則表示 DirectShow 捕獲篩選器會在內部使用 [波形音訊](../multimedia/waveform-audio.md) api 來與裝置通訊。 "WaveInID" 屬性的值會對應到 **waveIn \** _ 函式所使用的識別碼，例如 [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)。

若要從標記讀取屬性，請執行下列步驟。

1.  呼叫 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) 來取得 [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) 介面的指標。
2.  呼叫 **IPropertyBag：： read** 以讀取屬性。

下列程式碼範例示範如何列舉裝置名字標記的清單並取得屬性。


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



若要建立裝置的 DirectShow 捕獲篩選器，請呼叫 [**IMoniker：： BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) 方法來取得 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。 然後呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ，將篩選新增至篩選圖形：


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊捕獲](audio-capture.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 
