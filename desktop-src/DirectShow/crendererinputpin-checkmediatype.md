---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。 這個方法會覆寫 CBasePin：： CheckMediaType 方法。
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: 'CRendererInputPin. CheckMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989624"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="51cb6-104">CRendererInputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="51cb6-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="51cb6-105">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="51cb6-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="51cb6-106">這個方法會覆寫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="51cb6-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cb6-107">語法</span><span class="sxs-lookup"><span data-stu-id="51cb6-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="51cb6-108">參數</span><span class="sxs-lookup"><span data-stu-id="51cb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51cb6-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="51cb6-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="51cb6-110">媒體類型物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="51cb6-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51cb6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="51cb6-111">Return value</span></span>

<span data-ttu-id="51cb6-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="51cb6-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cb6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="51cb6-113">Requirements</span></span>



| <span data-ttu-id="51cb6-114">需求</span><span class="sxs-lookup"><span data-stu-id="51cb6-114">Requirement</span></span> | <span data-ttu-id="51cb6-115">值</span><span class="sxs-lookup"><span data-stu-id="51cb6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51cb6-116">標頭</span><span class="sxs-lookup"><span data-stu-id="51cb6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="51cb6-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="51cb6-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="51cb6-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="51cb6-118">Library</span></span><br/> | <dl> <span data-ttu-id="51cb6-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="51cb6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51cb6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51cb6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cb6-121">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="51cb6-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




