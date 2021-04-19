---
description: AddTail 方法會將專案附加至清單結尾。
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: CGenericList. AddTail 方法 (Wxlist .h) -pObj 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106993925"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="a794f-103">CGenericList. AddTail 方法 (Wxlist .h) -pObj 參數</span><span class="sxs-lookup"><span data-stu-id="a794f-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="a794f-104">方法會將 `AddTail` 專案附加至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="a794f-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a794f-105">語法</span><span class="sxs-lookup"><span data-stu-id="a794f-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="a794f-106">參數</span><span class="sxs-lookup"><span data-stu-id="a794f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a794f-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="a794f-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="a794f-108">**物件** 類型物件的指標， (範本類型) 。</span><span class="sxs-lookup"><span data-stu-id="a794f-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a794f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a794f-109">Return value</span></span>

<span data-ttu-id="a794f-110">傳回新結尾位置的位置值。</span><span class="sxs-lookup"><span data-stu-id="a794f-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="a794f-111">如果方法失敗，則會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a794f-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a794f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a794f-112">Requirements</span></span>

| <span data-ttu-id="a794f-113">需求</span><span class="sxs-lookup"><span data-stu-id="a794f-113">Requirement</span></span> | <span data-ttu-id="a794f-114">值</span><span class="sxs-lookup"><span data-stu-id="a794f-114">Value</span></span> |
|-|-|
| <span data-ttu-id="a794f-115">標頭</span><span class="sxs-lookup"><span data-stu-id="a794f-115">Header</span></span> | <span data-ttu-id="a794f-116">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="a794f-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="a794f-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="a794f-117">Library</span></span>| <span data-ttu-id="a794f-118"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="a794f-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a794f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a794f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a794f-120">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="a794f-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




