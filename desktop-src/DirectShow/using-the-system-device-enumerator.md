---
description: 使用系統裝置列舉值
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: 使用系統裝置列舉值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7192a1ea85d807dd388b79eef455edf59c83d3c22ab3a4a330799b3491253bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083530"
---
# <a name="using-the-system-device-enumerator"></a>使用系統裝置列舉值

系統裝置列舉值提供統一的方式來列舉使用者系統上註冊的篩選準則（依類別目錄）。 此外，它也會區分個別硬體裝置，即使相同的篩選器支援它們也是一樣。 這特別適用于使用 Windows Driver Model (WDM) 和 KSProxy 篩選器的裝置。 例如，使用者可能會有數個 WDM 影片捕獲裝置，而且全部都受到相同的篩選準則支援。 系統裝置列舉值會將它們視為個別的裝置實例。

系統裝置列舉值的運作方式是建立特定類別的列舉值，例如音訊捕獲或影片壓縮。 類別列舉值會針對類別中的每個裝置傳回唯一的標記。 類別列舉值會自動在類別中包含任何相關的隨插即用裝置。 如需分類清單，請參閱 [篩選分類](filter-categories.md)。

若要使用系統裝置列舉值，請執行下列動作：

1.  藉由呼叫 **CoCreateInstance** 來建立系統裝置枚舉器。 CLSID)  (的類別識別碼是 CLSID \_ SystemDeviceEnum。
2.  藉由呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) 與所需分類的 CLSID 來取得類別列舉值。 這個方法會傳回 **IEnumMoniker** 介面指標。 如果類別目錄是空的 (或不存在) 中，此方法會傳回 \_ FALSE，而不是錯誤碼。 如果是，則傳回的 **IEnumMoniker** 指標為 **Null** ，而取值會造成例外狀況。 因此， \_ 當您呼叫 **CreateClassEnumerator** 時，請明確地測試是否沒問題，而不是呼叫一般的 **SUCCEEDED** 宏。
3.  使用 **IEnumMoniker：： Next** 方法來列舉每個標記。 這個方法會傳回 **IMoniker** 介面指標。 當 **下一個** 方法到達列舉的結尾時，它也會傳回 \_ FALSE，因此再次檢查是否 \_ 正常。
4.  若要取得裝置的易記名稱 (例如，要顯示在使用者介面) 中，請呼叫 **IMoniker：： BindToStorage** 方法。
5.  若要建立及初始化管理裝置的 DirectShow 篩選，請在標記上呼叫 **IMoniker：： BindToObject** 。 呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 將篩選準則新增至圖形。

下圖說明此程序。

![列舉裝置](images/sysdevenum.png)

下列範例示範如何列舉在使用者系統上安裝的影片壓縮機。 為了簡潔起見，此範例會執行最少量的錯誤檢查。


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



**裝置的名字**

針對裝置的名字標記，您可以傳遞 [**IFilterGraph2：： AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) 方法來建立裝置的捕獲篩選器。 如需範例程式碼，請參閱該方法的檔。

**IMoniker：： GetDisplayName** 方法會傳回標記的顯示名稱。 雖然顯示名稱是可讀取的，但通常不會將它顯示給終端使用者。 改為取得屬性包中的易記名稱，如先前所述。

**IMoniker：:P arsedisplayname** 方法或 **MkParseDisplayName** 函數可以用來建立指定篩選類別目錄的預設裝置標記。 使用顯示名稱搭配表單 `@device:*:{category-clsid}` ，其中 `category-clsid` 是分類 GUID 的字串表示。 預設的名字標記是該類別的裝置列舉值所傳回的第一個標記。

 

 



