---
description: GetNext 方法會在指定的位置抓取專案，並將位置往前移。
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: 'CGenericList. GetNext 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978774"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="6a7ed-103">CGenericList. GetNext 方法</span><span class="sxs-lookup"><span data-stu-id="6a7ed-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="6a7ed-104">`GetNext`方法會在指定的位置抓取專案，並將位置往前移。</span><span class="sxs-lookup"><span data-stu-id="6a7ed-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7ed-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a7ed-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="6a7ed-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a7ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a7ed-107">*rp* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="6a7ed-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7ed-108">位置值的參考。</span><span class="sxs-lookup"><span data-stu-id="6a7ed-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a7ed-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a7ed-109">Return value</span></span>

<span data-ttu-id="6a7ed-110">傳回)  (範本型別 **物件** 之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6a7ed-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a7ed-111">備註</span><span class="sxs-lookup"><span data-stu-id="6a7ed-111">Remarks</span></span>

<span data-ttu-id="6a7ed-112">這個方法會將位置指標往前移到下一個位置。</span><span class="sxs-lookup"><span data-stu-id="6a7ed-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="6a7ed-113">如果位置指標移動超過清單的結尾，則方法會將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6a7ed-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="6a7ed-114">如果 *rp* 為 **null**，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="6a7ed-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a7ed-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a7ed-115">Requirements</span></span>



| <span data-ttu-id="6a7ed-116">需求</span><span class="sxs-lookup"><span data-stu-id="6a7ed-116">Requirement</span></span> | <span data-ttu-id="6a7ed-117">值</span><span class="sxs-lookup"><span data-stu-id="6a7ed-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7ed-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6a7ed-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6a7ed-119"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6a7ed-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6a7ed-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a7ed-120">Library</span></span><br/> | <dl> <span data-ttu-id="6a7ed-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6a7ed-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7ed-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a7ed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7ed-123">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="6a7ed-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




