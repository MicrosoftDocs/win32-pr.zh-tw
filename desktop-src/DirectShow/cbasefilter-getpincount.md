---
description: GetPinCount 方法會抓取釘選數目。
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993532"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="8418b-103">CBaseFilter. GetPinCount 方法</span><span class="sxs-lookup"><span data-stu-id="8418b-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="8418b-104">方法會抓取 `GetPinCount` 釘選數目。</span><span class="sxs-lookup"><span data-stu-id="8418b-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="8418b-105">語法</span><span class="sxs-lookup"><span data-stu-id="8418b-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="8418b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8418b-106">Parameters</span></span>

<span data-ttu-id="8418b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8418b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8418b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8418b-108">Return value</span></span>

<span data-ttu-id="8418b-109">傳回釘選數目。</span><span class="sxs-lookup"><span data-stu-id="8418b-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="8418b-110">備註</span><span class="sxs-lookup"><span data-stu-id="8418b-110">Remarks</span></span>

<span data-ttu-id="8418b-111">衍生的類別必須執行此純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="8418b-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="8418b-112">傳回此篩選器目前可用的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="8418b-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="8418b-113">篩選可以動態建立或終結圖釘。</span><span class="sxs-lookup"><span data-stu-id="8418b-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="8418b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8418b-114">Requirements</span></span>



| <span data-ttu-id="8418b-115">需求</span><span class="sxs-lookup"><span data-stu-id="8418b-115">Requirement</span></span> | <span data-ttu-id="8418b-116">值</span><span class="sxs-lookup"><span data-stu-id="8418b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8418b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8418b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8418b-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8418b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8418b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8418b-119">Library</span></span><br/> | <dl> <span data-ttu-id="8418b-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8418b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8418b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8418b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8418b-122">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="8418b-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




