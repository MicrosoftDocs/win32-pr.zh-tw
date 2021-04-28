---
description: CTransformInputPin. BreakConnect 方法-BreakConnect 方法會釋放連接的 pin。
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: 'CTransformInputPin. BreakConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085016"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="7a66d-103">CTransformInputPin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="7a66d-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="7a66d-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="7a66d-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a66d-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a66d-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="7a66d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a66d-106">Parameters</span></span>

<span data-ttu-id="7a66d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7a66d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a66d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a66d-108">Return value</span></span>

<span data-ttu-id="7a66d-109">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7a66d-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a66d-110">備註</span><span class="sxs-lookup"><span data-stu-id="7a66d-110">Remarks</span></span>

<span data-ttu-id="7a66d-111">這個方法會覆寫 [**CBaseInputPin：： BreakConnect**](cbaseinputpin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7a66d-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="7a66d-112">它會呼叫篩選器的 [**CTransformFilter：： BreakConnect**](ctransformfilter-breakconnect.md) 方法，它會 \_ 在基類中傳回 s OK。</span><span class="sxs-lookup"><span data-stu-id="7a66d-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="7a66d-113">衍生的類別可以覆寫 **CTransformFilter：： BreakConnect** 方法。</span><span class="sxs-lookup"><span data-stu-id="7a66d-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a66d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a66d-114">Requirements</span></span>



| <span data-ttu-id="7a66d-115">需求</span><span class="sxs-lookup"><span data-stu-id="7a66d-115">Requirement</span></span> | <span data-ttu-id="7a66d-116">值</span><span class="sxs-lookup"><span data-stu-id="7a66d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a66d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7a66d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7a66d-118"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7a66d-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a66d-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a66d-119">Library</span></span><br/> | <dl> <span data-ttu-id="7a66d-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7a66d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




