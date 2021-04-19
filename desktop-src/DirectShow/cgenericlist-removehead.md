---
description: RemoveHead 方法會移除清單中的第一個專案。
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: 'CGenericList. RemoveHead 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984326"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="81e84-103">CGenericList. RemoveHead 方法</span><span class="sxs-lookup"><span data-stu-id="81e84-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="81e84-104">`RemoveHead`方法會移除清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="81e84-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e84-105">語法</span><span class="sxs-lookup"><span data-stu-id="81e84-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="81e84-106">參數</span><span class="sxs-lookup"><span data-stu-id="81e84-106">Parameters</span></span>

<span data-ttu-id="81e84-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="81e84-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81e84-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="81e84-108">Return value</span></span>

<span data-ttu-id="81e84-109">傳回型別 **物件** 的物件指標 (範本型別) ，如果清單是空的，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="81e84-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e84-110">備註</span><span class="sxs-lookup"><span data-stu-id="81e84-110">Remarks</span></span>

<span data-ttu-id="81e84-111">這個方法會刪除清單節點，但不會刪除節點所包含的專案。</span><span class="sxs-lookup"><span data-stu-id="81e84-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e84-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="81e84-112">Requirements</span></span>



| <span data-ttu-id="81e84-113">需求</span><span class="sxs-lookup"><span data-stu-id="81e84-113">Requirement</span></span> | <span data-ttu-id="81e84-114">值</span><span class="sxs-lookup"><span data-stu-id="81e84-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e84-115">標頭</span><span class="sxs-lookup"><span data-stu-id="81e84-115">Header</span></span><br/>  | <dl> <span data-ttu-id="81e84-116"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81e84-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="81e84-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="81e84-117">Library</span></span><br/> | <dl> <span data-ttu-id="81e84-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81e84-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e84-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81e84-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e84-120">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="81e84-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




