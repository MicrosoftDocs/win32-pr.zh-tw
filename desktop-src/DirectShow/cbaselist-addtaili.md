---
description: AddTailI 方法會將專案加入至清單結尾。
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: 'CBaseList. AddTailI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001919"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="3ce22-103">CBaseList. AddTailI 方法</span><span class="sxs-lookup"><span data-stu-id="3ce22-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="3ce22-104">`AddTailI`方法會將專案加入至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="3ce22-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce22-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ce22-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="3ce22-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ce22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce22-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="3ce22-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="3ce22-108">專案的指標。</span><span class="sxs-lookup"><span data-stu-id="3ce22-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce22-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ce22-109">Return value</span></span>

<span data-ttu-id="3ce22-110">傳回新結尾位置的位置值。</span><span class="sxs-lookup"><span data-stu-id="3ce22-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce22-111">備註</span><span class="sxs-lookup"><span data-stu-id="3ce22-111">Remarks</span></span>

<span data-ttu-id="3ce22-112">如果方法失敗，則會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3ce22-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce22-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ce22-113">Requirements</span></span>



| <span data-ttu-id="3ce22-114">需求</span><span class="sxs-lookup"><span data-stu-id="3ce22-114">Requirement</span></span> | <span data-ttu-id="3ce22-115">值</span><span class="sxs-lookup"><span data-stu-id="3ce22-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce22-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3ce22-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3ce22-117"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3ce22-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3ce22-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ce22-118">Library</span></span><br/> | <dl> <span data-ttu-id="3ce22-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3ce22-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce22-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ce22-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce22-121">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="3ce22-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




