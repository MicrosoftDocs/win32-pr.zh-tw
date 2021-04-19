---
description: 本主題說明如何在 DirectShow 編輯服務中執行錯誤記錄。
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: 建立錯誤記錄類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972949"
---
# <a name="creating-an-error-logging-class"></a>建立錯誤記錄類別

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本主題說明如何在 [DirectShow 編輯服務](directshow-editing-services.md)中執行錯誤記錄。

首先，宣告將會執行錯誤記錄的類別。 類別會繼承 [**IAMErrorLog**](iamerrorlog.md) 介面。 它包含三個 **IUnknown** 方法的宣告，以及 [IAMErrorLog](implementing-iamerrorlog.md)中單一方法的宣告。 類別宣告如下所示：


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



類別中唯一的成員變數是 m \_ lRef，它會保存物件的參考計數。

接下來，在 **IUnknown** 中定義方法。 下列範例顯示這些方法的標準執行：


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



使用 COM 架構之後，您現在可以執行 **IAMErrorLog** 介面。 下一節將說明如何進行此操作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[記錄錯誤](logging-errors.md)
</dt> </dl>

 

 



