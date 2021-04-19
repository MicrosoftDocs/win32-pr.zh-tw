---
description: Remove 方法會移除指定位置上的專案。
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: 'CGenericList： Remove 方法 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994149"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="220a4-103">CGenericList 方法</span><span class="sxs-lookup"><span data-stu-id="220a4-103">CGenericList.Remove method</span></span>

<span data-ttu-id="220a4-104">`Remove`方法會移除指定位置上的專案。</span><span class="sxs-lookup"><span data-stu-id="220a4-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="220a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="220a4-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="220a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="220a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220a4-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="220a4-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="220a4-108">指出要移除之專案的位置值。</span><span class="sxs-lookup"><span data-stu-id="220a4-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220a4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="220a4-109">Return value</span></span>

<span data-ttu-id="220a4-110">傳回)  (範本型別 **物件** 之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="220a4-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="220a4-111">備註</span><span class="sxs-lookup"><span data-stu-id="220a4-111">Remarks</span></span>

<span data-ttu-id="220a4-112">這個方法會從清單中刪除節點，但不會刪除該節點中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="220a4-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="220a4-113">如果 *pos* 是 **null**，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="220a4-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="220a4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="220a4-114">Requirements</span></span>



| <span data-ttu-id="220a4-115">需求</span><span class="sxs-lookup"><span data-stu-id="220a4-115">Requirement</span></span> | <span data-ttu-id="220a4-116">值</span><span class="sxs-lookup"><span data-stu-id="220a4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="220a4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="220a4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="220a4-118"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="220a4-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="220a4-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="220a4-119">Library</span></span><br/> | <dl> <span data-ttu-id="220a4-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="220a4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220a4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="220a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220a4-122">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="220a4-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




