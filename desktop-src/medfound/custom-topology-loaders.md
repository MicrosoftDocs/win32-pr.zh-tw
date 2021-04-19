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
# <a name="custom-topology-loaders"></a>自訂拓撲載入器

當應用程式將部分拓撲排入媒體會話的佇列時，媒體會話會使用拓撲載入器來解析拓撲。 根據預設，媒體會話會使用拓撲載入器的標準媒體基礎執行，但您也可以提供自訂的執行。 這可讓您更充分掌控最後的拓撲。 自訂拓撲載入器必須執行 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) 介面。

若要在媒體會話上設定自訂拓撲載入器，請執行下列動作：

1.  藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)來建立空的屬性存放區。
2.  在屬性存放區上設定 [ [**MF \_ 會話 \_ TOPOLOADER**](mf-session-topoloader-attribute.md) ] 屬性。 屬性的值是您自訂載入器的 CLSID。
3.  呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立未受保護內容的媒體會話，或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) 以在受保護媒體路徑內建立媒體會話， (PMP) 。

> [!Note]  
> 若要在 PMP 內使用自訂拓撲載入器，拓撲載入器必須是受信任的元件。 如需詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。

 

下列程式碼顯示如何在媒體會話上設定自訂拓撲載入器。


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



您不需要在拓撲載入器中執行整個拓撲載入演算法。 或者，您可以包裝標準媒體基礎拓撲載入器。 在 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法的執行中，視需要修改拓撲，然後將修改過的拓撲傳遞給標準拓撲載入器。 然後，標準拓撲載入器會完成拓撲。 您也可以修改已完成的拓撲，然後將它傳回給媒體會話。

下列程式碼會顯示此方法的一般大綱。 它不會顯示 [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法的任何詳細資料，因為這些方法將取決於您應用程式的特定需求。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Advanced 拓朴建築](advanced-topology-building.md)
</dt> </dl>

 

 



