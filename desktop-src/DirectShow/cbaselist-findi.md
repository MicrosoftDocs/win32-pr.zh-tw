---
description: FindI 方法會抓取保留指定專案的第一個位置。
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: 'CBaseList. FindI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982637"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="ced62-103">CBaseList. FindI 方法</span><span class="sxs-lookup"><span data-stu-id="ced62-103">CBaseList.FindI method</span></span>

<span data-ttu-id="ced62-104">`FindI`方法會抓取保留指定專案的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="ced62-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced62-105">語法</span><span class="sxs-lookup"><span data-stu-id="ced62-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="ced62-106">參數</span><span class="sxs-lookup"><span data-stu-id="ced62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced62-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="ced62-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="ced62-108">專案的指標。</span><span class="sxs-lookup"><span data-stu-id="ced62-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced62-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ced62-109">Return value</span></span>

<span data-ttu-id="ced62-110">傳回位置值，如果專案不在清單中，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="ced62-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced62-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ced62-111">Requirements</span></span>



| <span data-ttu-id="ced62-112">需求</span><span class="sxs-lookup"><span data-stu-id="ced62-112">Requirement</span></span> | <span data-ttu-id="ced62-113">值</span><span class="sxs-lookup"><span data-stu-id="ced62-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced62-114">標頭</span><span class="sxs-lookup"><span data-stu-id="ced62-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ced62-115"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ced62-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ced62-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="ced62-116">Library</span></span><br/> | <dl> <span data-ttu-id="ced62-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ced62-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ced62-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ced62-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced62-119">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="ced62-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




