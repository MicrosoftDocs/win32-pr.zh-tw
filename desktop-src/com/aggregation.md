---
title: 彙總
description: 「匯總」是物件重複使用機制，在此機制中，外部物件會從內建物件公開介面，如同它們是在外部物件本身上執行一樣。
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a4f11f69f5d7b14047a8138cba93bd503b645a3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316534"
---
# <a name="aggregation"></a><span data-ttu-id="2fd86-103">彙總</span><span class="sxs-lookup"><span data-stu-id="2fd86-103">Aggregation</span></span>

<span data-ttu-id="2fd86-104">「匯總」是物件重複使用機制，在此機制中，外部物件會從內建物件公開介面，如同它們是在外部物件本身上執行一樣。</span><span class="sxs-lookup"><span data-stu-id="2fd86-104">Aggregation is the object reuse mechanism in which the outer object exposes interfaces from the inner object as if they were implemented on the outer object itself.</span></span> <span data-ttu-id="2fd86-105">當外部物件將其其中一個介面的每個呼叫委派給內建物件中的相同介面時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="2fd86-105">This is useful when the outer object delegates every call to one of its interfaces to the same interface in the inner object.</span></span> <span data-ttu-id="2fd86-106">為了方便起見，在此情況下，您可以使用匯總來避免外部物件產生額外的實負荷。</span><span class="sxs-lookup"><span data-stu-id="2fd86-106">Aggregation is available as a convenience to avoid extra implementation overhead in the outer object in this case.</span></span> <span data-ttu-id="2fd86-107">匯總實際上是內含專案 [/委派](containment-delegation.md)的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="2fd86-107">Aggregation is actually a specialized case of [containment/delegation](containment-delegation.md).</span></span>

<span data-ttu-id="2fd86-108">匯總幾乎就像內含專案一樣簡單，但三個 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 函數除外： [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="2fd86-108">Aggregation is almost as simple to implement as containment is, except for the three [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="2fd86-109">捕捉是從用戶端的觀點來看，外部物件上的任何 **IUnknown** 函數都必須影響外部物件。</span><span class="sxs-lookup"><span data-stu-id="2fd86-109">The catch is that from the client's perspective, any **IUnknown** function on the outer object must affect the outer object.</span></span> <span data-ttu-id="2fd86-110">也就是說， **AddRef** 和 **Release** 會影響外部物件，而 **QueryInterface** 會公開外部物件上所有可用的介面。</span><span class="sxs-lookup"><span data-stu-id="2fd86-110">That is, **AddRef** and **Release** affect the outer object and **QueryInterface** exposes all the interfaces available on the outer object.</span></span> <span data-ttu-id="2fd86-111">但是，如果外部物件直接公開內建物件的介面，則透過該介面呼叫的內建物件的 **iunknown** 成員將會與外部物件介面上的 **iunknown** 成員有不同的行為，即為管理 **IUnknown** 的規則和屬性絕對違規。</span><span class="sxs-lookup"><span data-stu-id="2fd86-111">However, if the outer object simply exposes an inner object's interface as its own, that inner object's **IUnknown** members called through that interface will behave differently than those **IUnknown** members on the outer object's interfaces, an absolute violation of the rules and properties governing **IUnknown**.</span></span>

<span data-ttu-id="2fd86-112">解決方法是，匯總需要在內建物件上明確執行 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ，以及將任何其他介面的 **iunknown** 方法委派給外部物件的 **iunknown** 方法。</span><span class="sxs-lookup"><span data-stu-id="2fd86-112">The solution is that aggregation requires an explicit implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) on the inner object and delegation of the **IUnknown** methods of any other interface to the outer object's **IUnknown** methods.</span></span>

## <a name="creating-aggregable-objects"></a><span data-ttu-id="2fd86-113">建立 Aggregable 物件</span><span class="sxs-lookup"><span data-stu-id="2fd86-113">Creating Aggregable Objects</span></span>

<span data-ttu-id="2fd86-114">建立可以匯總的物件是選擇性的;不過，這麼做很簡單，並提供顯著的優點。</span><span class="sxs-lookup"><span data-stu-id="2fd86-114">Creating objects that can be aggregated is optional; however, it is simple to do and provides significant benefits.</span></span> <span data-ttu-id="2fd86-115">下列規則適用于建立 aggregable 物件：</span><span class="sxs-lookup"><span data-stu-id="2fd86-115">The following rules apply to creating an aggregable object:</span></span>

-   <span data-ttu-id="2fd86-116">Aggregable (或內部) 物件對其 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面 [](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))控制內建物件的參考 [**計數，且**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)此實作為控制 **iunknown**) 的外部物件未知 (的實 [**作為。**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="2fd86-116">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface controls the inner object's reference count, and this implementation must not delegate to the outer object's unknown (the controlling **IUnknown**).</span></span>
-   <span data-ttu-id="2fd86-117">Aggregable (或內部) 物件對其其他介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 執行必須委派給控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ，而且不能直接影響內建物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="2fd86-117">The aggregable (or inner) object's implementation of [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) for its other interfaces must delegate to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and must not directly affect the inner object's reference count.</span></span>
-   <span data-ttu-id="2fd86-118">內部 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 必須只針對內建物件執行 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="2fd86-118">The inner [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) must implement [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) only for the inner object.</span></span>
-   <span data-ttu-id="2fd86-119">保存控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)指標的參考時，aggregable 物件不能呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 。</span><span class="sxs-lookup"><span data-stu-id="2fd86-119">The aggregable object must not call [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) when holding a reference to the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="2fd86-120">當建立物件時，如果要求 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 以外的任何介面，則建立必須失敗並出現 E \_ NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="2fd86-120">When the object is created, if any interface other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) is requested, the creation must fail with E\_NOINTERFACE.</span></span>

