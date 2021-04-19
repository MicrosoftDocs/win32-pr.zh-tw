---
description: AddAfter 方法會在指定的位置之後插入清單。
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: 'CBaseList. AddAfter 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995765"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="5fb5e-103">CBaseList. AddAfter 方法</span><span class="sxs-lookup"><span data-stu-id="5fb5e-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="5fb5e-104">方法會在 `AddAfter` 指定的位置之後插入清單。</span><span class="sxs-lookup"><span data-stu-id="5fb5e-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb5e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5fb5e-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="5fb5e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5fb5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb5e-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="5fb5e-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="5fb5e-108">要在其後插入清單的位置。</span><span class="sxs-lookup"><span data-stu-id="5fb5e-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="5fb5e-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="5fb5e-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="5fb5e-110">要插入之清單的指標。</span><span class="sxs-lookup"><span data-stu-id="5fb5e-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb5e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fb5e-111">Return value</span></span>

<span data-ttu-id="5fb5e-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5fb5e-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb5e-113">備註</span><span class="sxs-lookup"><span data-stu-id="5fb5e-113">Remarks</span></span>

<span data-ttu-id="5fb5e-114">現有的位置指標，包括 *pos* 參數中指定的指標，會保持有效。</span><span class="sxs-lookup"><span data-stu-id="5fb5e-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="5fb5e-115">如果此方法失敗，可能會加入一些專案。</span><span class="sxs-lookup"><span data-stu-id="5fb5e-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb5e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fb5e-116">Requirements</span></span>



| <span data-ttu-id="5fb5e-117">需求</span><span class="sxs-lookup"><span data-stu-id="5fb5e-117">Requirement</span></span> | <span data-ttu-id="5fb5e-118">值</span><span class="sxs-lookup"><span data-stu-id="5fb5e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb5e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5fb5e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5fb5e-120"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5fb5e-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5fb5e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="5fb5e-121">Library</span></span><br/> | <dl> <span data-ttu-id="5fb5e-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5fb5e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb5e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fb5e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb5e-124">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="5fb5e-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




