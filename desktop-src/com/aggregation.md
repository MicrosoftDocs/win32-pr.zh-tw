---
title: 彙總
description: 「匯總」是物件重複使用機制，在此機制中，外部物件會從內建物件公開介面，如同它們是在外部物件本身上執行一樣。
ms.assetid: 6845b114-8f43-47ad-acdf-b63d6008d221
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4855b1fa3a614d190b8f192aeee2e7cf3d3d53bbdce589a1363e0398f70430c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731718"
---
# <a name="aggregation"></a>彙總

「匯總」是物件重複使用機制，在此機制中，外部物件會從內建物件公開介面，如同它們是在外部物件本身上執行一樣。 當外部物件將其其中一個介面的每個呼叫委派給內建物件中的相同介面時，這會很有用。 為了方便起見，在此情況下，您可以使用匯總來避免外部物件產生額外的實負荷。 匯總實際上是內含專案 [/委派](containment-delegation.md)的特殊案例。

匯總幾乎就像內含專案一樣簡單，但三個 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 函數除外： [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。 捕捉是從用戶端的觀點來看，外部物件上的任何 **IUnknown** 函數都必須影響外部物件。 也就是說， **AddRef** 和 **Release** 會影響外部物件，而 **QueryInterface** 會公開外部物件上所有可用的介面。 但是，如果外部物件直接公開內建物件的介面，則透過該介面呼叫的內建物件的 **iunknown** 成員將會與外部物件介面上的 **iunknown** 成員有不同的行為，即為管理 **IUnknown** 的規則和屬性絕對違規。

解決方法是，匯總需要在內建物件上明確執行 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ，以及將任何其他介面的 **iunknown** 方法委派給外部物件的 **iunknown** 方法。

## <a name="creating-aggregable-objects"></a>建立 Aggregable 物件

建立可以匯總的物件是選擇性的;不過，這麼做很簡單，並提供顯著的優點。 下列規則適用于建立 aggregable 物件：

-   Aggregable (或內部) 物件對其 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面 [](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))控制內建物件的參考 [**計數，且**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)此實作為控制 **iunknown**) 的外部物件未知 (的實 [**作為。**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
-   Aggregable (或內部) 物件對其其他介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 執行必須委派給控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ，而且不能直接影響內建物件的參考計數。
-   內部 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 必須只針對內建物件執行 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 。
-   保存控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)指標的參考時，aggregable 物件不能呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 。
-   當建立物件時，如果要求 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 以外的任何介面，則建立必須失敗並出現 E \_ NOINTERFACE。

下列程式碼片段會使用實介面的嵌套類別方法，說明 aggregable 物件的正確執行：


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



## <a name="aggregating-objects"></a>匯總物件

開發 aggregable 物件時，適用下列規則：

-   建立內建物件時，外部物件必須明確地要求其 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)。
-   外部物件必須保護其 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 的執行，以在其終結程式碼周圍具有人工參考計數。
-   如果外部物件查詢任何內建物件介面的指標，則必須呼叫其控制 **IUnknown** [**釋放**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法。 若要釋放這個指標，外部物件會呼叫其控制 **IUnknown** [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 方法，然後在內建物件的指標上 **放開** 。
    ```C++
    // Obtaining inner object interface pointer 
    pUnkInner->QueryInterface(IID_ISomeInterface, &pISomeInterface); 
    pUnkOuter->Release(); 
     
    // Releasing inner object interface pointer 
    pUnkOuter->AddRef(); 
    pISomeInterface->Release(); 
     
    ```

    

-   外部物件不能將任何無法辨識之介面的查詢盲目委派給內建物件，除非該行為特別是外部物件的目的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[內含專案/委派](containment-delegation.md)
</dt> </dl>

 

 