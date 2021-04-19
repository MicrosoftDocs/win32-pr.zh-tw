---
description: RemoveHeadI 方法會移除清單中的第一個專案。
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: 'CBaseList. RemoveHeadI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996203"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="9b545-103">CBaseList. RemoveHeadI 方法</span><span class="sxs-lookup"><span data-stu-id="9b545-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="9b545-104">`RemoveHeadI`方法會移除清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="9b545-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b545-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b545-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="9b545-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b545-106">Parameters</span></span>

<span data-ttu-id="9b545-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9b545-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b545-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b545-108">Return value</span></span>

<span data-ttu-id="9b545-109">傳回專案的指標，如果清單是空的，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9b545-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b545-110">備註</span><span class="sxs-lookup"><span data-stu-id="9b545-110">Remarks</span></span>

<span data-ttu-id="9b545-111">這個方法會刪除清單節點，但不會刪除節點所包含的專案。</span><span class="sxs-lookup"><span data-stu-id="9b545-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b545-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b545-112">Requirements</span></span>



| <span data-ttu-id="9b545-113">需求</span><span class="sxs-lookup"><span data-stu-id="9b545-113">Requirement</span></span> | <span data-ttu-id="9b545-114">值</span><span class="sxs-lookup"><span data-stu-id="9b545-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b545-115">標頭</span><span class="sxs-lookup"><span data-stu-id="9b545-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9b545-116"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9b545-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9b545-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b545-117">Library</span></span><br/> | <dl> <span data-ttu-id="9b545-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9b545-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b545-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b545-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b545-120">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="9b545-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




