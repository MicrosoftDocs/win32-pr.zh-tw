---
description: AddHead 方法會在這份清單前面插入另一個清單。
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: 'CBaseList. AddHead 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990648"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="fc95d-103">CBaseList. AddHead 方法</span><span class="sxs-lookup"><span data-stu-id="fc95d-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="fc95d-104">`AddHead`方法會在這份清單前面插入另一個清單。</span><span class="sxs-lookup"><span data-stu-id="fc95d-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc95d-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc95d-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="fc95d-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc95d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc95d-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="fc95d-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="fc95d-108">要加入之專案清單的指標。</span><span class="sxs-lookup"><span data-stu-id="fc95d-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc95d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc95d-109">Return value</span></span>

<span data-ttu-id="fc95d-110">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fc95d-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc95d-111">備註</span><span class="sxs-lookup"><span data-stu-id="fc95d-111">Remarks</span></span>

<span data-ttu-id="fc95d-112">如果方法失敗，某些專案可能已加入至清單。</span><span class="sxs-lookup"><span data-stu-id="fc95d-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc95d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc95d-113">Requirements</span></span>



| <span data-ttu-id="fc95d-114">需求</span><span class="sxs-lookup"><span data-stu-id="fc95d-114">Requirement</span></span> | <span data-ttu-id="fc95d-115">值</span><span class="sxs-lookup"><span data-stu-id="fc95d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc95d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="fc95d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fc95d-117"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc95d-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fc95d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc95d-118">Library</span></span><br/> | <dl> <span data-ttu-id="fc95d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fc95d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc95d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc95d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc95d-121">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="fc95d-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




