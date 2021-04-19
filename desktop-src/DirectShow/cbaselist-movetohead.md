---
description: MoveToHead 方法會分割清單，並將結尾部分插入另一個清單的開頭。
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: 'CBaseList. MoveToHead 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993505"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="de0b2-103">CBaseList. MoveToHead 方法</span><span class="sxs-lookup"><span data-stu-id="de0b2-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="de0b2-104">`MoveToHead`方法會分割清單，並將結尾部分插入另一個清單的開頭。</span><span class="sxs-lookup"><span data-stu-id="de0b2-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="de0b2-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="de0b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="de0b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0b2-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="de0b2-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="de0b2-108">在清單中標示分割的位置指標。</span><span class="sxs-lookup"><span data-stu-id="de0b2-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="de0b2-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="de0b2-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="de0b2-110">指向另一個清單的指標。</span><span class="sxs-lookup"><span data-stu-id="de0b2-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0b2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="de0b2-111">Return value</span></span>

<span data-ttu-id="de0b2-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="de0b2-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="de0b2-113">備註</span><span class="sxs-lookup"><span data-stu-id="de0b2-113">Remarks</span></span>

<span data-ttu-id="de0b2-114">這個方法會將清單分割于 *pos* 參數所指定的位置之前。</span><span class="sxs-lookup"><span data-stu-id="de0b2-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="de0b2-115">標題部分會保留在清單中。</span><span class="sxs-lookup"><span data-stu-id="de0b2-115">The head portion remains in the list.</span></span> <span data-ttu-id="de0b2-116">結尾部分會插入另一個清單的開頭。</span><span class="sxs-lookup"><span data-stu-id="de0b2-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="de0b2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="de0b2-117">Requirements</span></span>



| <span data-ttu-id="de0b2-118">需求</span><span class="sxs-lookup"><span data-stu-id="de0b2-118">Requirement</span></span> | <span data-ttu-id="de0b2-119">值</span><span class="sxs-lookup"><span data-stu-id="de0b2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de0b2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="de0b2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="de0b2-121"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="de0b2-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="de0b2-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="de0b2-122">Library</span></span><br/> | <dl> <span data-ttu-id="de0b2-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="de0b2-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0b2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de0b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0b2-125">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="de0b2-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




