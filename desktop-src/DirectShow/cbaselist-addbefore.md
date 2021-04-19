---
description: AddBefore 方法會在指定的位置之前插入清單。
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: 'CBaseList. AddBefore 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981295"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="c6e29-103">CBaseList. AddBefore 方法</span><span class="sxs-lookup"><span data-stu-id="c6e29-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="c6e29-104">方法會在 `AddBefore` 指定的位置之前插入清單。</span><span class="sxs-lookup"><span data-stu-id="c6e29-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e29-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6e29-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="c6e29-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6e29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e29-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="c6e29-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="c6e29-108">要插入清單的位置。</span><span class="sxs-lookup"><span data-stu-id="c6e29-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="c6e29-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="c6e29-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="c6e29-110">要插入之清單的指標。</span><span class="sxs-lookup"><span data-stu-id="c6e29-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e29-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6e29-111">Return value</span></span>

<span data-ttu-id="c6e29-112">如果成功， **則傳回 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c6e29-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="c6e29-113">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c6e29-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e29-114">備註</span><span class="sxs-lookup"><span data-stu-id="c6e29-114">Remarks</span></span>

<span data-ttu-id="c6e29-115">現有的位置指標，包括 *pos* 參數中指定的指標，會保持有效。</span><span class="sxs-lookup"><span data-stu-id="c6e29-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="c6e29-116">如果此方法失敗，可能會加入一些專案。</span><span class="sxs-lookup"><span data-stu-id="c6e29-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e29-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6e29-117">Requirements</span></span>



| <span data-ttu-id="c6e29-118">需求</span><span class="sxs-lookup"><span data-stu-id="c6e29-118">Requirement</span></span> | <span data-ttu-id="c6e29-119">值</span><span class="sxs-lookup"><span data-stu-id="c6e29-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e29-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c6e29-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c6e29-121"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c6e29-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c6e29-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c6e29-122">Library</span></span><br/> | <dl> <span data-ttu-id="c6e29-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c6e29-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e29-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6e29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e29-125">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="c6e29-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




