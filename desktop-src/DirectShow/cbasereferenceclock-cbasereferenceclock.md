---
description: CBaseReferenceClock。 CBaseReferenceClock 函式-函數方法。
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: 'CBaseReferenceClock. CBaseReferenceClock (Refclock. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119936"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="7bc20-103">CBaseReferenceClock. CBaseReferenceClock 函數</span><span class="sxs-lookup"><span data-stu-id="7bc20-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="7bc20-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="7bc20-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc20-105">語法</span><span class="sxs-lookup"><span data-stu-id="7bc20-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="7bc20-106">參數</span><span class="sxs-lookup"><span data-stu-id="7bc20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc20-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="7bc20-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc20-108">包含物件名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="7bc20-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="7bc20-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="7bc20-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="7bc20-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="7bc20-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc20-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="7bc20-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="7bc20-112">如果物件已匯總，請將指標傳遞至匯總物件的 IUnknown 介面。</span><span class="sxs-lookup"><span data-stu-id="7bc20-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="7bc20-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7bc20-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7bc20-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="7bc20-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc20-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="7bc20-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="7bc20-116">如果發生錯誤，方法會在此參數中傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7bc20-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="7bc20-117">請勿將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7bc20-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7bc20-118">*Psched.sys*</span><span class="sxs-lookup"><span data-stu-id="7bc20-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc20-119">[**CAMSchedule**](camschedule.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7bc20-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="7bc20-120">如果是 **Null**，這個方法會建立新的 **CAMSchedule** 物件。</span><span class="sxs-lookup"><span data-stu-id="7bc20-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bc20-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bc20-121">Requirements</span></span>



| <span data-ttu-id="7bc20-122">需求</span><span class="sxs-lookup"><span data-stu-id="7bc20-122">Requirement</span></span> | <span data-ttu-id="7bc20-123">值</span><span class="sxs-lookup"><span data-stu-id="7bc20-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc20-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7bc20-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7bc20-125"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7bc20-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7bc20-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="7bc20-126">Library</span></span><br/> | <dl> <span data-ttu-id="7bc20-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7bc20-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bc20-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bc20-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc20-129">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="7bc20-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