<span data-ttu-id="2fd86-121">下列程式碼片段會使用實介面的嵌套類別方法，說明 aggregable 物件的正確執行：</span><span class="sxs-lookup"><span data-stu-id="2fd86-121">The following code fragment illustrates a correct implementation of an aggregable object by using the nested class method of implementing interfaces:</span></span>


```C++
// CSomeObject is an aggregable object that implements 
// IUnknown and ISomeInterface 
class CSomeObject : public IUnknown 
{ 
    private: 
        DWORD        m_cRef;         // Object reference count 
        IUnknown*    m_pUnkOuter;    // Controlling IUnknown, no AddRef 
 
        // Nested class to implement the ISomeInterface interface 
        class CImpSomeInterface : public ISomeInterface 
        { 
            friend class CSomeObject ; 
            private: 
                DWORD    m_cRef;    // Interface ref-count, for debugging 
                IUnknown*    m_pUnkOuter;    // Controlling IUnknown 
            public: 
                CImpSomeInterface() { m_cRef = 0;   }; 
                ~ CImpSomeInterface(void) {}; 
 
                // IUnknown members delegate to the outer unknown 
                // IUnknown members do not control lifetime of object 
                STDMETHODIMP     QueryInterface(REFIID riid, void** ppv) 
                {    return m_pUnkOuter->QueryInterface(riid,ppv);   }; 
 
                STDMETHODIMP_(DWORD) AddRef(void) 
                {    return m_pUnkOuter->AddRef();   }; 
 
                STDMETHODIMP_(DWORD) Release(void) 
                {    return m_pUnkOuter->Release();   }; 
 
                // ISomeInterface members 
                STDMETHODIMP SomeMethod(void) 
                {    return S_OK;   }; 
        } ; 
        CImpSomeInterface m_ImpSomeInterface ; 
    public: 
        CSomeObject(IUnknown * pUnkOuter) 
        { 
            m_cRef=0; 
            // No AddRef necessary if non-NULL as we're aggregated. 
            m_pUnkOuter=pUnkOuter; 
            m_ImpSomeInterface.m_pUnkOuter=pUnkOuter; 
        } ; 
        ~CSomeObject(void) {} ; 
 
        // Static member function for creating new instances (don't use 
        // new directly). Protects against outer objects asking for 
        // interfaces other than Iunknown. 
        static HRESULT Create(IUnknown* pUnkOuter, REFIID riid, void **ppv) 
        { 
            CSomeObject*        pObj; 
            if (pUnkOuter != NULL && riid != IID_IUnknown) 
                return CLASS_E_NOAGGREGATION; 
            pObj = new CSomeObject(pUnkOuter); 
            if (pObj == NULL) 
                return E_OUTOFMEMORY; 
            // Set up the right unknown for delegation (the non-
            // aggregation case) 
            if (pUnkOuter == NULL) 
            {
                pObj->m_pUnkOuter = (IUnknown*)pObj ; 
                pObj->m_ImpSomeInterface.m_pUnkOuter = (IUnknown*)pObj;
            }
            HRESULT hr; 
            if (FAILED(hr = pObj->QueryInterface(riid, (void**)ppv))) 
                delete pObj ; 
            return hr; 
        } 
 
        // Inner IUnknown members, non-delegating 
        // Inner QueryInterface only controls inner object 
        STDMETHODIMP QueryInterface(REFIID riid, void** ppv) 
        { 
            *ppv=NULL; 
            if (riid == IID_IUnknown) 
                *ppv=this; 
            if (riid == IID_ISomeInterface) 
                *ppv=&m_ImpSomeInterface; 
            if (NULL==*ppv) 
                return ResultFromScode(E_NOINTERFACE); 
            ((IUnknown*)*ppv)->AddRef(); 
            return NOERROR; 
        } ; 
        STDMETHODIMP_(DWORD) AddRef(void) 
        {    return ++m_cRef; }; 
        STDMETHODIMP_(DWORD) Release(void) 
        { 
            if (--m_cRef != 0) 
                return m_cRef; 
            delete this; 
            return 0; 
        }; 
}; 
 
```



