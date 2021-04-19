---
description: 函式方法。
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: 'CBaseFilter. CBaseFilter (const TCHAR *、LPUNKNOWN、CCritSec*、REFCLSID、HRESULT * )  (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4d8806c9b4103c06eb58e11547e83fc933d5d3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994693"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="49551-103">CBaseFilter. CBaseFilter (const TCHAR \* 、LPUNKNOWN、CCritSec \* 、REFCLSID、HRESULT \*) 的函式</span><span class="sxs-lookup"><span data-stu-id="49551-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="49551-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="49551-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49551-105">語法</span><span class="sxs-lookup"><span data-stu-id="49551-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="49551-106">參數</span><span class="sxs-lookup"><span data-stu-id="49551-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49551-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="49551-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="49551-108">包含篩選名稱之字串的指標，用於進行調試。</span><span class="sxs-lookup"><span data-stu-id="49551-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="49551-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="49551-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="49551-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="49551-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="49551-111">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="49551-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="49551-112">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="49551-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="49551-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="49551-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="49551-114">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="49551-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="49551-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="49551-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="49551-116">篩選準則 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="49551-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="49551-117">*phr*</span><span class="sxs-lookup"><span data-stu-id="49551-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="49551-118">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="49551-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="49551-119">此函數會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="49551-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49551-120">備註</span><span class="sxs-lookup"><span data-stu-id="49551-120">Remarks</span></span>

<span data-ttu-id="49551-121">針對重要區段物件，您通常會執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="49551-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="49551-122">衍生繼承 **CBaseFilter** 和 **CCritSec** 的類別。</span><span class="sxs-lookup"><span data-stu-id="49551-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="49551-123">若為 *pLock*，請傳遞 `this` 指標。</span><span class="sxs-lookup"><span data-stu-id="49551-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="49551-124">衍生繼承 **CBaseFilter** 的類別，並包含 **CCritSec** 成員變數。</span><span class="sxs-lookup"><span data-stu-id="49551-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="49551-125">若為 *pLock*，請傳遞該變數的位址。</span><span class="sxs-lookup"><span data-stu-id="49551-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="49551-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="49551-126">Requirements</span></span>



| <span data-ttu-id="49551-127">需求</span><span class="sxs-lookup"><span data-stu-id="49551-127">Requirement</span></span> | <span data-ttu-id="49551-128">值</span><span class="sxs-lookup"><span data-stu-id="49551-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49551-129">標頭</span><span class="sxs-lookup"><span data-stu-id="49551-129">Header</span></span><br/>  | <dl> <span data-ttu-id="49551-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="49551-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="49551-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="49551-131">Library</span></span><br/> | <dl> <span data-ttu-id="49551-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="49551-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49551-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49551-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49551-134">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="49551-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




