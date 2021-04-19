---
description: 旗標，指出 pin 是否先嘗試其慣用的媒體類型，再接收 pin。
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'CBasePin：： m_bTryMyTypesFirst 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978459"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="e56f5-103">CBasePin：： m \_ bTryMyTypesFirst 成員</span><span class="sxs-lookup"><span data-stu-id="e56f5-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="e56f5-104">旗標，指出 pin 是否先嘗試其慣用的媒體類型，再接收 pin。</span><span class="sxs-lookup"><span data-stu-id="e56f5-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="e56f5-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="e56f5-106">備註</span><span class="sxs-lookup"><span data-stu-id="e56f5-106">Remarks</span></span>

<span data-ttu-id="e56f5-107">此旗標的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e56f5-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="e56f5-108">如果旗標為 **TRUE**， [**CBasePin：： AgreeMediaType**](cbasepin-agreemediatype.md) 方法會反轉嘗試媒體類型的順序。</span><span class="sxs-lookup"><span data-stu-id="e56f5-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56f5-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="e56f5-109">Requirements</span></span>



| <span data-ttu-id="e56f5-110">需求</span><span class="sxs-lookup"><span data-stu-id="e56f5-110">Requirement</span></span> | <span data-ttu-id="e56f5-111">值</span><span class="sxs-lookup"><span data-stu-id="e56f5-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e56f5-112">標頭</span><span class="sxs-lookup"><span data-stu-id="e56f5-112">Header</span></span><br/>  | <dl> <span data-ttu-id="e56f5-113"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e56f5-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e56f5-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="e56f5-114">Library</span></span><br/> | <dl> <span data-ttu-id="e56f5-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e56f5-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56f5-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e56f5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56f5-117">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="e56f5-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




