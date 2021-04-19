---
description: 下一個方法會抓取清單中的下一個位置。
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: 'CBaseList 下一個方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994312"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="20d66-103">CBaseList. Next 方法</span><span class="sxs-lookup"><span data-stu-id="20d66-103">CBaseList.Next method</span></span>

<span data-ttu-id="20d66-104">方法會抓取 `Next` 清單中的下一個位置。</span><span class="sxs-lookup"><span data-stu-id="20d66-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d66-105">語法</span><span class="sxs-lookup"><span data-stu-id="20d66-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="20d66-106">參數</span><span class="sxs-lookup"><span data-stu-id="20d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20d66-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="20d66-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="20d66-108">位置值。</span><span class="sxs-lookup"><span data-stu-id="20d66-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20d66-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="20d66-109">Return value</span></span>

<span data-ttu-id="20d66-110">傳回位於 *pos* 所指定位置之後的位置指標。</span><span class="sxs-lookup"><span data-stu-id="20d66-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="20d66-111">備註</span><span class="sxs-lookup"><span data-stu-id="20d66-111">Remarks</span></span>

<span data-ttu-id="20d66-112">如果 *pos* 是清單中的最後一個位置，則方法會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="20d66-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="20d66-113">如果 *pos* 是 **Null**，則方法會傳回清單中的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="20d66-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="20d66-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="20d66-114">Requirements</span></span>



| <span data-ttu-id="20d66-115">需求</span><span class="sxs-lookup"><span data-stu-id="20d66-115">Requirement</span></span> | <span data-ttu-id="20d66-116">值</span><span class="sxs-lookup"><span data-stu-id="20d66-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d66-117">標頭</span><span class="sxs-lookup"><span data-stu-id="20d66-117">Header</span></span><br/>  | <dl> <span data-ttu-id="20d66-118"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="20d66-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="20d66-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="20d66-119">Library</span></span><br/> | <dl> <span data-ttu-id="20d66-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="20d66-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20d66-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20d66-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d66-122">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="20d66-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




