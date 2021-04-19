---
description: 中斷連接方法會中斷目前的 pin 連線。 這個方法會實 IPin：:D isconnect 方法。
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: 'CBasePin 連接方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997009"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="d195c-104">CBasePin 中斷方法</span><span class="sxs-lookup"><span data-stu-id="d195c-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="d195c-105">`Disconnect`方法會中斷目前的 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="d195c-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="d195c-106">這個方法會實 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法。</span><span class="sxs-lookup"><span data-stu-id="d195c-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d195c-107">語法</span><span class="sxs-lookup"><span data-stu-id="d195c-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="d195c-108">參數</span><span class="sxs-lookup"><span data-stu-id="d195c-108">Parameters</span></span>

<span data-ttu-id="d195c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d195c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d195c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d195c-110">Return value</span></span>

<span data-ttu-id="d195c-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d195c-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d195c-112">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="d195c-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="d195c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d195c-113">Return code</span></span>                                                                                         | <span data-ttu-id="d195c-114">Description</span><span class="sxs-lookup"><span data-stu-id="d195c-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d195c-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d195c-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="d195c-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="d195c-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d195c-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d195c-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="d195c-118">成功。</span><span class="sxs-lookup"><span data-stu-id="d195c-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="d195c-119"><dt>**VFW \_ E \_ 未 \_ 停止**</dt></span><span class="sxs-lookup"><span data-stu-id="d195c-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="d195c-120">篩選準則為使用中，且 pin 不支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="d195c-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d195c-121">備註</span><span class="sxs-lookup"><span data-stu-id="d195c-121">Remarks</span></span>

<span data-ttu-id="d195c-122">基類會將大部分的工作委派給 [**CBasePin：:D isconnectinternal**](cbasepin-disconnectinternal.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d195c-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d195c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d195c-123">Requirements</span></span>



| <span data-ttu-id="d195c-124">需求</span><span class="sxs-lookup"><span data-stu-id="d195c-124">Requirement</span></span> | <span data-ttu-id="d195c-125">值</span><span class="sxs-lookup"><span data-stu-id="d195c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d195c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d195c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d195c-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d195c-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d195c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d195c-128">Library</span></span><br/> | <dl> <span data-ttu-id="d195c-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d195c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d195c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d195c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d195c-131">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="d195c-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




