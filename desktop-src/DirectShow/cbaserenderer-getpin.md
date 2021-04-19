---
description: GetPin 方法會抓取 pin。
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: 'CBaseRenderer. GetPin 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987018"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="1477e-103">CBaseRenderer. GetPin 方法</span><span class="sxs-lookup"><span data-stu-id="1477e-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="1477e-104">方法會抓取 `GetPin` pin。</span><span class="sxs-lookup"><span data-stu-id="1477e-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="1477e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1477e-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="1477e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1477e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1477e-107">*n*</span><span class="sxs-lookup"><span data-stu-id="1477e-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="1477e-108">指定之 pin 的編號。</span><span class="sxs-lookup"><span data-stu-id="1477e-108">Number of the specified pin.</span></span> <span data-ttu-id="1477e-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1477e-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1477e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1477e-110">Return value</span></span>

<span data-ttu-id="1477e-111">傳回 [**CBaseRenderer：： m \_ pInputPin**](cbaserenderer-m-pinputpin.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="1477e-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="1477e-112">備註</span><span class="sxs-lookup"><span data-stu-id="1477e-112">Remarks</span></span>

<span data-ttu-id="1477e-113">這個方法會實 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法，這是 **CBaseFilter** 類別中的純虛擬。</span><span class="sxs-lookup"><span data-stu-id="1477e-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="1477e-114">篩選僅支援輸入 pin)  (一個 pin。</span><span class="sxs-lookup"><span data-stu-id="1477e-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="1477e-115">第一次呼叫這個方法時，它會將 pin 建立為新的 [**CRendererInputPin**](crendererinputpin.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1477e-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1477e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1477e-116">Requirements</span></span>



| <span data-ttu-id="1477e-117">需求</span><span class="sxs-lookup"><span data-stu-id="1477e-117">Requirement</span></span> | <span data-ttu-id="1477e-118">值</span><span class="sxs-lookup"><span data-stu-id="1477e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1477e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1477e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1477e-120"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1477e-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1477e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="1477e-121">Library</span></span><br/> | <dl> <span data-ttu-id="1477e-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1477e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1477e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1477e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1477e-124">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="1477e-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




