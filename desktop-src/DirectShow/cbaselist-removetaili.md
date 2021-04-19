---
description: RemoveTailI 方法會移除清單中的最後一個專案。
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: 'CBaseList. RemoveTailI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001114"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="02726-103">CBaseList. RemoveTailI 方法</span><span class="sxs-lookup"><span data-stu-id="02726-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="02726-104">`RemoveTailI`方法會移除清單中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="02726-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="02726-105">語法</span><span class="sxs-lookup"><span data-stu-id="02726-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="02726-106">參數</span><span class="sxs-lookup"><span data-stu-id="02726-106">Parameters</span></span>

<span data-ttu-id="02726-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="02726-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02726-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="02726-108">Return value</span></span>

<span data-ttu-id="02726-109">傳回專案的指標，如果清單是空的，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="02726-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="02726-110">備註</span><span class="sxs-lookup"><span data-stu-id="02726-110">Remarks</span></span>

<span data-ttu-id="02726-111">這個方法會刪除清單節點，但不會刪除節點中包含的專案。</span><span class="sxs-lookup"><span data-stu-id="02726-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="02726-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="02726-112">Requirements</span></span>



| <span data-ttu-id="02726-113">需求</span><span class="sxs-lookup"><span data-stu-id="02726-113">Requirement</span></span> | <span data-ttu-id="02726-114">值</span><span class="sxs-lookup"><span data-stu-id="02726-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02726-115">標頭</span><span class="sxs-lookup"><span data-stu-id="02726-115">Header</span></span><br/>  | <dl> <span data-ttu-id="02726-116"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="02726-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="02726-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="02726-117">Library</span></span><br/> | <dl> <span data-ttu-id="02726-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="02726-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02726-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02726-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02726-120">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="02726-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




