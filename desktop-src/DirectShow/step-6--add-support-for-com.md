---
description: 步驟 6.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: 步驟 6. 新增對 COM 的支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e477cc22650604bce623874c0afbba1063609e44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984230"
---
# <a name="step-6-add-support-for-com"></a>步驟 6. 新增對 COM 的支援

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟6。

最後一個步驟是新增對 COM 的支援。

## <a name="reference-counting"></a>參考計數

您不需要執行 [**IUnknown：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 或 [**Iunknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。 所有的篩選和釘選類別都是衍生自 [**CUnknown**](cunknown.md)，它會處理參考計數。

## <a name="queryinterface"></a>QueryInterface

所有的篩選和釘選類別都會針對它們所繼承的任何 COM 介面，執行 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。 例如， [**CTransformFilter**](ctransformfilter.md)會透過 [**CBaseFilter**](cbasefilter.md)) 繼承 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (。 如果您的篩選不會公開任何額外的介面，則不需要執行任何其他動作。

若要公開其他介面，請覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法。 例如，假設您的篩選器會執行名為 IMyCustomInterface 的自訂介面。 若要將此介面公開給用戶端，請執行下列動作：

-   從該介面衍生您的篩選類別。
-   將 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏放在公用宣告區段中。
-   覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 以檢查介面的 IID，並將指標傳回至篩選準則。

下列程式碼顯示這些步驟：


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



如需詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。

## <a name="object-creation"></a>建立物件

如果您打算將篩選封裝到 DLL 中，並將它提供給其他用戶端使用，您必須支援 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 和其他相關的 COM 函數。 基類庫會執行大部分的，您只需要提供一些關於篩選的資訊。 本節將簡短介紹該怎麼做。 如需詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。

首先，撰寫會傳回新的篩選準則實例的靜態類別方法。 您可以將此方法命名為任何您喜歡的名稱，但簽章必須符合下列範例中所示的內容：


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



接下來，宣告名為 *g \_ Templates* 的 [**CFactoryTemplate**](cfactorytemplate.md)類別實例的全域陣列。 每個 **CFactoryTemplate** 類別都包含一個篩選準則的登錄資訊。 有幾個篩選可以位於單一 DLL 中;只包含其他 **CFactoryTemplate** 專案。 您也可以宣告其他 COM 物件，例如屬性頁。


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



定義名為 *g \_ cTemplates* 的全域整數，其值等於 *g \_ 範本* 陣列的長度：


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



最後，請執行 DLL 註冊函式。 下列範例會顯示這些函式的最基本執行：


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a>篩選登錄專案

先前的範例示範如何註冊 COM 的篩選器 CLSID。 針對許多篩選準則，這就夠了。 接著，用戶端應該使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 建立篩選，並藉由呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter)將它新增至篩選圖形。 不過，在某些情況下，您可能會想要在登錄中提供篩選的其他相關資訊。 這項資訊會執行下列動作：

-   可讓用戶端使用 [篩選器](filter-mapper.md) 對應程式或 [系統裝置列舉](system-device-enumerator.md)值來探索篩選。
-   讓篩選圖形管理員在自動圖形建立期間探索篩選。

下列範例會在影片壓縮程式類別目錄中註冊 RLE 編碼器篩選器。 如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。 請務必閱讀註冊篩選準則的章節 [指導方針](guidelines-for-registering-filters.md)，其中描述了篩選註冊的建議作法。


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



此外，篩選不需要封裝在 Dll 內。 在某些情況下，您可能會撰寫僅針對特定應用程式所設計的特殊篩選。 在這種情況下，您可以直接在應用程式中編譯篩選類別，並使用運算子來建立它 `new` ，如下列範例所示：


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[智慧型連接](intelligent-connect.md)
</dt> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> <dt>

[寫入轉換篩選](writing-transform-filters.md)
</dt> </dl>

 

 
