---
description: CRendererInputPin 方法是一種函式方法。
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: 'CRendererInputPin. CRendererInputPin (Renbase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982697"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="3364f-103">CRendererInputPin. CRendererInputPin 函數</span><span class="sxs-lookup"><span data-stu-id="3364f-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="3364f-104">`CRendererInputPin`方法是一種函式方法。</span><span class="sxs-lookup"><span data-stu-id="3364f-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3364f-105">語法</span><span class="sxs-lookup"><span data-stu-id="3364f-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="3364f-106">參數</span><span class="sxs-lookup"><span data-stu-id="3364f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3364f-107">*pRenderer*</span><span class="sxs-lookup"><span data-stu-id="3364f-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="3364f-108">[**CBaseRenderer**](cbaserenderer.md)物件的指標，該物件會執行篩選。</span><span class="sxs-lookup"><span data-stu-id="3364f-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="3364f-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="3364f-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3364f-110">接收 **HRESULT** 值之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="3364f-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="3364f-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="3364f-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="3364f-112">包含 pin 識別碼之寬字元字串的指標。</span><span class="sxs-lookup"><span data-stu-id="3364f-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3364f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3364f-113">Requirements</span></span>



| <span data-ttu-id="3364f-114">需求</span><span class="sxs-lookup"><span data-stu-id="3364f-114">Requirement</span></span> | <span data-ttu-id="3364f-115">值</span><span class="sxs-lookup"><span data-stu-id="3364f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3364f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3364f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3364f-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3364f-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3364f-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3364f-118">Library</span></span><br/> | <dl> <span data-ttu-id="3364f-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3364f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3364f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3364f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3364f-121">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="3364f-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




