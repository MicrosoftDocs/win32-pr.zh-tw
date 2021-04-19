---
description: 設定 pin 的媒體類型時，會呼叫 SetMediaType 方法。
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: 'CBaseRenderer. SetMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001204"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="a5306-103">CBaseRenderer. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="a5306-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="a5306-104">`SetMediaType`當釘選的媒體類型設定時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="a5306-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5306-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5306-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="a5306-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5306-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="a5306-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a5306-108">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a5306-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5306-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5306-109">Return value</span></span>

<span data-ttu-id="a5306-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a5306-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5306-111">備註</span><span class="sxs-lookup"><span data-stu-id="a5306-111">Remarks</span></span>

<span data-ttu-id="a5306-112">輸入 pin 會從它自己的 [**CRendererInputPin：： SetMediaType**](crendererinputpin-setmediatype.md) 方法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a5306-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="a5306-113">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="a5306-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5306-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5306-114">Requirements</span></span>



| <span data-ttu-id="a5306-115">需求</span><span class="sxs-lookup"><span data-stu-id="a5306-115">Requirement</span></span> | <span data-ttu-id="a5306-116">值</span><span class="sxs-lookup"><span data-stu-id="a5306-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5306-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a5306-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a5306-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a5306-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5306-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5306-119">Library</span></span><br/> | <dl> <span data-ttu-id="a5306-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a5306-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5306-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5306-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5306-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="a5306-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




