---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: 'CBasePin. CheckMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000973"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="357b0-103">CBasePin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="357b0-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="357b0-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="357b0-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="357b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="357b0-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="357b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="357b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="357b0-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="357b0-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="357b0-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="357b0-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="357b0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="357b0-109">Return value</span></span>

<span data-ttu-id="357b0-110">\_如果建議的媒體類型是可接受的，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="357b0-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="357b0-111">否則，會傳回 \_ FALSE 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="357b0-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="357b0-112">備註</span><span class="sxs-lookup"><span data-stu-id="357b0-112">Remarks</span></span>

<span data-ttu-id="357b0-113">衍生的類別必須覆寫此純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="357b0-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="357b0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="357b0-114">Requirements</span></span>



| <span data-ttu-id="357b0-115">需求</span><span class="sxs-lookup"><span data-stu-id="357b0-115">Requirement</span></span> | <span data-ttu-id="357b0-116">值</span><span class="sxs-lookup"><span data-stu-id="357b0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="357b0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="357b0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="357b0-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="357b0-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="357b0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="357b0-119">Library</span></span><br/> | <dl> <span data-ttu-id="357b0-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="357b0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="357b0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="357b0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357b0-122">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="357b0-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




