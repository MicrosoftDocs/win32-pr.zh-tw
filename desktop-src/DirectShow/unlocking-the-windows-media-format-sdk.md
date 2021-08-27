---
description: 解除鎖定 Windows 媒體格式 SDK
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: 解除鎖定 Windows 媒體格式 SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1f332711e9fd12c9b0ff1f789438d051487b81711f157ae1024a8e47973386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078658"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>解除鎖定 Windows 媒體格式 SDK

若要存取 Windows 媒體格式 SDK 的7或7.1 版本，應用程式必須在執行時間提供軟體憑證，也稱為金鑰。 此索引鍵包含在應用程式在組建時連結的靜態程式庫，稱為 wmstub。 只有在建立或讀取受 DRM 保護的檔案時，才需要個別的金鑰。 您可以使用 Windows 媒體格式 SDK 提供的靜態程式庫來建立非 DRM 檔案。 如需取得 DRM 金鑰的詳細資訊，請參閱 Windows 媒體格式 SDK。 DirectShow 的應用程式會在將其憑證新增至篩選圖形時，提供其憑證給 WM ASF 寫入器。 應用程式必須使用 COM **IServiceProvider** 和 **IObjectWithSite** 介面註冊為金鑰提供者。 使用這項技術時，應用程式會實作為衍生自 **IServiceProvider** 的金鑰提供者類別。 這個類別會執行三個標準 COM 方法（**AddRef**、 **QueryInterface** 和 **Release**）以及一個額外的 **QueryService** 方法（由篩選圖形管理員呼叫）。 **QueryService** 會呼叫 Windows 媒體格式 SDK 方法 [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) ，並傳回至篩選圖形管理員所建立之憑證的指標。 如果憑證有效，則篩選圖形管理員可讓圖形建立程式繼續進行。

> [!Note]  
> 若要建立應用程式，請針對 [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))的原型包含 Wmsdkidl，並連結至 Wmstub .lib 程式庫。

 

下列程式碼範例說明此程式中的基本步驟：


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
