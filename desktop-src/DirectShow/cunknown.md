---
description: CUnknown 類別會實作為 IUnknown 介面。 大部分的元件物件模型 (DirectShow 中的 COM) 物件衍生自 CUnknown。
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: 'CUnknown 類別 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001846"
---
# <a name="cunknown-class"></a><span data-ttu-id="a949b-104">CUnknown 類別</span><span class="sxs-lookup"><span data-stu-id="a949b-104">CUnknown class</span></span>

![cunknown 類別階層](images/cbase01.png)

<span data-ttu-id="a949b-106">**CUnknown** 類別會實作為 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="a949b-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="a949b-107">大部分的元件物件模型 (DirectShow 中的 COM) 物件衍生自 **CUnknown**。</span><span class="sxs-lookup"><span data-stu-id="a949b-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="a949b-108">如果您執行的是 COM 物件，您可能會想要從 **CUnknown** 衍生。</span><span class="sxs-lookup"><span data-stu-id="a949b-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="a949b-109">衍生自 **CUnknown** 可提供安全線程的執行，並可讓您省下執行 **IUnknown** 的麻煩。</span><span class="sxs-lookup"><span data-stu-id="a949b-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="a949b-110">如需如何使用此基類的詳細討論，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="a949b-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="a949b-111">以下是簡短摘要：</span><span class="sxs-lookup"><span data-stu-id="a949b-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="a949b-112">在您類別定義的公用區段中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="a949b-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="a949b-113">此宏會宣告 **IUnknown** 介面的三種方法。</span><span class="sxs-lookup"><span data-stu-id="a949b-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="a949b-114">覆寫 [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) 方法以支援 **IUnknown** 以外的介面。</span><span class="sxs-lookup"><span data-stu-id="a949b-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="a949b-115">在這個方法中，呼叫 [**GetInterface**](getinterface.md) 函式來取出介面指標。</span><span class="sxs-lookup"><span data-stu-id="a949b-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="a949b-116">在類別的函式中，叫用 **CUnknown** 的方法。</span><span class="sxs-lookup"><span data-stu-id="a949b-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="a949b-117">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="a949b-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="a949b-118">Description</span><span class="sxs-lookup"><span data-stu-id="a949b-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a949b-119">**m \_ cRef**</span><span class="sxs-lookup"><span data-stu-id="a949b-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="a949b-120">參考計數。</span><span class="sxs-lookup"><span data-stu-id="a949b-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="a949b-121">公用方法</span><span class="sxs-lookup"><span data-stu-id="a949b-121">Public Methods</span></span>                                                              | <span data-ttu-id="a949b-122">Description</span><span class="sxs-lookup"><span data-stu-id="a949b-122">Description</span></span>                                                        |
| [<span data-ttu-id="a949b-123">**CUnknown**</span><span class="sxs-lookup"><span data-stu-id="a949b-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="a949b-124">函式方法。</span><span class="sxs-lookup"><span data-stu-id="a949b-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="a949b-125">**~ CUnknown**</span><span class="sxs-lookup"><span data-stu-id="a949b-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="a949b-126">函式方法。</span><span class="sxs-lookup"><span data-stu-id="a949b-126">Destructor method.</span></span> <span data-ttu-id="a949b-127">虛擬。</span><span class="sxs-lookup"><span data-stu-id="a949b-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="a949b-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="a949b-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="a949b-129">取得控制 **IUnknown** 的指標。</span><span class="sxs-lookup"><span data-stu-id="a949b-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="a949b-130">INonDelegatingUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="a949b-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="a949b-131">Description</span><span class="sxs-lookup"><span data-stu-id="a949b-131">Description</span></span>                                                        |
| [<span data-ttu-id="a949b-132">**NonDelegatingAddRef**</span><span class="sxs-lookup"><span data-stu-id="a949b-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="a949b-133">遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="a949b-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="a949b-134">**NonDelegatingQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="a949b-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="a949b-135">捕獲介面指標並遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="a949b-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="a949b-136">**NonDelegatingRelease**</span><span class="sxs-lookup"><span data-stu-id="a949b-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="a949b-137">遞減參考計數。</span><span class="sxs-lookup"><span data-stu-id="a949b-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="a949b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="a949b-138">Requirements</span></span>



| <span data-ttu-id="a949b-139">需求</span><span class="sxs-lookup"><span data-stu-id="a949b-139">Requirement</span></span> | <span data-ttu-id="a949b-140">值</span><span class="sxs-lookup"><span data-stu-id="a949b-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a949b-141">標頭</span><span class="sxs-lookup"><span data-stu-id="a949b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="a949b-142"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a949b-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a949b-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="a949b-143">Library</span></span><br/> | <dl> <span data-ttu-id="a949b-144"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a949b-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a949b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a949b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a949b-146">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="a949b-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




