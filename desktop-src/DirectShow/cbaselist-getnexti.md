---
description: GetNextI 方法會在指定的位置抓取專案，並將位置往前移。
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: 'CBaseList. GetNextI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992937"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="6c317-103">CBaseList. GetNextI 方法</span><span class="sxs-lookup"><span data-stu-id="6c317-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="6c317-104">`GetNextI`方法會在指定的位置抓取專案，並將位置往前移。</span><span class="sxs-lookup"><span data-stu-id="6c317-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c317-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c317-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="6c317-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c317-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c317-107">*rp* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="6c317-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6c317-108">位置值的參考。</span><span class="sxs-lookup"><span data-stu-id="6c317-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c317-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c317-109">Return value</span></span>

<span data-ttu-id="6c317-110">傳回專案的指標。</span><span class="sxs-lookup"><span data-stu-id="6c317-110">Returns a pointer to the item.</span></span> <span data-ttu-id="6c317-111">如果 *rp* 為 **null**，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="6c317-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c317-112">備註</span><span class="sxs-lookup"><span data-stu-id="6c317-112">Remarks</span></span>

<span data-ttu-id="6c317-113">這個方法會將位置指標往前移到下一個位置。</span><span class="sxs-lookup"><span data-stu-id="6c317-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="6c317-114">如果位置指標移動超過清單的結尾，則方法會將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6c317-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c317-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c317-115">Requirements</span></span>



| <span data-ttu-id="6c317-116">需求</span><span class="sxs-lookup"><span data-stu-id="6c317-116">Requirement</span></span> | <span data-ttu-id="6c317-117">值</span><span class="sxs-lookup"><span data-stu-id="6c317-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c317-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6c317-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6c317-119"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6c317-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6c317-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c317-120">Library</span></span><br/> | <dl> <span data-ttu-id="6c317-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6c317-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c317-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c317-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c317-123">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="6c317-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




