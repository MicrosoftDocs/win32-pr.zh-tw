---
description: 自訂非同步結果物件
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: 自訂非同步結果物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5a0109b47255bc14fcccafbbb09c419848b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191073"
---
# <a name="custom-asynchronous-result-objects"></a>自訂非同步結果物件

本主題說明如何執行 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面。

您很少需要撰寫 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的自訂執行。 在幾乎所有情況下，標準媒體基礎的實施都已足夠。  (此實 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 函式會傳回。 ) 不過，如果您撰寫自訂的執行，則有一些要注意的問題。

首先，您的執行必須繼承 [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) 結構。 媒體基礎的工作佇列會在內部使用此結構來分派作業。 將所有結構成員初始化為零，但 **pCallback** 成員除外，其中包含呼叫者的回呼介面指標。

其次，您的物件應該在其函式中呼叫 [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) ，以鎖定媒體基礎平臺。 呼叫 [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) 以將平臺解除鎖定。 這些函數有助於防止平臺在物件終結之前關閉。 如需詳細資訊，請參閱 [工作佇列](work-queues.md)。

下列程式碼顯示 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的基本執行。 如所示，此程式碼不提供標準媒體基礎的任何其他功能。


```C++
///////////////////////////////////////////////////////////////////////////////
//  CMyAsyncResult
//
//  Custom implementation of IMFAsyncResult. All implementations of this 
//  interface must inherit the MFASYNCRESULT structure.
// 
///////////////////////////////////////////////////////////////////////////////

class CMyAsyncResult : public MFASYNCRESULT
{
protected:
    LONG        m_cRef;             // Reference count.
    BOOL        m_bLockPlatform;    // Locked the Media Foundation platform?
    IUnknown*   m_pState;           // Caller's state object. 
    IUnknown*   m_pObject;  // Optional object. See IMFAsyncResult::GetObject.

    // Constructor. 
    CMyAsyncResult(IMFAsyncCallback *pCallback, IUnknown *pState, HRESULT *phr) :
        m_cRef(1),
        m_bLockPlatform(FALSE),
        m_pObject(NULL),
        m_pState(pState)
    {
        *phr = MFLockPlatform();

        m_bLockPlatform = TRUE;

        // Initialize the MFASYNCRESULT members.
        ZeroMemory(&this->overlapped, sizeof(OVERLAPPED));
        hrStatusResult = S_OK;
        dwBytesTransferred = 0;
        hEvent = NULL;

        this->pCallback = pCallback;
        if (pCallback)
        {
            this->pCallback->AddRef();
        }

        if (m_pState)
        {
            m_pState->AddRef();
        }
    }

    virtual ~CMyAsyncResult()
    {
        SafeRelease(&pCallback);
        SafeRelease(&m_pState);
        SafeRelease(&m_pObject);

        if (m_bLockPlatform)
        {
            MFUnlockPlatform();
        }
    }

public:
    // Static method to create an instance of this object.
    static HRESULT CreateInstance(
        IMFAsyncCallback *pCallback,    // Callback to invoke.
        IUnknown *pState,               // Optional state object.
        CMyAsyncResult **ppResult       // Receives a pointer to the object.
        )
    {
        HRESULT hr = S_OK;

        *ppResult = NULL;

        CMyAsyncResult *pResult = 
            new (std::nothrow) CMyAsyncResult(pCallback, pState, &hr);

        if (pResult == NULL)
        {
            return E_OUTOFMEMORY;
        }
        if (FAILED(hr))
        {
            delete pResult;
            return hr;
        }

        // If the callback is NULL, create an event that will be signaled.
        if (pCallback == NULL)
        {
            pResult->hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
            if (pResult->hEvent == NULL)
            {
                hr = HRESULT_FROM_WIN32(GetLastError());
            }
        }

        if (SUCCEEDED(hr))
        {
            *ppResult = pResult;  // Return the pointer to the caller.
        }
        else
        {
            pResult->Release();
        }
        return hr;
    }

    // SetObject: Sets the optional result object. 
    // (This method is not part of the interface.)
    HRESULT SetObject(IUnknown *pObject)
    {
        SafeRelease(&m_pObject);
        m_pObject = pObject;
        if (pObject)
        {
            m_pObject->AddRef();
        }
        return S_OK;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CMyAsyncResult, IMFAsyncResult),
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
    
    // IMFAsyncResult methods.
    STDMETHODIMP GetState(IUnknown** ppunkState)
    {
        if (ppunkState == NULL)
        {
            return E_POINTER;
        }

        *ppunkState = m_pState;
        if (m_pState)
        {
            (*ppunkState)->AddRef();
        }

        return S_OK;
    }

    STDMETHODIMP GetStatus( void)
    {
        return hrStatusResult;
    }

    STDMETHODIMP STDMETHODCALLTYPE SetStatus(HRESULT hrStatus)
    {
        hrStatusResult = hrStatus;
        return S_OK;
    }

    STDMETHODIMP GetObject(IUnknown **ppObject)
    {
        if (ppObject == NULL)
        {
            return E_POINTER;
        }

        *ppObject = m_pObject;
        if (m_pObject)
        {
            (*ppObject)->AddRef();
        }
        return S_OK;
    }

    IUnknown* STDMETHODCALLTYPE GetStateNoAddRef()
    {
        return m_pState;  // Warning! Can be NULL. 
    }
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作佇列](work-queues.md)
</dt> <dt>

[非同步回呼方法](asynchronous-callback-methods.md)
</dt> </dl>

 

 



