---
description: 支援多個回呼
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: 支援多個回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692308"
---
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="b957a-103">支援多個回呼</span><span class="sxs-lookup"><span data-stu-id="b957a-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="b957a-104">如果您呼叫一個以上的非同步方法，每個方法都需要 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)的個別實作為。</span><span class="sxs-lookup"><span data-stu-id="b957a-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="b957a-105">不過，您可能想要在單一 c + + 類別內執行回呼。</span><span class="sxs-lookup"><span data-stu-id="b957a-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="b957a-106">類別只能有一個叫用 **方法，** 因此其中一個解決方案是提供協助程式類別，將 **Invoke** 呼叫委派給容器類別上的另一個方法。</span><span class="sxs-lookup"><span data-stu-id="b957a-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="b957a-107">下列程式碼會示範名為的類別範本 `AsyncCallback` ，它會示範這種方法。</span><span class="sxs-lookup"><span data-stu-id="b957a-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



<span data-ttu-id="b957a-108">範本參數是容器類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b957a-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="b957a-109">此函式 `AsyncCallback` 有兩個參數：容器類別的指標，以及容器類別上的回呼方法位址。</span><span class="sxs-lookup"><span data-stu-id="b957a-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="b957a-110">容器類別可以有多個類別的實例 `AsyncCallback` 做為成員變數，每個非同步方法一個。</span><span class="sxs-lookup"><span data-stu-id="b957a-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="b957a-111">當容器類別呼叫非同步方法時，它會使用適當物件的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面 `AsyncCallback` 。</span><span class="sxs-lookup"><span data-stu-id="b957a-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="b957a-112">`AsyncCallback`呼叫物件的 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)方法時，會將呼叫委派給容器類別上的正確方法。</span><span class="sxs-lookup"><span data-stu-id="b957a-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="b957a-113">此 `AsyncCallback` 物件也會將 **AddRef** 和 **Release** 呼叫委派給容器類別，讓容器類別管理物件的存留期 `AsyncCallback` 。</span><span class="sxs-lookup"><span data-stu-id="b957a-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="b957a-114">這可保證在 `AsyncCallback` 容器物件本身刪除之前，將不會刪除物件。</span><span class="sxs-lookup"><span data-stu-id="b957a-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="b957a-115">下列程式碼顯示如何使用此範本：</span><span class="sxs-lookup"><span data-stu-id="b957a-115">The following code shows how to use this template:</span></span>


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



<span data-ttu-id="b957a-116">在此範例中，容器類別的名稱為 `CMyObject` 。</span><span class="sxs-lookup"><span data-stu-id="b957a-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="b957a-117">*M \_ CB* 成員變數是 `AsyncCallback` 物件。</span><span class="sxs-lookup"><span data-stu-id="b957a-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="b957a-118">在此函式中 `CMyObject` ，會使用方法的位址初始化 *m \_ CB* 成員變數 `CMyObject::OnInvoke` 。</span><span class="sxs-lookup"><span data-stu-id="b957a-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b957a-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b957a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b957a-120">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="b957a-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



