---
description: UsingDifferentAllocators 方法會判斷輸入和輸出圖釘是否使用不同的配置器。
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: 'CTransInPlaceFilter. UsingDifferentAllocators 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984445"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a><span data-ttu-id="3701d-103">CTransInPlaceFilter. UsingDifferentAllocators 方法</span><span class="sxs-lookup"><span data-stu-id="3701d-103">CTransInPlaceFilter.UsingDifferentAllocators method</span></span>

<span data-ttu-id="3701d-104">`UsingDifferentAllocators`方法會判斷輸入和輸出圖釘是否使用不同的配置器。</span><span class="sxs-lookup"><span data-stu-id="3701d-104">The `UsingDifferentAllocators` method determines whether the input and output pins are using different allocators.</span></span>

## <a name="syntax"></a><span data-ttu-id="3701d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3701d-105">Syntax</span></span>


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a><span data-ttu-id="3701d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3701d-106">Parameters</span></span>

<span data-ttu-id="3701d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3701d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3701d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3701d-108">Return value</span></span>

<span data-ttu-id="3701d-109">如果輸入和輸出圖釘使用不同的配置器，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3701d-109">Returns **TRUE** if the input and output pins are using different allocators, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3701d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3701d-110">Requirements</span></span>



| <span data-ttu-id="3701d-111">需求</span><span class="sxs-lookup"><span data-stu-id="3701d-111">Requirement</span></span> | <span data-ttu-id="3701d-112">值</span><span class="sxs-lookup"><span data-stu-id="3701d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3701d-113">標頭</span><span class="sxs-lookup"><span data-stu-id="3701d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3701d-114"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3701d-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3701d-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="3701d-115">Library</span></span><br/> | <dl> <span data-ttu-id="3701d-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3701d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3701d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3701d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3701d-118">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="3701d-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




