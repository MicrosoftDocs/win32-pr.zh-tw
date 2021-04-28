---
description: CBasePin. SetMediaType 方法-SetMediaType 方法會設定連接的媒體類型。
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: 'CBasePin. SetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095983"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="0d3f4-103">CBasePin. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="0d3f4-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="0d3f4-104">`SetMediaType`方法會設定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3f4-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d3f4-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="0d3f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d3f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3f4-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="0d3f4-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="0d3f4-108">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3f4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d3f4-109">Return value</span></span>

<span data-ttu-id="0d3f4-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d3f4-111">備註</span><span class="sxs-lookup"><span data-stu-id="0d3f4-111">Remarks</span></span>

<span data-ttu-id="0d3f4-112">這個方法會建立 pin 連接的格式。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="0d3f4-113">在呼叫這個方法之前，pin 會呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，以判斷是否可接受媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="0d3f4-114">因此，會假設 *pmt* 參數是可接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="0d3f4-115">在基類中，這個方法會設定 [**CBasePin：： m \_ mt**](cbasepin-m-mt.md) 成員變數，並傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="0d3f4-116">如果在設定媒體類型時需要通知，則衍生類別可以覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0d3f4-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d3f4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d3f4-117">Requirements</span></span>



| <span data-ttu-id="0d3f4-118">需求</span><span class="sxs-lookup"><span data-stu-id="0d3f4-118">Requirement</span></span> | <span data-ttu-id="0d3f4-119">值</span><span class="sxs-lookup"><span data-stu-id="0d3f4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3f4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0d3f4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0d3f4-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0d3f4-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0d3f4-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d3f4-122">Library</span></span><br/> | <dl> <span data-ttu-id="0d3f4-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0d3f4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3f4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d3f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3f4-125">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="0d3f4-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




