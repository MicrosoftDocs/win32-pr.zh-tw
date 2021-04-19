---
description: 前一個方法會抓取清單中先前的位置。
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: 'CBaseList 前一個方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976096"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="0aa8f-103">CBaseList. 上一方法</span><span class="sxs-lookup"><span data-stu-id="0aa8f-103">CBaseList.Prev method</span></span>

<span data-ttu-id="0aa8f-104">方法會抓取 `Prev` 清單中先前的位置。</span><span class="sxs-lookup"><span data-stu-id="0aa8f-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="0aa8f-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="0aa8f-106">參數</span><span class="sxs-lookup"><span data-stu-id="0aa8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa8f-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="0aa8f-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="0aa8f-108">位置值。</span><span class="sxs-lookup"><span data-stu-id="0aa8f-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa8f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0aa8f-109">Return value</span></span>

<span data-ttu-id="0aa8f-110">傳回在 *pos* 中指定位置之前的位置指標。</span><span class="sxs-lookup"><span data-stu-id="0aa8f-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa8f-111">備註</span><span class="sxs-lookup"><span data-stu-id="0aa8f-111">Remarks</span></span>

<span data-ttu-id="0aa8f-112">如果 *pos* 是清單中的第一個位置，則方法會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0aa8f-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="0aa8f-113">如果 *pos* 是 **Null**，則方法會傳回清單中的最後一個位置。</span><span class="sxs-lookup"><span data-stu-id="0aa8f-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa8f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aa8f-114">Requirements</span></span>



| <span data-ttu-id="0aa8f-115">需求</span><span class="sxs-lookup"><span data-stu-id="0aa8f-115">Requirement</span></span> | <span data-ttu-id="0aa8f-116">值</span><span class="sxs-lookup"><span data-stu-id="0aa8f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa8f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0aa8f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0aa8f-118"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0aa8f-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0aa8f-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0aa8f-119">Library</span></span><br/> | <dl> <span data-ttu-id="0aa8f-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0aa8f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa8f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aa8f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa8f-122">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="0aa8f-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




