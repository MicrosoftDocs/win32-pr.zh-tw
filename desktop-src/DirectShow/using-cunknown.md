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
# <a name="using-cunknown"></a><span data-ttu-id="5586d-103">使用 CUnknown</span><span class="sxs-lookup"><span data-stu-id="5586d-103">Using CUnknown</span></span>

<span data-ttu-id="5586d-104">DirectShow 會在名為 [**CUnknown**](cunknown.md)的基類中實行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。</span><span class="sxs-lookup"><span data-stu-id="5586d-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="5586d-105">您可以使用 **CUnknown** 來衍生其他類別，只覆寫在各元件之間變更的方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="5586d-106">DirectShow 中大部分的其他基類都衍生自 **CUnknown**，因此您的元件可以直接從 **CUnknown** 或從其他基類繼承。</span><span class="sxs-lookup"><span data-stu-id="5586d-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="5586d-107">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="5586d-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="5586d-108">[**CUnknown**](cunknown.md) 會實行 [**INonDelegatingUnknown**](inondelegatingunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="5586d-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="5586d-109">它會在內部管理參考計數，而且在大多數情況下，您的衍生類別可以繼承兩個參考計數方法，而不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="5586d-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="5586d-110">請注意，當參考計數降至零時， **CUnknown** 就會刪除本身。</span><span class="sxs-lookup"><span data-stu-id="5586d-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="5586d-111">另一方面，您必須覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md)，因為基類中的方法 \_ 會在收到 iid IUnknown 以外的任何 Iid 時傳回 E NOINTERFACE \_ 。</span><span class="sxs-lookup"><span data-stu-id="5586d-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="5586d-112">在您的衍生類別中，測試您支援的介面 Iid，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="5586d-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


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



<span data-ttu-id="5586d-113">公用程式函式 [**GetInterface**](getinterface.md) (參閱 [**COM**](com-helper-functions.md) 協助程式函式) 設定指標，以安全線程的方式遞增參考計數，然後傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5586d-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="5586d-114">在預設案例中，呼叫基類方法並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="5586d-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="5586d-115">如果您是從另一個基類衍生，請改為呼叫其 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="5586d-116">這可讓您支援父類別支援的所有介面。</span><span class="sxs-lookup"><span data-stu-id="5586d-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="5586d-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="5586d-117">IUnknown</span></span>

<span data-ttu-id="5586d-118">如先前所述，每個元件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 委派版本都是相同的，因為它只會叫用正確的 nondelegating 版本實例。</span><span class="sxs-lookup"><span data-stu-id="5586d-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="5586d-119">為了方便起見，標頭檔 Combase 包含宏，宣告 [**\_ IUNKNOWN**](declare-iunknown.md)，這會將三個委派的方法宣告為內嵌方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="5586d-120">它會擴充至下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="5586d-120">It expands to the following code:</span></span>


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



<span data-ttu-id="5586d-121">公用程式函式 [**CUnknown：： GetOwner**](cunknown-getowner.md) 會抓取擁有此元件之元件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="5586d-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="5586d-122">針對匯總的元件，擁有者是外部元件。</span><span class="sxs-lookup"><span data-stu-id="5586d-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="5586d-123">否則，元件擁有本身。</span><span class="sxs-lookup"><span data-stu-id="5586d-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="5586d-124">\_在您類別定義的公用區段中包含 DECLARE IUNKNOWN 宏。</span><span class="sxs-lookup"><span data-stu-id="5586d-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="5586d-125">類別建構函式</span><span class="sxs-lookup"><span data-stu-id="5586d-125">Class Constructor</span></span>

<span data-ttu-id="5586d-126">類別的函式除了針對您的類別所特有的任何作業之外，還應該叫用父類別的函式方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="5586d-127">下列範例是典型的函式方法：</span><span class="sxs-lookup"><span data-stu-id="5586d-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="5586d-128">方法會使用下列參數，而這些參數會直接傳遞給 [**CUnknown**](cunknown.md) 的方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="5586d-129">*tszName* 指定元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="5586d-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="5586d-130">*pUnk* 是匯總 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)的指標。</span><span class="sxs-lookup"><span data-stu-id="5586d-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="5586d-131">*pHr* 是 HRESULT 值的指標，表示方法成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="5586d-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="5586d-132">總結</span><span class="sxs-lookup"><span data-stu-id="5586d-132">Summary</span></span>

<span data-ttu-id="5586d-133">下列範例顯示支援 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 的衍生類別，以及名為 ISomeInterface 的假設介面：</span><span class="sxs-lookup"><span data-stu-id="5586d-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


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



<span data-ttu-id="5586d-134">此範例說明下列幾點：</span><span class="sxs-lookup"><span data-stu-id="5586d-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="5586d-135">[**CUnknown**](cunknown.md)類別會實作為 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5586d-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5586d-136">新的元件會繼承自元件所支援的 **CUnknown** 和任何介面。</span><span class="sxs-lookup"><span data-stu-id="5586d-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="5586d-137">元件可以改為衍生自繼承自 **CUnknown** 的另一個基類。</span><span class="sxs-lookup"><span data-stu-id="5586d-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="5586d-138">[**DECLARE \_ iunknown**](declare-iunknown.md)宏會將委派 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法宣告為內嵌方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="5586d-139">[**CUnknown**](cunknown.md)類別提供 [**INonDelegatingUnknown**](inondelegatingunknown.md)的實作為。</span><span class="sxs-lookup"><span data-stu-id="5586d-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="5586d-140">為了支援 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)以外的介面，衍生類別必須覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法，並測試新介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="5586d-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="5586d-141">類別的函式會叫用 [**CUnknown**](cunknown.md)的函式方法。</span><span class="sxs-lookup"><span data-stu-id="5586d-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="5586d-142">撰寫篩選的下一個步驟是讓應用程式建立元件的新實例。</span><span class="sxs-lookup"><span data-stu-id="5586d-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="5586d-143">這需要瞭解 Dll 及其與 class factory 和類別的函式方法的關聯。</span><span class="sxs-lookup"><span data-stu-id="5586d-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="5586d-144">如需詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="5586d-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5586d-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="5586d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5586d-146">如何執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="5586d-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 
