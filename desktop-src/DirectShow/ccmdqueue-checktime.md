---
description: CheckTime 方法會判斷指定的時間是否為逾期。
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: 'CCmdQueue. CheckTime 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983236"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="577ff-103">CCmdQueue. CheckTime 方法</span><span class="sxs-lookup"><span data-stu-id="577ff-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="577ff-104">`CheckTime`方法會判斷指定的時間是否為逾期。</span><span class="sxs-lookup"><span data-stu-id="577ff-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="577ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="577ff-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="577ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="577ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577ff-107">*time*</span><span class="sxs-lookup"><span data-stu-id="577ff-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="577ff-108">檢查的時間。</span><span class="sxs-lookup"><span data-stu-id="577ff-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="577ff-109">*bStream*</span><span class="sxs-lookup"><span data-stu-id="577ff-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="577ff-110">如果 *time* 參數是資料流程時間值，則 **為 TRUE** ;如果 *時間* 是展示時間值，則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="577ff-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577ff-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="577ff-111">Return value</span></span>

<span data-ttu-id="577ff-112">如果尚未通過指定的時間，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="577ff-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="577ff-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="577ff-113">Requirements</span></span>



| <span data-ttu-id="577ff-114">需求</span><span class="sxs-lookup"><span data-stu-id="577ff-114">Requirement</span></span> | <span data-ttu-id="577ff-115">值</span><span class="sxs-lookup"><span data-stu-id="577ff-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="577ff-116">標頭</span><span class="sxs-lookup"><span data-stu-id="577ff-116">Header</span></span><br/>  | <dl> <span data-ttu-id="577ff-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="577ff-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="577ff-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="577ff-118">Library</span></span><br/> | <dl> <span data-ttu-id="577ff-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="577ff-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577ff-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="577ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577ff-121">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="577ff-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




