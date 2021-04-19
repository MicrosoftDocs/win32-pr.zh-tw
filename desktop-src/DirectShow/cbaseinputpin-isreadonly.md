---
description: 查詢配置器是否使用唯讀媒體範例。
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: 'CBaseInputPin. IsReadOnly 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d1e7930631328a277ce7332f483ee264b2d525
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000462"
---
# <a name="cbaseinputpinisreadonly-method"></a><span data-ttu-id="9f314-103">CBaseInputPin. IsReadOnly 方法</span><span class="sxs-lookup"><span data-stu-id="9f314-103">CBaseInputPin.IsReadOnly method</span></span>

<span data-ttu-id="9f314-104">查詢配置器是否使用唯讀媒體範例。</span><span class="sxs-lookup"><span data-stu-id="9f314-104">Queries whether the allocator uses read-only media samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f314-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f314-105">Syntax</span></span>


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a><span data-ttu-id="9f314-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f314-106">Parameters</span></span>

<span data-ttu-id="9f314-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9f314-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f314-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f314-108">Return value</span></span>

<span data-ttu-id="9f314-109">傳回 [**CBaseInputPin：： m \_ bReadOnly**](cbaseinputpin-m-breadonly.md) 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="9f314-109">Returns the value of the [**CBaseInputPin::m\_bReadOnly**](cbaseinputpin-m-breadonly.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f314-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f314-110">Requirements</span></span>



| <span data-ttu-id="9f314-111">需求</span><span class="sxs-lookup"><span data-stu-id="9f314-111">Requirement</span></span> | <span data-ttu-id="9f314-112">值</span><span class="sxs-lookup"><span data-stu-id="9f314-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f314-113">標頭</span><span class="sxs-lookup"><span data-stu-id="9f314-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9f314-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9f314-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f314-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f314-115">Library</span></span><br/> | <dl> <span data-ttu-id="9f314-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9f314-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f314-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f314-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f314-118">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="9f314-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




