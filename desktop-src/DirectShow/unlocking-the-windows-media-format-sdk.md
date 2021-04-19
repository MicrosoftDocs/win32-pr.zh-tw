---
description: 解除鎖定 Windows Media Format SDK
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: 解除鎖定 Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106988525"
---
# <a name="unlocking-the-windows-media-format-sdk"></a><span data-ttu-id="271c3-103">解除鎖定 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="271c3-103">Unlocking the Windows Media Format SDK</span></span>

<span data-ttu-id="271c3-104">若要存取7或7.1 版的 Windows Media Format SDK，應用程式必須在執行時間提供軟體憑證，也稱為金鑰。</span><span class="sxs-lookup"><span data-stu-id="271c3-104">To access version 7 or 7.1 of the Windows Media Format SDK, an application must provide a software certificate, also called a key, at run time.</span></span> <span data-ttu-id="271c3-105">此索引鍵包含在應用程式在組建時連結的靜態程式庫，稱為 wmstub。</span><span class="sxs-lookup"><span data-stu-id="271c3-105">This key is contained in a static library called wmstub.lib to which the application links at build time.</span></span> <span data-ttu-id="271c3-106">只有在建立或讀取受 DRM 保護的檔案時，才需要個別的金鑰。</span><span class="sxs-lookup"><span data-stu-id="271c3-106">An individualized key is only required for creating or reading DRM-protected files.</span></span> <span data-ttu-id="271c3-107">您可以使用 Windows Media Format SDK 提供的靜態程式庫來建立非 DRM 檔案。</span><span class="sxs-lookup"><span data-stu-id="271c3-107">Non-DRM files can be created using the static library provided with the Windows Media Format SDK.</span></span> <span data-ttu-id="271c3-108">如需取得 DRM 金鑰的詳細資訊，請參閱 Windows Media Format SDK。</span><span class="sxs-lookup"><span data-stu-id="271c3-108">For details on obtaining the DRM key, see the Windows Media Format SDK.</span></span> <span data-ttu-id="271c3-109">當 DirectShow 應用程式新增至篩選圖形時，它會提供其憑證給 WM ASF 寫入器。</span><span class="sxs-lookup"><span data-stu-id="271c3-109">A DirectShow application provides its certificate to the WM ASF Writer when it is added to the filter graph.</span></span> <span data-ttu-id="271c3-110">應用程式必須使用 COM **IServiceProvider** 和 **IObjectWithSite** 介面註冊為金鑰提供者。</span><span class="sxs-lookup"><span data-stu-id="271c3-110">The application must register as a key provider using the COM **IServiceProvider** and **IObjectWithSite** interfaces.</span></span> <span data-ttu-id="271c3-111">使用這項技術時，應用程式會實作為衍生自 **IServiceProvider** 的金鑰提供者類別。</span><span class="sxs-lookup"><span data-stu-id="271c3-111">Using this technique, the application implements a key provider class derived from **IServiceProvider**.</span></span> <span data-ttu-id="271c3-112">這個類別會執行三個標準 COM 方法（**AddRef**、 **QueryInterface** 和 **Release**）以及一個額外的 **QueryService** 方法（由篩選圖形管理員呼叫）。</span><span class="sxs-lookup"><span data-stu-id="271c3-112">This class implements the three standard COM methods—**AddRef**, **QueryInterface**, and **Release**—along with one additional method, **QueryService**, which is called by the filter graph manager.</span></span> <span data-ttu-id="271c3-113">**QueryService** 會呼叫 Windows MEDIA Format SDK 方法 [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) ，並將指標移至篩選圖形管理員，以指向所建立的憑證。</span><span class="sxs-lookup"><span data-stu-id="271c3-113">**QueryService** calls the Windows Media Format SDK method [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) and returns to the filter graph manager a pointer to the certificate that was created.</span></span> <span data-ttu-id="271c3-114">如果憑證有效，則篩選圖形管理員可讓圖形建立程式繼續進行。</span><span class="sxs-lookup"><span data-stu-id="271c3-114">If the certificate is valid, the filter graph manager allows the graph-building process to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="271c3-115">若要建立應用程式，請針對 [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))的原型包含 Wmsdkidl，並連結至 Wmstub .lib 程式庫。</span><span class="sxs-lookup"><span data-stu-id="271c3-115">To build an application, include Wmsdkidl.h for the prototype for [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)), and link to the Wmstub.lib library.</span></span>

 

<span data-ttu-id="271c3-116">下列程式碼範例說明此程式中的基本步驟：</span><span class="sxs-lookup"><span data-stu-id="271c3-116">The following code example illustrates the basic steps in this process:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="271c3-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="271c3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="271c3-118">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="271c3-118">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
