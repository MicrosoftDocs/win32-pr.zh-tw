---
description: IUnknown 的運作方式
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: IUnknown 的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108472"
---
# <a name="how-iunknown-works"></a>IUnknown 的運作方式

**IUnknown** 中的方法可讓應用程式查詢元件上的介面，以及管理元件的參考計數。

**參考計數**

參考計數是在 **AddRef** 方法中遞增的內部變數，在 **Release** 方法中會遞減。 基類會管理參考計數，並同步處理多個執行緒之間參考計數的存取。

**介面查詢**

查詢介面也很簡單。 呼叫端會傳遞兩個參數：介面識別碼 (IID) 和指標的位址。 如果元件支援要求的介面，它會將指標設定為介面、遞增其本身的參考計數，然後傳回 \_ [確定]。 否則，它會將指標設定為 **Null** ，並傳回 E \_ NOINTERFACE。 下列虛擬程式碼會顯示 **QueryInterface** 方法的一般大綱。 下一節所述的元件匯總會帶來一些額外的複雜性。


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



其中一個元件的 **queryinterface** 方法和另一個元件的 **queryinterface** 方法之間的唯一差異，就是每個元件測試的 iid 清單。 對於元件支援的每個介面，元件必須測試該介面的 IID。

**匯總和委派**

呼叫端的元件匯總必須是透明的。 因此，匯總必須公開單一 **IUnknown** 介面，且匯總的元件會延後至外部元件的實作為。 否則，呼叫端會在同一個匯總中看到兩個不同的 **IUnknown** 介面。 如果元件未匯總，則會使用它自己的實作為。

若要支援此行為，元件必須加入間接取值層級。 *委派的 IUnknown* 會將工作委派給適當的位置：外部元件（如果有的話），或元件的內部版本。 *Nondelegating IUnknown* 會執行工作，如上一節中所述。

委派的版本是公用的，而且會保留名稱 **IUnknown**。 Nondelegating 版本已重新命名為 [**INonDelegatingUnknown**](inondelegatingunknown.md)。 此名稱不是 COM 規格的一部分，因為它不是公用介面。

當用戶端建立元件的實例時，會呼叫 **IClassFactory：： CreateInstance** 方法。 其中一個參數是匯總元件之 **IUnknown** 介面的指標，如果未匯總新的實例，則為 **Null** 。 元件會使用這個參數來儲存成員變數，以指出要使用的 **IUnknown** 介面，如下列範例所示：


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



委派 **IUnknown** 中的每個方法都會呼叫其 nondelegating 對應項，如下列範例所示：


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



根據委派的本質，委派的方法在每個元件中看起來都一樣。 只有 nondelegating 版本會變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何執行 IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



