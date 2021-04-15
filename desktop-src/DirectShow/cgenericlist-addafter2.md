---
description: AddAfter 方法會在指定的位置之後插入清單，並使用 ' pos ' 和 ' plist ' 參數。
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: CGenericList. AddAfter 方法 (Wxlist .h) -pos，plist 參數
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
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514729"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="e4c74-103">CGenericList. AddAfter 方法 (Wxlist .h) -pos，plist 參數</span><span class="sxs-lookup"><span data-stu-id="e4c74-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="e4c74-104">方法會在 `AddAfter` 指定的位置之後插入清單。</span><span class="sxs-lookup"><span data-stu-id="e4c74-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c74-105">語法</span><span class="sxs-lookup"><span data-stu-id="e4c74-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="e4c74-106">參數</span><span class="sxs-lookup"><span data-stu-id="e4c74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c74-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="e4c74-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c74-108">要插入清單的位置。</span><span class="sxs-lookup"><span data-stu-id="e4c74-108">Position to insert the list.</span></span> <span data-ttu-id="e4c74-109">此清單會插入此位置之後。</span><span class="sxs-lookup"><span data-stu-id="e4c74-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="e4c74-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="e4c74-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="e4c74-111">要插入之清單的指標。</span><span class="sxs-lookup"><span data-stu-id="e4c74-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c74-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4c74-112">Return value</span></span>

<span data-ttu-id="e4c74-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e4c74-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c74-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4c74-114">Requirements</span></span>

| <span data-ttu-id="e4c74-115">需求</span><span class="sxs-lookup"><span data-stu-id="e4c74-115">Requirement</span></span> | <span data-ttu-id="e4c74-116">值</span><span class="sxs-lookup"><span data-stu-id="e4c74-116">Value</span></span> |
|-|-|
| <span data-ttu-id="e4c74-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e4c74-117">Header</span></span> | <span data-ttu-id="e4c74-118">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="e4c74-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="e4c74-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4c74-119">Library</span></span>| <span data-ttu-id="e4c74-120"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="e4c74-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4c74-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4c74-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c74-122">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="e4c74-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




