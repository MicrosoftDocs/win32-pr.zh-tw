---
description: AddBeforeI 方法會在指定的位置之前插入專案。
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: 'CBaseList. AddBeforeI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983059"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="bd9e4-103">CBaseList. AddBeforeI 方法</span><span class="sxs-lookup"><span data-stu-id="bd9e4-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="bd9e4-104">方法會在 `AddBeforeI` 指定的位置之前插入專案。</span><span class="sxs-lookup"><span data-stu-id="bd9e4-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd9e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd9e4-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="bd9e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd9e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd9e4-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="bd9e4-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="bd9e4-108">要在其中加入專案的位置。</span><span class="sxs-lookup"><span data-stu-id="bd9e4-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="bd9e4-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="bd9e4-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="bd9e4-110">專案的指標。</span><span class="sxs-lookup"><span data-stu-id="bd9e4-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd9e4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd9e4-111">Return value</span></span>

<span data-ttu-id="bd9e4-112">傳回所插入專案的位置指標。</span><span class="sxs-lookup"><span data-stu-id="bd9e4-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd9e4-113">備註</span><span class="sxs-lookup"><span data-stu-id="bd9e4-113">Remarks</span></span>

<span data-ttu-id="bd9e4-114">如果 *pos* 是 **Null**，這個方法會將專案加入至清單的結尾 (相當於呼叫 [**CBaseList：： AddTailI**](cbaselist-addtaili.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="bd9e4-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd9e4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd9e4-115">Requirements</span></span>



| <span data-ttu-id="bd9e4-116">需求</span><span class="sxs-lookup"><span data-stu-id="bd9e4-116">Requirement</span></span> | <span data-ttu-id="bd9e4-117">值</span><span class="sxs-lookup"><span data-stu-id="bd9e4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd9e4-118">標頭</span><span class="sxs-lookup"><span data-stu-id="bd9e4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bd9e4-119"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bd9e4-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bd9e4-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd9e4-120">Library</span></span><br/> | <dl> <span data-ttu-id="bd9e4-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bd9e4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd9e4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd9e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd9e4-123">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="bd9e4-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




