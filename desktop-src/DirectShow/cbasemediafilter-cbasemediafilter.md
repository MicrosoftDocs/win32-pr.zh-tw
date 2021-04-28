---
description: CBaseMediaFilter。 CBaseMediaFilter 函式-函數方法。
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
ms.openlocfilehash: f123c7af29c6420de6004132180eba8dbf33fa72
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096316"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="9ab48-103">CBaseMediaFilter. CBaseMediaFilter 函數</span><span class="sxs-lookup"><span data-stu-id="9ab48-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="9ab48-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="9ab48-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab48-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ab48-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="9ab48-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ab48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab48-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="9ab48-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab48-108">包含物件名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="9ab48-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="9ab48-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="9ab48-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab48-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="9ab48-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="9ab48-111">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="9ab48-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9ab48-112">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9ab48-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9ab48-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="9ab48-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab48-114">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9ab48-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="9ab48-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="9ab48-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab48-116">物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ab48-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ab48-117">備註</span><span class="sxs-lookup"><span data-stu-id="9ab48-117">Remarks</span></span>

<span data-ttu-id="9ab48-118">如果另一個物件包含或匯總 `CBaseMediaFilter` 物件， **CCritSec** 鎖定可能會在 `CBaseMediaFilter` 物件外部。</span><span class="sxs-lookup"><span data-stu-id="9ab48-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="9ab48-119">在此情況下，請將指標傳遞至 *pLock* 中的鎖定。</span><span class="sxs-lookup"><span data-stu-id="9ab48-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="9ab48-120">否則，您可以：</span><span class="sxs-lookup"><span data-stu-id="9ab48-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="9ab48-121">衍生繼承和 CCritSec 的類別 `CBaseMediaFilter` 。 </span><span class="sxs-lookup"><span data-stu-id="9ab48-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="9ab48-122">若為 *pLock*，請傳遞 this 指標。</span><span class="sxs-lookup"><span data-stu-id="9ab48-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="9ab48-123">衍生繼承 `CBaseMediaFilter` 並包含 **CCritSec** 成員變數的類別。</span><span class="sxs-lookup"><span data-stu-id="9ab48-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="9ab48-124">若為 *pLock*，請傳遞該變數的位址。</span><span class="sxs-lookup"><span data-stu-id="9ab48-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab48-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ab48-125">Requirements</span></span>



| <span data-ttu-id="9ab48-126">需求</span><span class="sxs-lookup"><span data-stu-id="9ab48-126">Requirement</span></span> | <span data-ttu-id="9ab48-127">值</span><span class="sxs-lookup"><span data-stu-id="9ab48-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab48-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9ab48-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9ab48-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9ab48-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ab48-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9ab48-130">Library</span></span><br/> | <dl> <span data-ttu-id="9ab48-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9ab48-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab48-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ab48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab48-133">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="9ab48-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




