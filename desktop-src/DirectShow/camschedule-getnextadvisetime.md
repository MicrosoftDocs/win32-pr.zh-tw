---
description: GetNextAdviseTime 方法會捕獲下一個建議要求的時間。
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: 'CAMSchedule. GetNextAdviseTime 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987190"
---
# <a name="camschedulegetnextadvisetime-method"></a><span data-ttu-id="a53ca-103">CAMSchedule. GetNextAdviseTime 方法</span><span class="sxs-lookup"><span data-stu-id="a53ca-103">CAMSchedule.GetNextAdviseTime method</span></span>

<span data-ttu-id="a53ca-104">`GetNextAdviseTime`方法會捕獲下一個建議要求的時間。</span><span class="sxs-lookup"><span data-stu-id="a53ca-104">The `GetNextAdviseTime` method retrieves the time of the next advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="a53ca-105">Syntax</span></span>


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a><span data-ttu-id="a53ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="a53ca-106">Parameters</span></span>

<span data-ttu-id="a53ca-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a53ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a53ca-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a53ca-108">Return value</span></span>

<span data-ttu-id="a53ca-109">傳回下一個建議要求的參考時間，或 \_ 未排定任何要求的最大時間。</span><span class="sxs-lookup"><span data-stu-id="a53ca-109">Returns the reference time of the next advise request, or MAX\_TIME no requests are scheduled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a53ca-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a53ca-110">Requirements</span></span>



| <span data-ttu-id="a53ca-111">需求</span><span class="sxs-lookup"><span data-stu-id="a53ca-111">Requirement</span></span> | <span data-ttu-id="a53ca-112">值</span><span class="sxs-lookup"><span data-stu-id="a53ca-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53ca-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a53ca-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a53ca-114"><dt>Dsschedule (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a53ca-114"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="a53ca-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="a53ca-115">Library</span></span><br/> | <dl> <span data-ttu-id="a53ca-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a53ca-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a53ca-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a53ca-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53ca-118">**CAMSchedule 類別**</span><span class="sxs-lookup"><span data-stu-id="a53ca-118">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




