---
description: AddBefore 方法會在指定的位置之前插入清單。 這個方法會使用 ' pos ' 和 ' pList ' 參數。
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: CGenericList. AddBefore 方法 (Wxlist .h) -pos，pList 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103696892"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="859a0-104">CGenericList. AddBefore 方法 (Wxlist .h) -pos，pList 參數</span><span class="sxs-lookup"><span data-stu-id="859a0-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="859a0-105">方法會在 `AddBefore` 指定的位置之前插入清單。</span><span class="sxs-lookup"><span data-stu-id="859a0-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="859a0-106">語法</span><span class="sxs-lookup"><span data-stu-id="859a0-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="859a0-107">參數</span><span class="sxs-lookup"><span data-stu-id="859a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="859a0-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="859a0-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="859a0-109">要插入清單的位置。</span><span class="sxs-lookup"><span data-stu-id="859a0-109">Position to insert the list.</span></span> <span data-ttu-id="859a0-110">此清單會插入此位置之前。</span><span class="sxs-lookup"><span data-stu-id="859a0-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="859a0-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="859a0-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="859a0-112">要插入之清單的指標。</span><span class="sxs-lookup"><span data-stu-id="859a0-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="859a0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="859a0-113">Return value</span></span>

<span data-ttu-id="859a0-114">如果成功， **則傳回 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="859a0-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="859a0-115">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="859a0-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="859a0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="859a0-116">Requirements</span></span>

| <span data-ttu-id="859a0-117">需求</span><span class="sxs-lookup"><span data-stu-id="859a0-117">Requirement</span></span> | <span data-ttu-id="859a0-118">值</span><span class="sxs-lookup"><span data-stu-id="859a0-118">Value</span></span> |
|-|-|
| <span data-ttu-id="859a0-119">標頭</span><span class="sxs-lookup"><span data-stu-id="859a0-119">Header</span></span> | <span data-ttu-id="859a0-120">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="859a0-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="859a0-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="859a0-121">Library</span></span>| <span data-ttu-id="859a0-122"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="859a0-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="859a0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="859a0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="859a0-124">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="859a0-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




