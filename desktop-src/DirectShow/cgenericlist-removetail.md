---
description: RemoveTail 方法會移除清單中的最後一個專案。
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: 'CGenericList. RemoveTail 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987201"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="8e96f-103">CGenericList. RemoveTail 方法</span><span class="sxs-lookup"><span data-stu-id="8e96f-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="8e96f-104">`RemoveTail`方法會移除清單中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="8e96f-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e96f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e96f-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="8e96f-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e96f-106">Parameters</span></span>

<span data-ttu-id="8e96f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8e96f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e96f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e96f-108">Return value</span></span>

<span data-ttu-id="8e96f-109">傳回型別 **物件** 的物件指標 (範本型別) ，如果清單是空的，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8e96f-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e96f-110">備註</span><span class="sxs-lookup"><span data-stu-id="8e96f-110">Remarks</span></span>

<span data-ttu-id="8e96f-111">這個方法會刪除清單節點，但不會刪除節點中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="8e96f-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e96f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e96f-112">Requirements</span></span>



| <span data-ttu-id="8e96f-113">需求</span><span class="sxs-lookup"><span data-stu-id="8e96f-113">Requirement</span></span> | <span data-ttu-id="8e96f-114">值</span><span class="sxs-lookup"><span data-stu-id="8e96f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e96f-115">標頭</span><span class="sxs-lookup"><span data-stu-id="8e96f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8e96f-116"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8e96f-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8e96f-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e96f-117">Library</span></span><br/> | <dl> <span data-ttu-id="8e96f-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8e96f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e96f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e96f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e96f-120">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="8e96f-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




