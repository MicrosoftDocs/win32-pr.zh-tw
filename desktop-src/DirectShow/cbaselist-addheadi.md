---
description: AddHeadI 方法會將專案加入至清單的前方。
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: 'CBaseList. AddHeadI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994107"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="35298-103">CBaseList. AddHeadI 方法</span><span class="sxs-lookup"><span data-stu-id="35298-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="35298-104">`AddHeadI`方法會將專案加入至清單的前方。</span><span class="sxs-lookup"><span data-stu-id="35298-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="35298-105">語法</span><span class="sxs-lookup"><span data-stu-id="35298-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="35298-106">參數</span><span class="sxs-lookup"><span data-stu-id="35298-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35298-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="35298-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="35298-108">專案的指標。</span><span class="sxs-lookup"><span data-stu-id="35298-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35298-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="35298-109">Return value</span></span>

<span data-ttu-id="35298-110">傳回位置值，表示新的標頭位置。</span><span class="sxs-lookup"><span data-stu-id="35298-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="35298-111">備註</span><span class="sxs-lookup"><span data-stu-id="35298-111">Remarks</span></span>

<span data-ttu-id="35298-112">如果方法失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="35298-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="35298-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="35298-113">Requirements</span></span>



| <span data-ttu-id="35298-114">需求</span><span class="sxs-lookup"><span data-stu-id="35298-114">Requirement</span></span> | <span data-ttu-id="35298-115">值</span><span class="sxs-lookup"><span data-stu-id="35298-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35298-116">標頭</span><span class="sxs-lookup"><span data-stu-id="35298-116">Header</span></span><br/>  | <dl> <span data-ttu-id="35298-117"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="35298-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="35298-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="35298-118">Library</span></span><br/> | <dl> <span data-ttu-id="35298-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="35298-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35298-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35298-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35298-121">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="35298-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




