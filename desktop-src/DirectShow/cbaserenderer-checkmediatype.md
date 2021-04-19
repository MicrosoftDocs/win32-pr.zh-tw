---
description: CheckMediaType 方法會判斷篩選是否接受特定的媒體類型。
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: 'CBaseRenderer. CheckMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997008"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="6b827-103">CBaseRenderer. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="6b827-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="6b827-104">`CheckMediaType`方法會判斷篩選準則是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b827-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b827-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b827-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6b827-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b827-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="6b827-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6b827-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b827-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b827-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b827-109">Return value</span></span>

<span data-ttu-id="6b827-110">\_如果建議的媒體類型是可接受的，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="6b827-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="6b827-111">否則，會傳回 \_ FALSE 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6b827-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b827-112">備註</span><span class="sxs-lookup"><span data-stu-id="6b827-112">Remarks</span></span>

<span data-ttu-id="6b827-113">輸入 pin 會從它自己的 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6b827-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="6b827-114">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="6b827-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b827-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b827-115">Requirements</span></span>



| <span data-ttu-id="6b827-116">需求</span><span class="sxs-lookup"><span data-stu-id="6b827-116">Requirement</span></span> | <span data-ttu-id="6b827-117">值</span><span class="sxs-lookup"><span data-stu-id="6b827-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b827-118">標頭</span><span class="sxs-lookup"><span data-stu-id="6b827-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6b827-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6b827-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b827-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b827-120">Library</span></span><br/> | <dl> <span data-ttu-id="6b827-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6b827-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b827-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b827-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b827-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="6b827-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




