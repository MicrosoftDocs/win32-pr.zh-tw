---
description: 支援多個回呼
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: 支援多個回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614d92a50101a5ed4e7c281dc76a3edce930fa06d68e11484dc89a3cad83de05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057703"
---
# <a name="supporting-multiple-callbacks"></a>支援多個回呼

如果您呼叫一個以上的非同步方法，每個方法都需要 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)的個別實作為。 不過，您可能想要在單一 c + + 類別內執行回呼。 類別只能有一個叫用 **方法，** 因此其中一個解決方案是提供協助程式類別，將 **Invoke** 呼叫委派給容器類別上的另一個方法。

下列程式碼會示範名為的類別範本 `AsyncCallback` ，它會示範這種方法。


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



範本參數是容器類別的名稱。 此函式 `AsyncCallback` 有兩個參數：容器類別的指標，以及容器類別上的回呼方法位址。 容器類別可以有多個類別的實例 `AsyncCallback` 做為成員變數，每個非同步方法一個。 當容器類別呼叫非同步方法時，它會使用適當物件的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面 `AsyncCallback` 。 `AsyncCallback`呼叫物件的 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)方法時，會將呼叫委派給容器類別上的正確方法。

此 `AsyncCallback` 物件也會將 **AddRef** 和 **Release** 呼叫委派給容器類別，讓容器類別管理物件的存留期 `AsyncCallback` 。 這可保證在 `AsyncCallback` 容器物件本身刪除之前，將不會刪除物件。

下列程式碼顯示如何使用此範本：


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



在此範例中，容器類別的名稱為 `CMyObject` 。 *M \_ CB* 成員變數是 `AsyncCallback` 物件。 在此函式中 `CMyObject` ，會使用方法的位址初始化 *m \_ CB* 成員變數 `CMyObject::OnInvoke` 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步回呼方法](asynchronous-callback-methods.md)
</dt> </dl>

 

 



