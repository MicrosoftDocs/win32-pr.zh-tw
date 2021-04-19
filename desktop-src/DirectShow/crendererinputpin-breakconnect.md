---
description: BreakConnect 方法會從連接釋放 pin。 這個方法會覆寫 CBaseInputPin：： BreakConnect 方法。
ms.assetid: 47bfd666-4ef2-4978-a4f8-a83647dd782d
title: 'CRendererInputPin. BreakConnect 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2df44a190d2cc127da390556e52f3f960b07d57b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989632"
---
# <a name="crendererinputpinbreakconnect-method"></a><span data-ttu-id="e345a-104">CRendererInputPin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="e345a-104">CRendererInputPin.BreakConnect method</span></span>

<span data-ttu-id="e345a-105">**BreakConnect** 方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="e345a-105">The **BreakConnect** method releases the pin from a connection.</span></span> <span data-ttu-id="e345a-106">這個方法會覆寫 [**CBaseInputPin：： BreakConnect**](cbaseinputpin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e345a-106">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e345a-107">語法</span><span class="sxs-lookup"><span data-stu-id="e345a-107">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="e345a-108">參數</span><span class="sxs-lookup"><span data-stu-id="e345a-108">Parameters</span></span>

<span data-ttu-id="e345a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e345a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e345a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e345a-110">Return value</span></span>

<span data-ttu-id="e345a-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e345a-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e345a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e345a-112">Requirements</span></span>



| <span data-ttu-id="e345a-113">需求</span><span class="sxs-lookup"><span data-stu-id="e345a-113">Requirement</span></span> | <span data-ttu-id="e345a-114">值</span><span class="sxs-lookup"><span data-stu-id="e345a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e345a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="e345a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e345a-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e345a-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e345a-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="e345a-117">Library</span></span><br/> | <dl> <span data-ttu-id="e345a-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e345a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e345a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e345a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e345a-120">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="e345a-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




