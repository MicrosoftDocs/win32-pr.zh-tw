---
description: 列舉效果和轉換
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: 列舉效果和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971929"
---
# <a name="enumerating-effects-and-transitions"></a>列舉效果和轉換

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

DirectShow 提供用來列舉裝置的 [系統裝置列舉](system-device-enumerator.md) 值物件。 您可以使用它來抓取在使用者系統上安裝之效果或轉換的名字標記。

系統裝置列舉值會公開 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面。 它會傳回指定裝置類別的類別列舉值。 類別列舉值接著會公開 [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) 介面，並傳回類別中每個裝置的名字。 如需使用 **ICreateDevEnum** 的詳細討論，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。 以下是有關 DirectShow 編輯服務的簡短摘要。

若要列舉效果或轉換，請執行下列步驟。

1.  建立系統裝置列舉值的實例。
2.  呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 方法以取出類別列舉值。 類別目錄是由)  (Clsid 的類別識別碼所定義。 使用 CLSID \_ VideoEffects1Category 進行轉換的效果或 clsid \_ VideoEffects2Category。
3.  呼叫 **IEnumMoniker：： Next** 以取得列舉中的每個標記。
4.  針對每個標記，呼叫 **IMoniker：： BindToStorage** 來取出其相關聯的屬性包。

屬性包包含效果或轉換 (GUID) 的易記名稱和全域唯一識別碼。 應用程式可以顯示易記名稱清單，然後取得對應的 GUID。

下列程式碼範例說明這些步驟。


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
