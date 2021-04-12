---
title: 解析函數名稱衝突的範例
description: 本主題說明如何在建立 ADSI 的延伸模組時解決函式名稱衝突。
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，範例程式碼 Visual Basic，解析函數名稱衝突
- 解決函式名稱衝突 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316465"
---
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="e418d-105">解析函數名稱衝突的範例</span><span class="sxs-lookup"><span data-stu-id="e418d-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="e418d-106">請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="e418d-106">Consider the following:</span></span>

-   <span data-ttu-id="e418d-107">IADs0 不支援 Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="e418d-108">IADs1 支援 Func1 和 Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="e418d-109">IADs2 支援 Func2 和 Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="e418d-110">這三個介面都是雙重介面。</span><span class="sxs-lookup"><span data-stu-id="e418d-110">All three interfaces are dual interfaces.</span></span>


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



<span data-ttu-id="e418d-111">請注意，雖然 IADs1 不支援 Func2，但 ADSI 用戶端會辨識一個支援模型中所有雙重和分派介面的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 。</span><span class="sxs-lookup"><span data-stu-id="e418d-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="e418d-112">因此，ADSI 用戶端可以使用 myInf1 直接呼叫 Func2，而不需解析支援 Func2 的介面。</span><span class="sxs-lookup"><span data-stu-id="e418d-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="e418d-113">IADs1 和 IADs2 都有一個稱為 Func0 的函式，但 IADs1：： Func0 是直接使用 vtable 存取來叫用，因為下列兩項都適用于用戶端：</span><span class="sxs-lookup"><span data-stu-id="e418d-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="e418d-114">用戶端有一個指向雙重介面 IADs1 物件的指標，該物件具有稱為 Func0 的函式。</span><span class="sxs-lookup"><span data-stu-id="e418d-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="e418d-115">Visual Basic 支援直接 vtable 存取，並假設資料類型可透過類型程式庫取得。</span><span class="sxs-lookup"><span data-stu-id="e418d-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="e418d-116">在下一個程式碼範例中，用戶端有一個 IADs2 的雙重介面指標，而不是 IADs1。</span><span class="sxs-lookup"><span data-stu-id="e418d-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="e418d-117">因此，IADs2：： Func0 是使用直接 vtable 存取來叫用的。</span><span class="sxs-lookup"><span data-stu-id="e418d-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="e418d-118">同樣地，在下一個程式碼範例中，IADs1 和 IADs2 都有一個稱為 Func0 的函式，但在這裡，用戶端有一個指向雙重介面 IADs0 的指標，該函式沒有稱為 Func0 的函式。</span><span class="sxs-lookup"><span data-stu-id="e418d-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="e418d-119">因此，不能執行直接 vtable 存取。</span><span class="sxs-lookup"><span data-stu-id="e418d-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="e418d-120">相反地，會呼叫 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 來叫用 Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="e418d-121">請考慮下列兩個案例：</span><span class="sxs-lookup"><span data-stu-id="e418d-121">Consider these two cases:</span></span>

-   <span data-ttu-id="e418d-122">IADs1 和 IADs2 分別由兩個 COM 元件（Ext1 和 Ext2）來執行。</span><span class="sxs-lookup"><span data-stu-id="e418d-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="e418d-123">如果 Ext1 在登錄中 Ext2 之前，則會叫用 IADs1：： Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="e418d-124">但是，如果 Ext2 在登錄中最先出現，則會叫用 IADs2：： Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="e418d-125">如果 IADs1 和 ADs2 是由相同的擴充物件所執行，則一律會由擴充功能的 [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 和 [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) 方法來叫用 Func0。</span><span class="sxs-lookup"><span data-stu-id="e418d-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="e418d-126">延伸模組開發人員必須判斷如何解決在擴充功能中具有相同名稱之不同雙重 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面的函式或屬性衝突。</span><span class="sxs-lookup"><span data-stu-id="e418d-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="e418d-127">[**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)和 [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke)方法的執行應該可解決此衝突。</span><span class="sxs-lookup"><span data-stu-id="e418d-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="e418d-128">例如，如果您使用 IMyInterface1：： Func1 和 IMyInterface2：： Func1，其中 IMyInterface1 和 IMyInterface2 是相同擴充物件所支援的雙重 **IDispatch** 介面。</span><span class="sxs-lookup"><span data-stu-id="e418d-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="e418d-129">**PrivateGetIDsOfNames** 和 **PrivateInvoke** 方法必須決定應一律呼叫的 Func1。</span><span class="sxs-lookup"><span data-stu-id="e418d-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="e418d-130">這同樣適用于不同的雙重或 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面中的衝突 dispid。</span><span class="sxs-lookup"><span data-stu-id="e418d-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="e418d-131">例如，IMyInterface1. odl 或 IMyInterface1 中的 DISPID IMyInterface1：： Y 是2。</span><span class="sxs-lookup"><span data-stu-id="e418d-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="e418d-132">IMyInterface2：： X 的 DISPID 也是 iMyInterface2. odl 中的2。</span><span class="sxs-lookup"><span data-stu-id="e418d-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="e418d-133">[**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 必須在延伸模組本身內傳回唯一的 dispid，而不是針對兩者傳回相同的 dispid。</span><span class="sxs-lookup"><span data-stu-id="e418d-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="e418d-134">ADSI 藉由不支援具有衝突函式或屬性名稱的多個介面，來解決第一個問題。</span><span class="sxs-lookup"><span data-stu-id="e418d-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="e418d-135">它會解決第二個問題，方法是將唯一的（位於相同的延伸模組物件內）介面編號新增至 DISPID 未使用的位。</span><span class="sxs-lookup"><span data-stu-id="e418d-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 