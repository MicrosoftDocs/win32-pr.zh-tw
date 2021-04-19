---
description: AddTail 方法會將另一個清單附加至這份清單的結尾。
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: 'CBaseList. AddTail 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984085"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="360aa-103">CBaseList. AddTail 方法</span><span class="sxs-lookup"><span data-stu-id="360aa-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="360aa-104">方法會將 `AddTail` 另一個清單附加至這份清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="360aa-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="360aa-105">語法</span><span class="sxs-lookup"><span data-stu-id="360aa-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="360aa-106">參數</span><span class="sxs-lookup"><span data-stu-id="360aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360aa-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="360aa-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="360aa-108">要附加之清單的指標。</span><span class="sxs-lookup"><span data-stu-id="360aa-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360aa-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="360aa-109">Return value</span></span>

<span data-ttu-id="360aa-110">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="360aa-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="360aa-111">備註</span><span class="sxs-lookup"><span data-stu-id="360aa-111">Remarks</span></span>

<span data-ttu-id="360aa-112">如果方法失敗，某些專案可能已加入至清單。</span><span class="sxs-lookup"><span data-stu-id="360aa-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="360aa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="360aa-113">Requirements</span></span>



| <span data-ttu-id="360aa-114">需求</span><span class="sxs-lookup"><span data-stu-id="360aa-114">Requirement</span></span> | <span data-ttu-id="360aa-115">值</span><span class="sxs-lookup"><span data-stu-id="360aa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360aa-116">標頭</span><span class="sxs-lookup"><span data-stu-id="360aa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="360aa-117"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="360aa-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="360aa-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="360aa-118">Library</span></span><br/> | <dl> <span data-ttu-id="360aa-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="360aa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="360aa-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="360aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360aa-121">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="360aa-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




