---
description: 如何設定 Proxy 定位器
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: 如何設定 Proxy 定位器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b383dda9ac78b2c62aa8481a09cc5c0d7b3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971681"
---
# <a name="how-to-configure-the-proxy-locator"></a><span data-ttu-id="854c7-103">如何設定 Proxy 定位器</span><span class="sxs-lookup"><span data-stu-id="854c7-103">How to Configure the Proxy Locator</span></span>

<span data-ttu-id="854c7-104">應用程式可以藉由將 [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) 屬性設定為應用程式所執行的 proxy 定位器 factory 物件，來變更 proxy 定位器的預設設定。</span><span class="sxs-lookup"><span data-stu-id="854c7-104">The application can change the default configuration of the proxy locator by setting the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property to the proxy locator factory object that is implemented by the application.</span></span> <span data-ttu-id="854c7-105">當應用程式呼叫來源解析程式方法來建立網路來源時，媒體基礎會呼叫 proxy 定位器 factory。</span><span class="sxs-lookup"><span data-stu-id="854c7-105">When the application calls source resolver methods to create the network source, Media Foundation calls the proxy locator factory.</span></span> <span data-ttu-id="854c7-106">此物件會使用自訂設定來建立 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="854c7-106">This object creates the proxy locator with custom configuration.</span></span>

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a><span data-ttu-id="854c7-107">變更 proxy 定位器的預設設定</span><span class="sxs-lookup"><span data-stu-id="854c7-107">To change the default configuration setting of the proxy locator</span></span>

1.  <span data-ttu-id="854c7-108">執行 [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) 介面。</span><span class="sxs-lookup"><span data-stu-id="854c7-108">Implement the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
2.  <span data-ttu-id="854c7-109">在 [**IMFNetProxyLocatorFactory：： CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) 方法中，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="854c7-109">In the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method, do the following:</span></span>
    1.  <span data-ttu-id="854c7-110">建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="854c7-110">Create a property store.</span></span>
    2.  <span data-ttu-id="854c7-111">設定 proxy 定位器的設定。</span><span class="sxs-lookup"><span data-stu-id="854c7-111">Set the configuration settings for the proxy locator.</span></span> <span data-ttu-id="854c7-112">如需這些設定的詳細資訊，請參閱 [Proxy 定位器設定](proxy-locator-configuration-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="854c7-112">For information about these settings, see [Proxy Locator Configuration Settings](proxy-locator-configuration-settings.md).</span></span>
    3.  <span data-ttu-id="854c7-113">呼叫 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) 函數。</span><span class="sxs-lookup"><span data-stu-id="854c7-113">Call the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="854c7-114">傳入屬性存放區和通訊協定。</span><span class="sxs-lookup"><span data-stu-id="854c7-114">Pass in the property store and the protocol.</span></span> <span data-ttu-id="854c7-115">此通訊協定是在 [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)的 *pszProtocol* 參數中指定。</span><span class="sxs-lookup"><span data-stu-id="854c7-115">The protocol is specified in the *pszProtocol* parameter of [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span></span>
3.  <span data-ttu-id="854c7-116">建立 proxy 定位器 factory 類別的實例，並取得其 [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="854c7-116">Create an instance of your proxy locator factory class and get a pointer to its [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
4.  <span data-ttu-id="854c7-117">建立另一個屬性存放區，並將 [**MFNETSOURCE \_ PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) 屬性的值設定為等於步驟3的 [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) 指標。</span><span class="sxs-lookup"><span data-stu-id="854c7-117">Create another property store and set the value of the [**MFNETSOURCE\_PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) property equal to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer from step 3.</span></span>
5.  <span data-ttu-id="854c7-118">當您建立網路來源時，請在來源解析程式方法（例如 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)）的 *pProps* 參數中傳遞屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="854c7-118">When you create the network source, pass the property store in the *pProps* parameter of the source resolver methods such as [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

## <a name="example"></a><span data-ttu-id="854c7-119">範例</span><span class="sxs-lookup"><span data-stu-id="854c7-119">Example</span></span>

<span data-ttu-id="854c7-120">下列程式碼範例會執行 [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) 介面。</span><span class="sxs-lookup"><span data-stu-id="854c7-120">The following code example implements the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span> <span data-ttu-id="854c7-121">[**IMFNetProxyLocatorFactory：： CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)方法會建立預設 proxy 定位器的實例，並將它設定為在自動偵測模式下運作。</span><span class="sxs-lookup"><span data-stu-id="854c7-121">The [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method creates an instance of the default proxy locator, and configures it to operate in auto-detect mode.</span></span>


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



<span data-ttu-id="854c7-122">下一個範例顯示如何將 [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) 指標傳遞至網路來源。</span><span class="sxs-lookup"><span data-stu-id="854c7-122">The next example shows how to pass the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer to the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="854c7-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="854c7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="854c7-124">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="854c7-124">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



