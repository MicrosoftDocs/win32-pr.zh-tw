---
description: AddBefore 方法會在指定的位置之前插入專案。 這個方法會使用 ' p ' 和 ' pObj ' 參數。
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: CGenericList. AddBefore 方法 (Wxlist .h) -p，pObj 參數
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103946282"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="bd195-104">CGenericList. AddBefore 方法 (Wxlist .h) -p，pObj 參數</span><span class="sxs-lookup"><span data-stu-id="bd195-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="bd195-105">方法會在 `AddBefore` 指定的位置之前插入專案。</span><span class="sxs-lookup"><span data-stu-id="bd195-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd195-106">語法</span><span class="sxs-lookup"><span data-stu-id="bd195-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="bd195-107">參數</span><span class="sxs-lookup"><span data-stu-id="bd195-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd195-108">*P*</span><span class="sxs-lookup"><span data-stu-id="bd195-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="bd195-109">要插入清單的位置。</span><span class="sxs-lookup"><span data-stu-id="bd195-109">Position before which to insert the list.</span></span> <span data-ttu-id="bd195-110">如果 *p* 是 **Null**，這個方法會將專案加入至清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="bd195-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="bd195-111">*pObj*</span><span class="sxs-lookup"><span data-stu-id="bd195-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="bd195-112">**物件** 類型物件的指標， (範本類型) 。</span><span class="sxs-lookup"><span data-stu-id="bd195-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd195-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd195-113">Return value</span></span>

<span data-ttu-id="bd195-114">傳回所插入專案的位置指標。</span><span class="sxs-lookup"><span data-stu-id="bd195-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd195-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd195-115">Requirements</span></span>

| <span data-ttu-id="bd195-116">需求</span><span class="sxs-lookup"><span data-stu-id="bd195-116">Requirement</span></span> | <span data-ttu-id="bd195-117">值</span><span class="sxs-lookup"><span data-stu-id="bd195-117">Value</span></span> |
|-|-|
| <span data-ttu-id="bd195-118">標頭</span><span class="sxs-lookup"><span data-stu-id="bd195-118">Header</span></span> | <span data-ttu-id="bd195-119">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="bd195-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="bd195-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd195-120">Library</span></span>| <span data-ttu-id="bd195-121"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="bd195-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="bd195-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd195-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd195-123">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="bd195-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




