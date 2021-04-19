---
title: 執行 QueryInterface 的規則
description: 執行 QueryInterface 的規則
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106999593"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="49c93-103">執行 QueryInterface 的規則</span><span class="sxs-lookup"><span data-stu-id="49c93-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="49c93-104">有三個主要規則會管理 COM 物件的 [**IUnknown：： QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法：</span><span class="sxs-lookup"><span data-stu-id="49c93-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="49c93-105">物件必須有身分識別。</span><span class="sxs-lookup"><span data-stu-id="49c93-105">Objects must have identity.</span></span>
-   <span data-ttu-id="49c93-106">物件實例上的介面集合必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="49c93-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="49c93-107">您必須能夠成功地從任何其他介面針對物件上的任何介面進行查詢。</span><span class="sxs-lookup"><span data-stu-id="49c93-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="49c93-108">物件必須有身分識別</span><span class="sxs-lookup"><span data-stu-id="49c93-108">Objects Must Have Identity</span></span>

<span data-ttu-id="49c93-109">對於任何指定的物件實例，對具有 IID IUnknown 的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫 \_ 都必須一律傳回相同的實體指標值。</span><span class="sxs-lookup"><span data-stu-id="49c93-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="49c93-110">這可讓您在任何兩個介面上呼叫 **QueryInterface** 並比較結果，以判斷它們是否指向相同的物件實例。</span><span class="sxs-lookup"><span data-stu-id="49c93-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="49c93-111">物件實例上的介面集合必須是靜態的</span><span class="sxs-lookup"><span data-stu-id="49c93-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="49c93-112">透過 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 可在物件上存取的介面集必須是靜態的，而非動態的。</span><span class="sxs-lookup"><span data-stu-id="49c93-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="49c93-113">明確地說 ，如果 queryinterface \_ 針對指定的 iid 傳回 S OK，則在相同物件上的後續呼叫中，它永遠不會傳回 e \_ NOINTERFACE; 而如果 **Queryinterface** \_ 傳回指定 iid 的 e NOINTERFACE，則在相同物件上對相同 IID 的後續呼叫絕不能傳回 S \_ ok。</span><span class="sxs-lookup"><span data-stu-id="49c93-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="49c93-114">您必須能夠成功地從任何其他介面針對物件上的任何介面進行查詢</span><span class="sxs-lookup"><span data-stu-id="49c93-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="49c93-115">亦即，假設有下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="49c93-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="49c93-116">適用下列規則：</span><span class="sxs-lookup"><span data-stu-id="49c93-116">the following rules apply:</span></span>

-   <span data-ttu-id="49c93-117">如果您有物件介面的指標，則對相同介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 進行的呼叫必須成功：</span><span class="sxs-lookup"><span data-stu-id="49c93-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="49c93-118">如果對第二個介面指標的 [**queryinterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫成功，則從該指標對第一個介面進行的 **queryinterface** 呼叫也必須成功。</span><span class="sxs-lookup"><span data-stu-id="49c93-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="49c93-119">如果已成功取得 pB，則下列也必須成功：</span><span class="sxs-lookup"><span data-stu-id="49c93-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="49c93-120">任何介面都必須能夠查詢物件上的任何其他介面。</span><span class="sxs-lookup"><span data-stu-id="49c93-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="49c93-121">如果已成功取得 pB，且您已使用該指標成功查詢第三個介面 (內部) ，您也必須能夠使用第一個指標 pA 來成功查詢內部。</span><span class="sxs-lookup"><span data-stu-id="49c93-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="49c93-122">在此情況下，下列順序必須成功：</span><span class="sxs-lookup"><span data-stu-id="49c93-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="49c93-123">介面執行必須維持對指定物件上所有介面之未完成指標參考的計數器。</span><span class="sxs-lookup"><span data-stu-id="49c93-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="49c93-124">您應該為計數器使用 **不帶正負號的整數** 。</span><span class="sxs-lookup"><span data-stu-id="49c93-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="49c93-125">如果用戶端需要知道資源已經釋出，它必須在呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)之前，在具有較高層級語義的物件上的某個介面中使用方法。</span><span class="sxs-lookup"><span data-stu-id="49c93-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49c93-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="49c93-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49c93-127">使用和執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="49c93-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 