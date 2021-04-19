---
description: QueryInternalConnections 方法會將在內部連接的釘選到篩選) 內 (的釘選。 這個方法會實 IPin：： QueryInternalConnections 方法。
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: 'CBasePin. QueryInternalConnections 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983045"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="d5cd7-104">CBasePin. QueryInternalConnections 方法</span><span class="sxs-lookup"><span data-stu-id="d5cd7-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="d5cd7-105">`QueryInternalConnections`方法會將在內部連接的釘選到篩選) 內 (的釘選。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="d5cd7-106">這個方法會實 [**IPin：： QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) 方法。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5cd7-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5cd7-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="d5cd7-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5cd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5cd7-109">*apPin*</span><span class="sxs-lookup"><span data-stu-id="d5cd7-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d5cd7-110">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)指標陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="d5cd7-111">*nPin*</span><span class="sxs-lookup"><span data-stu-id="d5cd7-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d5cd7-112">在 [輸入] 上，指定陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="d5cd7-113">當方法傳回時，值會設定為數組中傳回的指標數目。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5cd7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5cd7-114">Return value</span></span>

<span data-ttu-id="d5cd7-115">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d5cd7-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d5cd7-116">Return code</span></span>                                                                               | <span data-ttu-id="d5cd7-117">Description</span><span class="sxs-lookup"><span data-stu-id="d5cd7-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="d5cd7-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="d5cd7-119">陣列大小不足。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="d5cd7-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d5cd7-121">成功。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="d5cd7-122"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="d5cd7-123">失敗。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="d5cd7-124"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="d5cd7-125">未實作。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d5cd7-126">備註</span><span class="sxs-lookup"><span data-stu-id="d5cd7-126">Remarks</span></span>

<span data-ttu-id="d5cd7-127">在某些篩選器上，輸入圖釘會對應到特定的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="d5cd7-128">針對每個圖釘，此方法會在陣列中填入對應的釘選指標。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="d5cd7-129">如果每個輸入 pin 都提供每個輸出 pin 的資料，則傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="d5cd7-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cd7-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5cd7-130">Requirements</span></span>



| <span data-ttu-id="d5cd7-131">需求</span><span class="sxs-lookup"><span data-stu-id="d5cd7-131">Requirement</span></span> | <span data-ttu-id="d5cd7-132">值</span><span class="sxs-lookup"><span data-stu-id="d5cd7-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5cd7-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d5cd7-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d5cd7-134"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5cd7-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5cd7-135">Library</span></span><br/> | <dl> <span data-ttu-id="d5cd7-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d5cd7-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5cd7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5cd7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5cd7-138">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="d5cd7-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




