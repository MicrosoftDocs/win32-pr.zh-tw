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
# <a name="custom-asynchronous-result-objects"></a><span data-ttu-id="74111-103">自訂非同步結果物件</span><span class="sxs-lookup"><span data-stu-id="74111-103">Custom Asynchronous Result Objects</span></span>

<span data-ttu-id="74111-104">本主題說明如何執行 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面。</span><span class="sxs-lookup"><span data-stu-id="74111-104">This topic describes how to implement the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>

<span data-ttu-id="74111-105">您很少需要撰寫 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="74111-105">It is rare that you will need to write a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="74111-106">在幾乎所有情況下，標準媒體基礎的實施都已足夠。</span><span class="sxs-lookup"><span data-stu-id="74111-106">In almost all cases, the standard Media Foundation implementation is sufficient.</span></span> <span data-ttu-id="74111-107"> (此實 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 函式會傳回。 ) 不過，如果您撰寫自訂的執行，則有一些要注意的問題。</span><span class="sxs-lookup"><span data-stu-id="74111-107">(This implementation is returned by the [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) function.) However, if you do write a custom implementation, there are some issues to be aware of.</span></span>

<span data-ttu-id="74111-108">首先，您的執行必須繼承 [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) 結構。</span><span class="sxs-lookup"><span data-stu-id="74111-108">First, your implementation must inherit the [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) structure.</span></span> <span data-ttu-id="74111-109">媒體基礎的工作佇列會在內部使用此結構來分派作業。</span><span class="sxs-lookup"><span data-stu-id="74111-109">The Media Foundation work queues use this structure internally to dispatch the operation.</span></span> <span data-ttu-id="74111-110">將所有結構成員初始化為零，但 **pCallback** 成員除外，其中包含呼叫者的回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="74111-110">Initialize all of the structure members to zero, except for the **pCallback** member, which contains a pointer to the caller's callback interface.</span></span>

<span data-ttu-id="74111-111">其次，您的物件應該在其函式中呼叫 [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) ，以鎖定媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="74111-111">Second, your object should call [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) in its constructor, to lock the Media Foundation platform.</span></span> <span data-ttu-id="74111-112">呼叫 [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) 以將平臺解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="74111-112">Call [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) to unlock the platform.</span></span> <span data-ttu-id="74111-113">這些函數有助於防止平臺在物件終結之前關閉。</span><span class="sxs-lookup"><span data-stu-id="74111-113">These functions help to prevent the platform from shutting down before the object is destroyed.</span></span> <span data-ttu-id="74111-114">如需詳細資訊，請參閱 [工作佇列](work-queues.md)。</span><span class="sxs-lookup"><span data-stu-id="74111-114">For more information, see [Work Queues](work-queues.md).</span></span>

<span data-ttu-id="74111-115">下列程式碼顯示 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的基本執行。</span><span class="sxs-lookup"><span data-stu-id="74111-115">The following code shows a basic implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="74111-116">如所示，此程式碼不提供標準媒體基礎的任何其他功能。</span><span class="sxs-lookup"><span data-stu-id="74111-116">As shown, this code provides no additional features beyond the standard Media Foundation implementation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="74111-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="74111-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74111-118">工作佇列</span><span class="sxs-lookup"><span data-stu-id="74111-118">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="74111-119">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="74111-119">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



