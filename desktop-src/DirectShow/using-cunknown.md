---
description: DirectShow 會在名為 CUnknown 的基類中實行 IUnknown。
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: 使用 CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980373"
---
# <a name="using-cunknown"></a>使用 CUnknown

DirectShow 會在名為 [**CUnknown**](cunknown.md)的基類中實行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。 您可以使用 **CUnknown** 來衍生其他類別，只覆寫在各元件之間變更的方法。 DirectShow 中大部分的其他基類都衍生自 **CUnknown**，因此您的元件可以直接從 **CUnknown** 或從其他基類繼承。

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) 會實行 [**INonDelegatingUnknown**](inondelegatingunknown.md)。 它會在內部管理參考計數，而且在大多數情況下，您的衍生類別可以繼承兩個參考計數方法，而不會有任何變更。 請注意，當參考計數降至零時， **CUnknown** 就會刪除本身。 另一方面，您必須覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md)，因為基類中的方法 \_ 會在收到 iid IUnknown 以外的任何 Iid 時傳回 E NOINTERFACE \_ 。 在您的衍生類別中，測試您支援的介面 Iid，如下列範例所示：


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



公用程式函式 [**GetInterface**](getinterface.md) (參閱 [**COM**](com-helper-functions.md) 協助程式函式) 設定指標，以安全線程的方式遞增參考計數，然後傳回 S \_ OK。 在預設案例中，呼叫基類方法並傳回結果。 如果您是從另一個基類衍生，請改為呼叫其 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法。 這可讓您支援父類別支援的所有介面。

## <a name="iunknown"></a>IUnknown

如先前所述，每個元件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 委派版本都是相同的，因為它只會叫用正確的 nondelegating 版本實例。 為了方便起見，標頭檔 Combase 包含宏，宣告 [**\_ IUNKNOWN**](declare-iunknown.md)，這會將三個委派的方法宣告為內嵌方法。 它會擴充至下列程式碼：


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



公用程式函式 [**CUnknown：： GetOwner**](cunknown-getowner.md) 會抓取擁有此元件之元件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。 針對匯總的元件，擁有者是外部元件。 否則，元件擁有本身。 \_在您類別定義的公用區段中包含 DECLARE IUNKNOWN 宏。

## <a name="class-constructor"></a>類別建構函式

類別的函式除了針對您的類別所特有的任何作業之外，還應該叫用父類別的函式方法。 下列範例是典型的函式方法：


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



方法會使用下列參數，而這些參數會直接傳遞給 [**CUnknown**](cunknown.md) 的方法。

-   *tszName* 指定元件的名稱。
-   *pUnk* 是匯總 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)的指標。
-   *pHr* 是 HRESULT 值的指標，表示方法成功或失敗。

## <a name="summary"></a>總結

下列範例顯示支援 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 的衍生類別，以及名為 ISomeInterface 的假設介面：


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



此範例說明下列幾點：

-   [**CUnknown**](cunknown.md)類別會實作為 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 新的元件會繼承自元件所支援的 **CUnknown** 和任何介面。 元件可以改為衍生自繼承自 **CUnknown** 的另一個基類。
-   [**DECLARE \_ iunknown**](declare-iunknown.md)宏會將委派 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法宣告為內嵌方法。
-   [**CUnknown**](cunknown.md)類別提供 [**INonDelegatingUnknown**](inondelegatingunknown.md)的實作為。
-   為了支援 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)以外的介面，衍生類別必須覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法，並測試新介面的 IID。
-   類別的函式會叫用 [**CUnknown**](cunknown.md)的函式方法。

撰寫篩選的下一個步驟是讓應用程式建立元件的新實例。 這需要瞭解 Dll 及其與 class factory 和類別的函式方法的關聯。 如需詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何執行 IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
