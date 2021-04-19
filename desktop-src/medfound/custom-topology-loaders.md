---
description: 自訂拓撲載入器
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: 自訂拓撲載入器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973404"
---
# <a name="custom-topology-loaders"></a><span data-ttu-id="99b00-103">自訂拓撲載入器</span><span class="sxs-lookup"><span data-stu-id="99b00-103">Custom Topology Loaders</span></span>

<span data-ttu-id="99b00-104">當應用程式將部分拓撲排入媒體會話的佇列時，媒體會話會使用拓撲載入器來解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="99b00-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="99b00-105">根據預設，媒體會話會使用拓撲載入器的標準媒體基礎執行，但您也可以提供自訂的執行。</span><span class="sxs-lookup"><span data-stu-id="99b00-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="99b00-106">這可讓您更充分掌控最後的拓撲。</span><span class="sxs-lookup"><span data-stu-id="99b00-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="99b00-107">自訂拓撲載入器必須執行 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) 介面。</span><span class="sxs-lookup"><span data-stu-id="99b00-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="99b00-108">若要在媒體會話上設定自訂拓撲載入器，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="99b00-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="99b00-109">藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)來建立空的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="99b00-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="99b00-110">在屬性存放區上設定 [ [**MF \_ 會話 \_ TOPOLOADER**](mf-session-topoloader-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="99b00-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="99b00-111">屬性的值是您自訂載入器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="99b00-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="99b00-112">呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立未受保護內容的媒體會話，或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) 以在受保護媒體路徑內建立媒體會話， (PMP) 。</span><span class="sxs-lookup"><span data-stu-id="99b00-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="99b00-113">若要在 PMP 內使用自訂拓撲載入器，拓撲載入器必須是受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="99b00-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="99b00-114">如需詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。</span><span class="sxs-lookup"><span data-stu-id="99b00-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="99b00-115">下列程式碼顯示如何在媒體會話上設定自訂拓撲載入器。</span><span class="sxs-lookup"><span data-stu-id="99b00-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



<span data-ttu-id="99b00-116">您不需要在拓撲載入器中執行整個拓撲載入演算法。</span><span class="sxs-lookup"><span data-stu-id="99b00-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="99b00-117">或者，您可以包裝標準媒體基礎拓撲載入器。</span><span class="sxs-lookup"><span data-stu-id="99b00-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="99b00-118">在 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法的執行中，視需要修改拓撲，然後將修改過的拓撲傳遞給標準拓撲載入器。</span><span class="sxs-lookup"><span data-stu-id="99b00-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="99b00-119">然後，標準拓撲載入器會完成拓撲。</span><span class="sxs-lookup"><span data-stu-id="99b00-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="99b00-120">您也可以修改已完成的拓撲，然後將它傳回給媒體會話。</span><span class="sxs-lookup"><span data-stu-id="99b00-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="99b00-121">下列程式碼會顯示此方法的一般大綱。</span><span class="sxs-lookup"><span data-stu-id="99b00-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="99b00-122">它不會顯示 [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法的任何詳細資料，因為這些方法將取決於您應用程式的特定需求。</span><span class="sxs-lookup"><span data-stu-id="99b00-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a><span data-ttu-id="99b00-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="99b00-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99b00-124">**MFCreateTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="99b00-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="99b00-125">Advanced 拓朴建築</span><span class="sxs-lookup"><span data-stu-id="99b00-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



