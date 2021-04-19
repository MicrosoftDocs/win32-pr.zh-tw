---
description: MoveToTail 方法會分割清單，並將標頭部分附加至另一個清單的結尾。
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: 'CBaseList. MoveToTail 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990238"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="2dafb-103">CBaseList. MoveToTail 方法</span><span class="sxs-lookup"><span data-stu-id="2dafb-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="2dafb-104">`MoveToTail`方法會分割清單，並將標頭部分附加至另一個清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="2dafb-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dafb-105">語法</span><span class="sxs-lookup"><span data-stu-id="2dafb-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="2dafb-106">參數</span><span class="sxs-lookup"><span data-stu-id="2dafb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dafb-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="2dafb-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="2dafb-108">在清單中標示分割的位置指標。</span><span class="sxs-lookup"><span data-stu-id="2dafb-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="2dafb-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="2dafb-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="2dafb-110">指向另一個清單的指標。</span><span class="sxs-lookup"><span data-stu-id="2dafb-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dafb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dafb-111">Return value</span></span>

<span data-ttu-id="2dafb-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2dafb-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dafb-113">備註</span><span class="sxs-lookup"><span data-stu-id="2dafb-113">Remarks</span></span>

<span data-ttu-id="2dafb-114">這個方法會將清單分割于 *pos* 參數所指定的位置之後。</span><span class="sxs-lookup"><span data-stu-id="2dafb-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="2dafb-115">結尾部分會保留在清單中。</span><span class="sxs-lookup"><span data-stu-id="2dafb-115">The tail portion remains in the list.</span></span> <span data-ttu-id="2dafb-116">前端部分會附加至另一個清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="2dafb-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dafb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dafb-117">Requirements</span></span>



| <span data-ttu-id="2dafb-118">需求</span><span class="sxs-lookup"><span data-stu-id="2dafb-118">Requirement</span></span> | <span data-ttu-id="2dafb-119">值</span><span class="sxs-lookup"><span data-stu-id="2dafb-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dafb-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2dafb-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2dafb-121"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2dafb-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2dafb-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="2dafb-122">Library</span></span><br/> | <dl> <span data-ttu-id="2dafb-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2dafb-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dafb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dafb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dafb-125">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="2dafb-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




