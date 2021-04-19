---
description: GetPin 方法會抓取 pin。 這個方法會實作為純虛擬 CBaseFilter：： GetPin 方法。
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: 'CSource. GetPin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998773"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="cd99d-104">CSource. GetPin 方法</span><span class="sxs-lookup"><span data-stu-id="cd99d-104">CSource.GetPin method</span></span>

<span data-ttu-id="cd99d-105">方法會抓取 `GetPin` pin。</span><span class="sxs-lookup"><span data-stu-id="cd99d-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="cd99d-106">這個方法會實作為純虛擬 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cd99d-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd99d-107">語法</span><span class="sxs-lookup"><span data-stu-id="cd99d-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="cd99d-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd99d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd99d-109">*n*</span><span class="sxs-lookup"><span data-stu-id="cd99d-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="cd99d-110">指定之 pin 的編號。</span><span class="sxs-lookup"><span data-stu-id="cd99d-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd99d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd99d-111">Return value</span></span>

<span data-ttu-id="cd99d-112">傳回 [**CBasePin**](cbasepin.md) 物件的指標，該物件會執行釘選，如果索引超出範圍，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="cd99d-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd99d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd99d-113">Requirements</span></span>



| <span data-ttu-id="cd99d-114">需求</span><span class="sxs-lookup"><span data-stu-id="cd99d-114">Requirement</span></span> | <span data-ttu-id="cd99d-115">值</span><span class="sxs-lookup"><span data-stu-id="cd99d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd99d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cd99d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cd99d-117"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="cd99d-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cd99d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd99d-118">Library</span></span><br/> | <dl> <span data-ttu-id="cd99d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cd99d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd99d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd99d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd99d-121">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="cd99d-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




