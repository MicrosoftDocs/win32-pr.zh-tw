---
description: QueryDirection 方法會 (輸入或輸出) 來抓取 pin 的方向。 這個方法會實 IPin：： QueryDirection 方法。
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: 'CBasePin. QueryDirection 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999234"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="2ef56-104">CBasePin. QueryDirection 方法</span><span class="sxs-lookup"><span data-stu-id="2ef56-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="2ef56-105">方法會抓取 `QueryDirection` pin (輸入或輸出) 的方向。</span><span class="sxs-lookup"><span data-stu-id="2ef56-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="2ef56-106">這個方法會實 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 方法。</span><span class="sxs-lookup"><span data-stu-id="2ef56-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef56-107">語法</span><span class="sxs-lookup"><span data-stu-id="2ef56-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="2ef56-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ef56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef56-109">*pPinDir*</span><span class="sxs-lookup"><span data-stu-id="2ef56-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="2ef56-110">變數的指標，此變數會接收釘選 [**\_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction) 列舉類型的成員。</span><span class="sxs-lookup"><span data-stu-id="2ef56-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef56-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ef56-111">Return value</span></span>

<span data-ttu-id="2ef56-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="2ef56-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef56-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ef56-113">Requirements</span></span>



| <span data-ttu-id="2ef56-114">需求</span><span class="sxs-lookup"><span data-stu-id="2ef56-114">Requirement</span></span> | <span data-ttu-id="2ef56-115">值</span><span class="sxs-lookup"><span data-stu-id="2ef56-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef56-116">標頭</span><span class="sxs-lookup"><span data-stu-id="2ef56-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2ef56-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2ef56-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2ef56-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="2ef56-118">Library</span></span><br/> | <dl> <span data-ttu-id="2ef56-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2ef56-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef56-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ef56-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef56-121">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="2ef56-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




