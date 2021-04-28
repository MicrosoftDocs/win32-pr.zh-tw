---
description: CBaseFilter. GetPinCount 方法-GetPinCount 方法會抓取釘選數目。
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: 'CBaseFilter. GetPinCount 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099786"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="31cd3-103">CBaseFilter. GetPinCount 方法</span><span class="sxs-lookup"><span data-stu-id="31cd3-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="31cd3-104">方法會抓取 `GetPinCount` 釘選數目。</span><span class="sxs-lookup"><span data-stu-id="31cd3-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cd3-105">語法</span><span class="sxs-lookup"><span data-stu-id="31cd3-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="31cd3-106">參數</span><span class="sxs-lookup"><span data-stu-id="31cd3-106">Parameters</span></span>

<span data-ttu-id="31cd3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="31cd3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31cd3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="31cd3-108">Return value</span></span>

<span data-ttu-id="31cd3-109">傳回釘選數目。</span><span class="sxs-lookup"><span data-stu-id="31cd3-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="31cd3-110">備註</span><span class="sxs-lookup"><span data-stu-id="31cd3-110">Remarks</span></span>

<span data-ttu-id="31cd3-111">衍生的類別必須執行此純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="31cd3-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="31cd3-112">傳回此篩選器目前可用的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="31cd3-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="31cd3-113">篩選可以動態建立或終結圖釘。</span><span class="sxs-lookup"><span data-stu-id="31cd3-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="31cd3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="31cd3-114">Requirements</span></span>



| <span data-ttu-id="31cd3-115">需求</span><span class="sxs-lookup"><span data-stu-id="31cd3-115">Requirement</span></span> | <span data-ttu-id="31cd3-116">值</span><span class="sxs-lookup"><span data-stu-id="31cd3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31cd3-117">標頭</span><span class="sxs-lookup"><span data-stu-id="31cd3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="31cd3-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="31cd3-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="31cd3-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="31cd3-119">Library</span></span><br/> | <dl> <span data-ttu-id="31cd3-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="31cd3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31cd3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31cd3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cd3-122">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="31cd3-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




