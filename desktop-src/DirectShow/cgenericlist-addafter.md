---
description: AddAfter 方法會在指定的位置之後插入專案，並使用 ' p ' 和 ' pObj ' 參數。
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: CGenericList. AddAfter 方法 (Wxlist .h) -p，pObj 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323439"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="77de2-103">CGenericList. AddAfter 方法 (Wxlist .h) -p，pObj 參數</span><span class="sxs-lookup"><span data-stu-id="77de2-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="77de2-104">方法會在 `AddAfter` 指定的位置之後插入專案。</span><span class="sxs-lookup"><span data-stu-id="77de2-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="77de2-105">語法</span><span class="sxs-lookup"><span data-stu-id="77de2-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="77de2-106">參數</span><span class="sxs-lookup"><span data-stu-id="77de2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77de2-107">*P*</span><span class="sxs-lookup"><span data-stu-id="77de2-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="77de2-108">要在其後加入專案的位置。</span><span class="sxs-lookup"><span data-stu-id="77de2-108">Position after which to add the item.</span></span> <span data-ttu-id="77de2-109">如果 *p* 為 **Null**，則方法會將專案加入至清單的開頭。</span><span class="sxs-lookup"><span data-stu-id="77de2-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="77de2-110">*pObj*</span><span class="sxs-lookup"><span data-stu-id="77de2-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="77de2-111">**物件** 類型物件的指標， (範本類型) 。</span><span class="sxs-lookup"><span data-stu-id="77de2-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77de2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="77de2-112">Return value</span></span>

<span data-ttu-id="77de2-113">傳回所插入專案的位置指標。</span><span class="sxs-lookup"><span data-stu-id="77de2-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="77de2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="77de2-114">Requirements</span></span>

| <span data-ttu-id="77de2-115">需求</span><span class="sxs-lookup"><span data-stu-id="77de2-115">Requirement</span></span> | <span data-ttu-id="77de2-116">值</span><span class="sxs-lookup"><span data-stu-id="77de2-116">Value</span></span> |
|-|-|
| <span data-ttu-id="77de2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="77de2-117">Header</span></span> | <span data-ttu-id="77de2-118">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="77de2-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="77de2-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="77de2-119">Library</span></span>| <span data-ttu-id="77de2-120"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="77de2-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="77de2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77de2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77de2-122">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="77de2-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




