---
description: GetI 方法會在指定的位置抓取專案。
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: 'CBaseList. GetI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989834"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="b3056-103">CBaseList. GetI 方法</span><span class="sxs-lookup"><span data-stu-id="b3056-103">CBaseList.GetI method</span></span>

<span data-ttu-id="b3056-104">`GetI`方法會在指定的位置抓取專案。</span><span class="sxs-lookup"><span data-stu-id="b3056-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3056-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3056-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="b3056-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3056-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="b3056-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="b3056-108">要取得之專案的位置指標。</span><span class="sxs-lookup"><span data-stu-id="b3056-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3056-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3056-109">Return value</span></span>

<span data-ttu-id="b3056-110">傳回專案的指標。</span><span class="sxs-lookup"><span data-stu-id="b3056-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3056-111">備註</span><span class="sxs-lookup"><span data-stu-id="b3056-111">Remarks</span></span>

<span data-ttu-id="b3056-112">如果 *pos* 是 **null**，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="b3056-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3056-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3056-113">Requirements</span></span>



| <span data-ttu-id="b3056-114">需求</span><span class="sxs-lookup"><span data-stu-id="b3056-114">Requirement</span></span> | <span data-ttu-id="b3056-115">值</span><span class="sxs-lookup"><span data-stu-id="b3056-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3056-116">標頭</span><span class="sxs-lookup"><span data-stu-id="b3056-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b3056-117"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b3056-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b3056-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3056-118">Library</span></span><br/> | <dl> <span data-ttu-id="b3056-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b3056-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3056-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3056-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3056-121">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="b3056-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




