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
# <a name="how-iunknown-works"></a><span data-ttu-id="38fd8-103">IUnknown 的運作方式</span><span class="sxs-lookup"><span data-stu-id="38fd8-103">How IUnknown Works</span></span>

<span data-ttu-id="38fd8-104">**IUnknown** 中的方法可讓應用程式查詢元件上的介面，以及管理元件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="38fd8-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="38fd8-105">**參考計數**</span><span class="sxs-lookup"><span data-stu-id="38fd8-105">**Reference Count**</span></span>

<span data-ttu-id="38fd8-106">參考計數是在 **AddRef** 方法中遞增的內部變數，在 **Release** 方法中會遞減。</span><span class="sxs-lookup"><span data-stu-id="38fd8-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="38fd8-107">基類會管理參考計數，並同步處理多個執行緒之間參考計數的存取。</span><span class="sxs-lookup"><span data-stu-id="38fd8-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="38fd8-108">**介面查詢**</span><span class="sxs-lookup"><span data-stu-id="38fd8-108">**Interface Queries**</span></span>

<span data-ttu-id="38fd8-109">查詢介面也很簡單。</span><span class="sxs-lookup"><span data-stu-id="38fd8-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="38fd8-110">呼叫端會傳遞兩個參數：介面識別碼 (IID) 和指標的位址。</span><span class="sxs-lookup"><span data-stu-id="38fd8-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="38fd8-111">如果元件支援要求的介面，它會將指標設定為介面、遞增其本身的參考計數，然後傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="38fd8-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="38fd8-112">否則，它會將指標設定為 **Null** ，並傳回 E \_ NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="38fd8-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="38fd8-113">下列虛擬程式碼會顯示 **QueryInterface** 方法的一般大綱。</span><span class="sxs-lookup"><span data-stu-id="38fd8-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="38fd8-114">下一節所述的元件匯總會帶來一些額外的複雜性。</span><span class="sxs-lookup"><span data-stu-id="38fd8-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


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



<span data-ttu-id="38fd8-115">其中一個元件的 **queryinterface** 方法和另一個元件的 **queryinterface** 方法之間的唯一差異，就是每個元件測試的 iid 清單。</span><span class="sxs-lookup"><span data-stu-id="38fd8-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="38fd8-116">對於元件支援的每個介面，元件必須測試該介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="38fd8-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="38fd8-117">**匯總和委派**</span><span class="sxs-lookup"><span data-stu-id="38fd8-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="38fd8-118">呼叫端的元件匯總必須是透明的。</span><span class="sxs-lookup"><span data-stu-id="38fd8-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="38fd8-119">因此，匯總必須公開單一 **IUnknown** 介面，且匯總的元件會延後至外部元件的實作為。</span><span class="sxs-lookup"><span data-stu-id="38fd8-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="38fd8-120">否則，呼叫端會在同一個匯總中看到兩個不同的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="38fd8-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="38fd8-121">如果元件未匯總，則會使用它自己的實作為。</span><span class="sxs-lookup"><span data-stu-id="38fd8-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="38fd8-122">若要支援此行為，元件必須加入間接取值層級。</span><span class="sxs-lookup"><span data-stu-id="38fd8-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="38fd8-123">*委派的 IUnknown* 會將工作委派給適當的位置：外部元件（如果有的話），或元件的內部版本。</span><span class="sxs-lookup"><span data-stu-id="38fd8-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="38fd8-124">*Nondelegating IUnknown* 會執行工作，如上一節中所述。</span><span class="sxs-lookup"><span data-stu-id="38fd8-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="38fd8-125">委派的版本是公用的，而且會保留名稱 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="38fd8-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="38fd8-126">Nondelegating 版本已重新命名為 [**INonDelegatingUnknown**](inondelegatingunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="38fd8-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="38fd8-127">此名稱不是 COM 規格的一部分，因為它不是公用介面。</span><span class="sxs-lookup"><span data-stu-id="38fd8-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="38fd8-128">當用戶端建立元件的實例時，會呼叫 **IClassFactory：： CreateInstance** 方法。</span><span class="sxs-lookup"><span data-stu-id="38fd8-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="38fd8-129">其中一個參數是匯總元件之 **IUnknown** 介面的指標，如果未匯總新的實例，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="38fd8-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="38fd8-130">元件會使用這個參數來儲存成員變數，以指出要使用的 **IUnknown** 介面，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="38fd8-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


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



<span data-ttu-id="38fd8-131">委派 **IUnknown** 中的每個方法都會呼叫其 nondelegating 對應項，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="38fd8-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="38fd8-132">根據委派的本質，委派的方法在每個元件中看起來都一樣。</span><span class="sxs-lookup"><span data-stu-id="38fd8-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="38fd8-133">只有 nondelegating 版本會變更。</span><span class="sxs-lookup"><span data-stu-id="38fd8-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38fd8-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="38fd8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38fd8-135">如何執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="38fd8-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



