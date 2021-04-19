---
description: PassNotify 方法會將品質控制訊息傳遞至適當的物件。
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: 'CBaseInputPin. PassNotify 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998392"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="eadd7-103">CBaseInputPin. PassNotify 方法</span><span class="sxs-lookup"><span data-stu-id="eadd7-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="eadd7-104">方法會將 `PassNotify` 品質控制訊息傳遞至適當的物件。</span><span class="sxs-lookup"><span data-stu-id="eadd7-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="eadd7-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="eadd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="eadd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eadd7-107">*問*</span><span class="sxs-lookup"><span data-stu-id="eadd7-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="eadd7-108">包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。</span><span class="sxs-lookup"><span data-stu-id="eadd7-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eadd7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eadd7-109">Return value</span></span>

<span data-ttu-id="eadd7-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="eadd7-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eadd7-111">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="eadd7-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="eadd7-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eadd7-112">Return code</span></span>                                                                                       | <span data-ttu-id="eadd7-113">Description</span><span class="sxs-lookup"><span data-stu-id="eadd7-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="eadd7-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eadd7-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="eadd7-115">成功。</span><span class="sxs-lookup"><span data-stu-id="eadd7-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="eadd7-116"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eadd7-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="eadd7-117">找不到接受訊息的物件。</span><span class="sxs-lookup"><span data-stu-id="eadd7-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eadd7-118">備註</span><span class="sxs-lookup"><span data-stu-id="eadd7-118">Remarks</span></span>

<span data-ttu-id="eadd7-119">如果篩選器不會處理品質控制訊息，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="eadd7-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="eadd7-120">這個方法會依照喜好設定，將訊息傳遞至下列其中一個物件：</span><span class="sxs-lookup"><span data-stu-id="eadd7-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="eadd7-121">外部品質控制管理員（如果呼叫 [**IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) 方法）。</span><span class="sxs-lookup"><span data-stu-id="eadd7-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="eadd7-122">上游輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="eadd7-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="eadd7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="eadd7-123">Requirements</span></span>



| <span data-ttu-id="eadd7-124">需求</span><span class="sxs-lookup"><span data-stu-id="eadd7-124">Requirement</span></span> | <span data-ttu-id="eadd7-125">值</span><span class="sxs-lookup"><span data-stu-id="eadd7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eadd7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="eadd7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eadd7-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eadd7-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eadd7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="eadd7-128">Library</span></span><br/> | <dl> <span data-ttu-id="eadd7-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eadd7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadd7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eadd7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadd7-131">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="eadd7-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="eadd7-132">品質控制管理</span><span class="sxs-lookup"><span data-stu-id="eadd7-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




