---
description: IsFlushing 方法會查詢篩選目前是否正在排清。
ms.assetid: 366b6162-7a2c-4882-8774-8b4bf83012b4
title: 'CBaseInputPin. IsFlushing 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsFlushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5af91e78d10f480596b8e0820ee6de4c4df2998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982558"
---
# <a name="cbaseinputpinisflushing-method"></a><span data-ttu-id="9102b-103">CBaseInputPin. IsFlushing 方法</span><span class="sxs-lookup"><span data-stu-id="9102b-103">CBaseInputPin.IsFlushing method</span></span>

<span data-ttu-id="9102b-104">`IsFlushing`方法會查詢篩選目前是否正在排清。</span><span class="sxs-lookup"><span data-stu-id="9102b-104">The `IsFlushing` method queries whether the filter is currently flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9102b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9102b-105">Syntax</span></span>


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a><span data-ttu-id="9102b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9102b-106">Parameters</span></span>

<span data-ttu-id="9102b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9102b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9102b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9102b-108">Return value</span></span>

<span data-ttu-id="9102b-109">傳回 [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="9102b-109">Returns the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9102b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9102b-110">Requirements</span></span>



| <span data-ttu-id="9102b-111">需求</span><span class="sxs-lookup"><span data-stu-id="9102b-111">Requirement</span></span> | <span data-ttu-id="9102b-112">值</span><span class="sxs-lookup"><span data-stu-id="9102b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9102b-113">標頭</span><span class="sxs-lookup"><span data-stu-id="9102b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9102b-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9102b-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9102b-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="9102b-115">Library</span></span><br/> | <dl> <span data-ttu-id="9102b-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9102b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9102b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9102b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9102b-118">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9102b-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




