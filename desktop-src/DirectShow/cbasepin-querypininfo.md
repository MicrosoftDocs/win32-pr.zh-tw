---
description: QueryPinInfo 方法會抓取釘選的相關資訊。 這個方法會實 IPin：： QueryPinInfo 方法。
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: 'CBasePin. QueryPinInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992929"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="59f1f-104">CBasePin. QueryPinInfo 方法</span><span class="sxs-lookup"><span data-stu-id="59f1f-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="59f1f-105">方法會抓取 `QueryPinInfo` 釘選的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="59f1f-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="59f1f-106">這個方法會實 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="59f1f-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f1f-107">語法</span><span class="sxs-lookup"><span data-stu-id="59f1f-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="59f1f-108">參數</span><span class="sxs-lookup"><span data-stu-id="59f1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f1f-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="59f1f-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="59f1f-110">接收釘選資訊之釘選資訊結構的指標。 [**\_**](/windows/win32/api/strmif/ns-strmif-pin_info)</span><span class="sxs-lookup"><span data-stu-id="59f1f-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f1f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="59f1f-111">Return value</span></span>

<span data-ttu-id="59f1f-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="59f1f-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="59f1f-113">備註</span><span class="sxs-lookup"><span data-stu-id="59f1f-113">Remarks</span></span>

<span data-ttu-id="59f1f-114">這個方法會針對 PIN 資訊結構的 **achName** 成員使用 [**CBasePin：： m \_ pName**](cbasepin-m-pname.md)成員變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="59f1f-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="59f1f-115">當方法傳回時，如果 PIN 資訊結構的 **pFilter** 成員 \_ 為非 **Null**，則會有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="59f1f-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="59f1f-116">當您完成時，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="59f1f-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="59f1f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="59f1f-117">Requirements</span></span>



| <span data-ttu-id="59f1f-118">需求</span><span class="sxs-lookup"><span data-stu-id="59f1f-118">Requirement</span></span> | <span data-ttu-id="59f1f-119">值</span><span class="sxs-lookup"><span data-stu-id="59f1f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f1f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="59f1f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="59f1f-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="59f1f-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="59f1f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="59f1f-122">Library</span></span><br/> | <dl> <span data-ttu-id="59f1f-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="59f1f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f1f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59f1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f1f-125">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="59f1f-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




