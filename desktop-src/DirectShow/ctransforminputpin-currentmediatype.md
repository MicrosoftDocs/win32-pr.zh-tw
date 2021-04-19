---
description: CurrentMediaType 方法會抓取目前 pin 連接的媒體類型。
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: 'CTransformInputPin. CurrentMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59feca88e896b2a81a352b693e57ceaa5388d452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992581"
---
# <a name="ctransforminputpincurrentmediatype-method"></a><span data-ttu-id="81b55-103">CTransformInputPin. CurrentMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="81b55-103">CTransformInputPin.CurrentMediaType method</span></span>

<span data-ttu-id="81b55-104">方法會抓取 `CurrentMediaType` 目前連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="81b55-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b55-105">語法</span><span class="sxs-lookup"><span data-stu-id="81b55-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="81b55-106">參數</span><span class="sxs-lookup"><span data-stu-id="81b55-106">Parameters</span></span>

<span data-ttu-id="81b55-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="81b55-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81b55-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="81b55-108">Return value</span></span>

<span data-ttu-id="81b55-109">傳回 [**CBasePin：： m \_ mt**](cbasepin-m-mt.md) 成員變數的參考。</span><span class="sxs-lookup"><span data-stu-id="81b55-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b55-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="81b55-110">Requirements</span></span>



| <span data-ttu-id="81b55-111">需求</span><span class="sxs-lookup"><span data-stu-id="81b55-111">Requirement</span></span> | <span data-ttu-id="81b55-112">值</span><span class="sxs-lookup"><span data-stu-id="81b55-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b55-113">標頭</span><span class="sxs-lookup"><span data-stu-id="81b55-113">Header</span></span><br/>  | <dl> <span data-ttu-id="81b55-114"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81b55-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81b55-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="81b55-115">Library</span></span><br/> | <dl> <span data-ttu-id="81b55-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81b55-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




