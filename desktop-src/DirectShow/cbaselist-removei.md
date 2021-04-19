---
description: RemoveI 方法會在指定的位置移除專案。
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: 'CBaseList. RemoveI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994796"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="6cbe9-103">CBaseList. RemoveI 方法</span><span class="sxs-lookup"><span data-stu-id="6cbe9-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="6cbe9-104">`RemoveI`方法會移除指定位置上的專案。</span><span class="sxs-lookup"><span data-stu-id="6cbe9-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cbe9-105">語法</span><span class="sxs-lookup"><span data-stu-id="6cbe9-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="6cbe9-106">參數</span><span class="sxs-lookup"><span data-stu-id="6cbe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cbe9-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="6cbe9-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="6cbe9-108">指出要移除之專案的位置值。</span><span class="sxs-lookup"><span data-stu-id="6cbe9-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cbe9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cbe9-109">Return value</span></span>

<span data-ttu-id="6cbe9-110">傳回專案的指標。</span><span class="sxs-lookup"><span data-stu-id="6cbe9-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cbe9-111">備註</span><span class="sxs-lookup"><span data-stu-id="6cbe9-111">Remarks</span></span>

<span data-ttu-id="6cbe9-112">這個方法會從清單中刪除節點，但不會刪除該節點中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="6cbe9-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="6cbe9-113">如果 *pos* 是 **null**，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="6cbe9-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cbe9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cbe9-114">Requirements</span></span>



| <span data-ttu-id="6cbe9-115">需求</span><span class="sxs-lookup"><span data-stu-id="6cbe9-115">Requirement</span></span> | <span data-ttu-id="6cbe9-116">值</span><span class="sxs-lookup"><span data-stu-id="6cbe9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cbe9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6cbe9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6cbe9-118"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6cbe9-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6cbe9-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6cbe9-119">Library</span></span><br/> | <dl> <span data-ttu-id="6cbe9-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6cbe9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cbe9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cbe9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cbe9-122">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="6cbe9-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




