---
description: CTransformOutputPin. CurrentMediaType 方法-CurrentMediaType 方法會抓取目前 pin 連接的媒體類型。
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: 'CTransformOutputPin. CurrentMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094906"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="9df43-103">CTransformOutputPin. CurrentMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="9df43-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="9df43-104">方法會抓取 `CurrentMediaType` 目前連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9df43-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df43-105">語法</span><span class="sxs-lookup"><span data-stu-id="9df43-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="9df43-106">參數</span><span class="sxs-lookup"><span data-stu-id="9df43-106">Parameters</span></span>

<span data-ttu-id="9df43-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9df43-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9df43-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9df43-108">Return value</span></span>

<span data-ttu-id="9df43-109">傳回 [**CBasePin：： m \_ mt**](cbasepin-m-mt.md) 成員變數的參考。</span><span class="sxs-lookup"><span data-stu-id="9df43-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9df43-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9df43-110">Requirements</span></span>



| <span data-ttu-id="9df43-111">需求</span><span class="sxs-lookup"><span data-stu-id="9df43-111">Requirement</span></span> | <span data-ttu-id="9df43-112">值</span><span class="sxs-lookup"><span data-stu-id="9df43-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df43-113">標頭</span><span class="sxs-lookup"><span data-stu-id="9df43-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9df43-114"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9df43-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9df43-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="9df43-115">Library</span></span><br/> | <dl> <span data-ttu-id="9df43-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9df43-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




