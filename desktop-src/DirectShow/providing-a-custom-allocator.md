---
description: 提供自訂配置器
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: 提供自訂配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385655"
---
# <a name="providing-a-custom-allocator"></a>提供自訂配置器

本節說明如何提供篩選的自訂配置器。 僅說明 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 連接，但是 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 連線的步驟很類似。

首先，定義配置器的 c + + 類別。 您的配置器可以衍生自其中一個標準配置器類別（ [**CBaseAllocator**](cbaseallocator.md) 或 [**CMemAllocator**](cmemallocator.md)），或者您可以建立全新的配置器類別。 如果您建立新的類別，它必須公開 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。

其餘步驟取決於您的配置器是否屬於輸入釘選或您篩選上的輸出 pin。 在配置器協商階段，輸入 pin 扮演的角色與輸出 pin 不同，因為輸出 pin 最終會選取配置器。

**提供輸入 Pin 的自訂配置器**

若要為輸入 pin 提供配置器，請覆寫輸入釘選的 [**CBaseInputPin：： GetAllocator**](cbaseinputpin-getallocator.md) 方法。 在這個方法中，檢查 **m \_ pAllocator** 成員變數。 如果這個變數不是 **Null**，則表示已針對此連接選取配置器，因此 **GetAllocator** 方法必須傳回該配置器的指標。 如果 **m \_ PAllocator** 為 **Null**，表示尚未選取配置器，因此 **GetAllocator** 方法應傳回輸入釘選配置器的指標。 在此情況下，請建立自訂配置器的實例，並傳回其 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 指標。 下列程式碼顯示如何執行 **GetAllocator** 方法：


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



當上游篩選器選取配置器時，它會呼叫輸入釘選的 [**IMemInputPin：： NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) 方法。 覆寫 [**CBaseInputPin：： NotifyAllocator**](cbaseinputpin-notifyallocator.md) 方法以檢查配置器屬性。 在某些情況下，如果配置器不是您的自訂配置器，則輸入 pin 可能會拒絕配置器，但這可能會導致整個 pin 連線失敗。

**提供輸出釘選的自訂配置器**

若要為輸出 pin 提供配置器，請覆寫 [**CBaseOutputPin：： InitAllocator**](cbaseoutputpin-initallocator.md) 方法，以建立配置器的實例：


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



根據預設， [**CBaseOutputPin**](cbaseoutputpin.md) 類別會先從輸入 pin 要求配置器。 如果該配置器不適合，則輸出 pin 會建立自己的配置器。 若要強制連接使用您的自訂配置器，請覆寫 [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md) 方法。 不過，請注意，這可能會導致您的輸出 pin 無法與某些篩選連接，因為另一個篩選器可能也需要自己的自訂配置器。 第三個選項是切換順序：先嘗試您的自訂配置器，然後再切換回其他篩選器的配置器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[協商配置器](negotiating-allocators.md)
</dt> </dl>

 

 