## <a name="aggregating-objects"></a><span data-ttu-id="2fd86-122">匯總物件</span><span class="sxs-lookup"><span data-stu-id="2fd86-122">Aggregating Objects</span></span>

<span data-ttu-id="2fd86-123">開發 aggregable 物件時，適用下列規則：</span><span class="sxs-lookup"><span data-stu-id="2fd86-123">When developing an aggregable object, the following rules apply:</span></span>

-   <span data-ttu-id="2fd86-124">建立內建物件時，外部物件必須明確地要求其 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)。</span><span class="sxs-lookup"><span data-stu-id="2fd86-124">When creating the inner object, the outer object must explicitly ask for its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="2fd86-125">外部物件必須保護其 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 的執行，以在其終結程式碼周圍具有人工參考計數。</span><span class="sxs-lookup"><span data-stu-id="2fd86-125">The outer object must protect its implementation of [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) from reentrancy with an artificial reference count around its destruction code.</span></span>
-   <span data-ttu-id="2fd86-126">如果外部物件查詢任何內建物件介面的指標，則必須呼叫其控制 **IUnknown** [**釋放**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法。</span><span class="sxs-lookup"><span data-stu-id="2fd86-126">The outer object must call its controlling **IUnknown** [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method if it queries for a pointer to any of the inner object's interfaces.</span></span> <span data-ttu-id="2fd86-127">若要釋放這個指標，外部物件會呼叫其控制 **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 方法，然後在內建物件的指標上 **放開** 。</span><span class="sxs-lookup"><span data-stu-id="2fd86-127">To free this pointer, the outer object calls its controlling **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method, followed by **Release** on the inner object's pointer.</span></span>
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   <span data-ttu-id="2fd86-128">外部物件不能將任何無法辨識之介面的查詢盲目委派給內建物件，除非該行為特別是外部物件的目的。</span><span class="sxs-lookup"><span data-stu-id="2fd86-128">The outer object must not blindly delegate a query for any unrecognized interface to the inner object, unless that behavior is specifically the intention of the outer object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fd86-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fd86-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd86-130">內含專案/委派</span><span class="sxs-lookup"><span data-stu-id="2fd86-130">Containment/Delegation</span></span>](containment-delegation.md)
</dt> </dl>

 

 