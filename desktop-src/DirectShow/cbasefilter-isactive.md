---
description: IsActive 方法會判斷篩選目前是否正在使用中， (執行中或已暫停) 。
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: 'CBaseFilter. IsActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63cf2cd78bb61562c9b4d6a09de3d88c88d4c643
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998666"
---
# <a name="cbasefilterisactive-method"></a><span data-ttu-id="9633a-103">CBaseFilter. IsActive 方法</span><span class="sxs-lookup"><span data-stu-id="9633a-103">CBaseFilter.IsActive method</span></span>

<span data-ttu-id="9633a-104">`IsActive`方法會判斷篩選目前是否為作用中， (執行中或已暫停) 。</span><span class="sxs-lookup"><span data-stu-id="9633a-104">The `IsActive` method determines whether the filter is currently active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="9633a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9633a-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="9633a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9633a-106">Parameters</span></span>

<span data-ttu-id="9633a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9633a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9633a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9633a-108">Return value</span></span>

<span data-ttu-id="9633a-109">如果篩選已暫停或正在執行，則傳回 **TRUE** ; 如果已停止，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9633a-109">Returns **TRUE** if the filter is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="9633a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9633a-110">Requirements</span></span>



| <span data-ttu-id="9633a-111">需求</span><span class="sxs-lookup"><span data-stu-id="9633a-111">Requirement</span></span> | <span data-ttu-id="9633a-112">值</span><span class="sxs-lookup"><span data-stu-id="9633a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9633a-113">標頭</span><span class="sxs-lookup"><span data-stu-id="9633a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9633a-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9633a-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9633a-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="9633a-115">Library</span></span><br/> | <dl> <span data-ttu-id="9633a-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9633a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9633a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9633a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9633a-118">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="9633a-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




