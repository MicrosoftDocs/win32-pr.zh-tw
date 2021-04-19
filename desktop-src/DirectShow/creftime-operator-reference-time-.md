---
description: 參考 \_ 時間 () 運算子會將物件轉換為參考 \_ 時間資料類型。
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: CRefTime (Reftime) 的運算子 REFERENCE_TIME 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992952"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="4533a-103">CRefTime。 operator 參考 \_ 時間方法</span><span class="sxs-lookup"><span data-stu-id="4533a-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="4533a-104">運算子會將 `REFERENCE_TIME()` 物件轉換為 [**參考 \_ 時間**](reference-time.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4533a-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4533a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4533a-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="4533a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4533a-106">Parameters</span></span>

<span data-ttu-id="4533a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4533a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4533a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4533a-108">Return value</span></span>

<span data-ttu-id="4533a-109">傳回 [**CRefTime：： m \_ 時間**](creftime-m-time.md)的值。</span><span class="sxs-lookup"><span data-stu-id="4533a-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4533a-110">備註</span><span class="sxs-lookup"><span data-stu-id="4533a-110">Remarks</span></span>

<span data-ttu-id="4533a-111">下列範例示範如何使用這個 cast 運算子：</span><span class="sxs-lookup"><span data-stu-id="4533a-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="4533a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4533a-112">Requirements</span></span>



| <span data-ttu-id="4533a-113">需求</span><span class="sxs-lookup"><span data-stu-id="4533a-113">Requirement</span></span> | <span data-ttu-id="4533a-114">值</span><span class="sxs-lookup"><span data-stu-id="4533a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4533a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="4533a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4533a-116"><dt>Reftime (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4533a-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4533a-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="4533a-117">Library</span></span><br/> | <dl> <span data-ttu-id="4533a-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4533a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




