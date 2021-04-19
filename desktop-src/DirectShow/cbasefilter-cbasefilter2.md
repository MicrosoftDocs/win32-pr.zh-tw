---
description: 函式方法。
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: 'CBaseFilter. CBaseFilter (const TCHAR *、LPUNKNOWN、CCritSec*、REFCLSID)  (Amfilter. h) '
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
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000680"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="205c9-103">CBaseFilter. CBaseFilter (const TCHAR \* 、LPUNKNOWN、CCritSec \* 、REFCLSID) 函數</span><span class="sxs-lookup"><span data-stu-id="205c9-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="205c9-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="205c9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="205c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="205c9-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="205c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="205c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205c9-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="205c9-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="205c9-108">包含篩選名稱之字串的指標，用於進行調試。</span><span class="sxs-lookup"><span data-stu-id="205c9-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="205c9-109">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="205c9-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="205c9-110">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="205c9-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="205c9-111">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="205c9-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="205c9-112">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="205c9-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="205c9-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="205c9-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="205c9-114">[**CCritSec**](ccritsec.md)鎖定的指標，用來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="205c9-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="205c9-115">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="205c9-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="205c9-116">篩選準則 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="205c9-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="205c9-117">備註</span><span class="sxs-lookup"><span data-stu-id="205c9-117">Remarks</span></span>

<span data-ttu-id="205c9-118">針對重要區段物件，您通常會執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="205c9-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="205c9-119">衍生繼承 **CBaseFilter** 和 **CCritSec** 的類別。</span><span class="sxs-lookup"><span data-stu-id="205c9-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="205c9-120">若為 *pLock*，請傳遞 `this` 指標。</span><span class="sxs-lookup"><span data-stu-id="205c9-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="205c9-121">衍生繼承 **CBaseFilter** 的類別，並包含 **CCritSec** 成員變數。</span><span class="sxs-lookup"><span data-stu-id="205c9-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="205c9-122">若為 *pLock*，請傳遞該變數的位址。</span><span class="sxs-lookup"><span data-stu-id="205c9-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="205c9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="205c9-123">Requirements</span></span>



| <span data-ttu-id="205c9-124">需求</span><span class="sxs-lookup"><span data-stu-id="205c9-124">Requirement</span></span> | <span data-ttu-id="205c9-125">值</span><span class="sxs-lookup"><span data-stu-id="205c9-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205c9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="205c9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="205c9-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="205c9-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="205c9-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="205c9-128">Library</span></span><br/> | <dl> <span data-ttu-id="205c9-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="205c9-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205c9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="205c9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205c9-131">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="205c9-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




