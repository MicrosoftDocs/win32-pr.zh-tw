---
description: AddAfterI 方法會在指定的位置之後插入專案。
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: 'CBaseList. AddAfterI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994109"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="68f75-103">CBaseList. AddAfterI 方法</span><span class="sxs-lookup"><span data-stu-id="68f75-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="68f75-104">方法會在 `AddAfterI` 指定的位置之後插入專案。</span><span class="sxs-lookup"><span data-stu-id="68f75-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f75-105">語法</span><span class="sxs-lookup"><span data-stu-id="68f75-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="68f75-106">參數</span><span class="sxs-lookup"><span data-stu-id="68f75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f75-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="68f75-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="68f75-108">要在其後加入專案的位置。</span><span class="sxs-lookup"><span data-stu-id="68f75-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="68f75-109">*pObj*</span><span class="sxs-lookup"><span data-stu-id="68f75-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="68f75-110">要加入之專案的指標。</span><span class="sxs-lookup"><span data-stu-id="68f75-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f75-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="68f75-111">Return value</span></span>

<span data-ttu-id="68f75-112">傳回所插入專案的位置指標。</span><span class="sxs-lookup"><span data-stu-id="68f75-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="68f75-113">備註</span><span class="sxs-lookup"><span data-stu-id="68f75-113">Remarks</span></span>

<span data-ttu-id="68f75-114">如果 *pos* 是 **Null**，這個方法會將專案加入至清單的開頭 (相當於呼叫 [**CBaseList：： AddHeadI**](cbaselist-addheadi.md) 方法) 。</span><span class="sxs-lookup"><span data-stu-id="68f75-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="68f75-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="68f75-115">Requirements</span></span>



| <span data-ttu-id="68f75-116">需求</span><span class="sxs-lookup"><span data-stu-id="68f75-116">Requirement</span></span> | <span data-ttu-id="68f75-117">值</span><span class="sxs-lookup"><span data-stu-id="68f75-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f75-118">標頭</span><span class="sxs-lookup"><span data-stu-id="68f75-118">Header</span></span><br/>  | <dl> <span data-ttu-id="68f75-119"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68f75-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="68f75-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="68f75-120">Library</span></span><br/> | <dl> <span data-ttu-id="68f75-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="68f75-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f75-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68f75-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f75-123">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="68f75-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




