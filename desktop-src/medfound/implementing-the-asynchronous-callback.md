---
description: 執行非同步回呼
ms.assetid: c2c9d0f7-038b-4f23-985c-b812908d71a7
title: 執行非同步回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24088aea4e74b39ae08625c6917a5ca56f554158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000069"
---
# <a name="implementing-the-asynchronous-callback"></a><span data-ttu-id="2ca3d-103">執行非同步回呼</span><span class="sxs-lookup"><span data-stu-id="2ca3d-103">Implementing the Asynchronous Callback</span></span>

<span data-ttu-id="2ca3d-104">下列程式碼顯示執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面所需的基本架構。</span><span class="sxs-lookup"><span data-stu-id="2ca3d-104">The following code shows the basic framework needed to implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="2ca3d-105">在此範例中，會將 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法宣告為純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="2ca3d-105">In this example, the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is declared as a pure virtual method.</span></span> <span data-ttu-id="2ca3d-106">此方法的執行取決於您要呼叫的非同步方法。</span><span class="sxs-lookup"><span data-stu-id="2ca3d-106">The implementation of this method will depend on which asynchronous method you are calling.</span></span> <span data-ttu-id="2ca3d-107">如需詳細資訊，請參閱 [呼叫非同步方法](calling-asynchronous-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="2ca3d-107">For more information, see [Calling Asynchronous Methods](calling-asynchronous-methods.md).</span></span>


```C++
#include <shlwapi.h>

class CAsyncCallback : public IMFAsyncCallback 
{
public:
    CAsyncCallback () : m_cRef(1) { }
    virtual ~CAsyncCallback() { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CAsyncCallback, IMFAsyncCallback),
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
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult) = 0;
    // TODO: Implement this method. 

    // Inside Invoke, IMFAsyncResult::GetStatus to get the status.
    // Then call the EndX method to complete the operation. 

private:
    long    m_cRef;
};
```



<span data-ttu-id="2ca3d-108">下列程式碼顯示衍生自之類別的範例 `CAsyncCallback` ：</span><span class="sxs-lookup"><span data-stu-id="2ca3d-108">This following code shows an example implementation of a class that derives from `CAsyncCallback`:</span></span>


```C++
class CMyCallback : public CAsyncCallback
{
    HANDLE m_hEvent;
    IMFByteStream *m_pStream;

    HRESULT m_hrStatus;
    ULONG   m_cbRead;

public:

    CMyCallback(IMFByteStream *pStream, HRESULT *phr) 
        : m_pStream(pStream), m_hrStatus(E_PENDING), m_cbRead(0)
    {
        *phr = S_OK;

        m_pStream->AddRef();

        m_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

        if (m_hEvent == NULL)
        {
            *phr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    ~CMyCallback()
    {
        m_pStream->Release();
        CloseHandle(m_hEvent);
    }

    HRESULT WaitForCompletion(DWORD msec)
    {
        DWORD result = WaitForSingleObject(m_hEvent, msec);

        switch (result)
        {
        case WAIT_TIMEOUT:
            return E_PENDING;

        case WAIT_ABANDONED:
        case WAIT_OBJECT_0:
            return m_hrStatus;

        default:
            return HRESULT_FROM_WIN32(GetLastError());
        }
    }

    ULONG   GetBytesRead() const { return m_cbRead; }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
};
```



<span data-ttu-id="2ca3d-109">此範例會對 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法內的事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="2ca3d-109">This example signals an event inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="2ca3d-110">如需各種選項的討論，請參閱 [呼叫非同步方法](calling-asynchronous-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="2ca3d-110">For a discussion of the various options, see [Calling Asynchronous Methods](calling-asynchronous-methods.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ca3d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ca3d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca3d-112">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="2ca3d-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



