---
description: CSourceSeeking。 CSourceSeeking 函式-函數方法。
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: 'CSourceSeeking. CSourceSeeking (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098816"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="58725-103">CSourceSeeking. CSourceSeeking 函數</span><span class="sxs-lookup"><span data-stu-id="58725-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="58725-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="58725-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58725-105">語法</span><span class="sxs-lookup"><span data-stu-id="58725-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="58725-106">參數</span><span class="sxs-lookup"><span data-stu-id="58725-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58725-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="58725-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="58725-108">包含物件名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="58725-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="58725-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="58725-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="58725-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="58725-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="58725-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="58725-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="58725-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="58725-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="58725-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="58725-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="58725-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="58725-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="58725-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="58725-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="58725-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="58725-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="58725-117">*pLock*</span><span class="sxs-lookup"><span data-stu-id="58725-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="58725-118">[**CCritSec**](ccritsec.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="58725-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="58725-119">在您的衍生類別中，宣告 **CCritSec** 成員變數，並針對此參數使用它的位址。</span><span class="sxs-lookup"><span data-stu-id="58725-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="58725-120">`CSourceSeeking`類別會使用此重要區段來同步處理開始和停止時間、持續時間和播放速率的存取。</span><span class="sxs-lookup"><span data-stu-id="58725-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="58725-121">當您在衍生類別中存取這些變數時，請保留此鎖定。</span><span class="sxs-lookup"><span data-stu-id="58725-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58725-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="58725-122">Requirements</span></span>



| <span data-ttu-id="58725-123">需求</span><span class="sxs-lookup"><span data-stu-id="58725-123">Requirement</span></span> | <span data-ttu-id="58725-124">值</span><span class="sxs-lookup"><span data-stu-id="58725-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58725-125">標頭</span><span class="sxs-lookup"><span data-stu-id="58725-125">Header</span></span><br/>  | <dl> <span data-ttu-id="58725-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="58725-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="58725-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="58725-127">Library</span></span><br/> | <dl> <span data-ttu-id="58725-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="58725-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58725-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58725-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58725-130">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="58725-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




