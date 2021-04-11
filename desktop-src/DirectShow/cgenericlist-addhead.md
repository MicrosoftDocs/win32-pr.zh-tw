---
description: AddHead 方法會將專案加入至清單的前方。
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: CGenericList. AddHead 方法 (Wxlist .h) -pObj 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104035450"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="81e82-103">CGenericList. AddHead 方法 (Wxlist .h) -pObj 參數</span><span class="sxs-lookup"><span data-stu-id="81e82-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="81e82-104">`AddHead`方法會將專案加入至清單的前方。</span><span class="sxs-lookup"><span data-stu-id="81e82-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e82-105">語法</span><span class="sxs-lookup"><span data-stu-id="81e82-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="81e82-106">參數</span><span class="sxs-lookup"><span data-stu-id="81e82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e82-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="81e82-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="81e82-108">**物件** 類型物件的指標， (範本類型) 。</span><span class="sxs-lookup"><span data-stu-id="81e82-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e82-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="81e82-109">Return value</span></span>

<span data-ttu-id="81e82-110">傳回位置值，表示新的標頭位置。</span><span class="sxs-lookup"><span data-stu-id="81e82-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="81e82-111">如果方法失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="81e82-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e82-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="81e82-112">Requirements</span></span>

| <span data-ttu-id="81e82-113">需求</span><span class="sxs-lookup"><span data-stu-id="81e82-113">Requirement</span></span> | <span data-ttu-id="81e82-114">值</span><span class="sxs-lookup"><span data-stu-id="81e82-114">Value</span></span> |
|-|-|
| <span data-ttu-id="81e82-115">標頭</span><span class="sxs-lookup"><span data-stu-id="81e82-115">Header</span></span> | <span data-ttu-id="81e82-116">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="81e82-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="81e82-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="81e82-117">Library</span></span>| <span data-ttu-id="81e82-118"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="81e82-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="81e82-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81e82-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e82-120">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="81e82-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




