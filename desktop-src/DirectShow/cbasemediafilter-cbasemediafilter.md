---
description: 函式方法。
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: 'CBaseMediaFilter. CBaseMediaFilter (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994204"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="4207b-103">CBaseMediaFilter. CBaseMediaFilter 函數</span><span class="sxs-lookup"><span data-stu-id="4207b-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="4207b-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4207b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4207b-105">語法</span><span class="sxs-lookup"><span data-stu-id="4207b-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="4207b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4207b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4207b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="4207b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4207b-108">包含物件名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4207b-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="4207b-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="4207b-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4207b-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="4207b-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="4207b-111">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="4207b-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="4207b-112">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4207b-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4207b-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="4207b-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="4207b-114">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="4207b-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="4207b-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="4207b-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="4207b-116">物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="4207b-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4207b-117">備註</span><span class="sxs-lookup"><span data-stu-id="4207b-117">Remarks</span></span>

<span data-ttu-id="4207b-118">如果另一個物件包含或匯總 `CBaseMediaFilter` 物件， **CCritSec** 鎖定可能會在 `CBaseMediaFilter` 物件外部。</span><span class="sxs-lookup"><span data-stu-id="4207b-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="4207b-119">在此情況下，請將指標傳遞至 *pLock* 中的鎖定。</span><span class="sxs-lookup"><span data-stu-id="4207b-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="4207b-120">否則，您可以：</span><span class="sxs-lookup"><span data-stu-id="4207b-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="4207b-121">衍生繼承和 CCritSec 的類別 `CBaseMediaFilter` 。 </span><span class="sxs-lookup"><span data-stu-id="4207b-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="4207b-122">若為 *pLock*，請傳遞 this 指標。</span><span class="sxs-lookup"><span data-stu-id="4207b-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="4207b-123">衍生繼承 `CBaseMediaFilter` 並包含 **CCritSec** 成員變數的類別。</span><span class="sxs-lookup"><span data-stu-id="4207b-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="4207b-124">若為 *pLock*，請傳遞該變數的位址。</span><span class="sxs-lookup"><span data-stu-id="4207b-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4207b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4207b-125">Requirements</span></span>



| <span data-ttu-id="4207b-126">需求</span><span class="sxs-lookup"><span data-stu-id="4207b-126">Requirement</span></span> | <span data-ttu-id="4207b-127">值</span><span class="sxs-lookup"><span data-stu-id="4207b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4207b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4207b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4207b-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4207b-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4207b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="4207b-130">Library</span></span><br/> | <dl> <span data-ttu-id="4207b-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4207b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4207b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4207b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4207b-133">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4207b-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




