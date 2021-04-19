---
description: 通知方法會通知 pin，要求品質變更。 這個方法會執行 IQualityControl：： Notify 方法。
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: 'CTransformOutputPin： Notify 方法 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991139"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="0cd0d-104">CTransformOutputPin。通知方法</span><span class="sxs-lookup"><span data-stu-id="0cd0d-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="0cd0d-105">`Notify`方法會通知 pin，要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="0cd0d-106">這個方法會 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd0d-107">語法</span><span class="sxs-lookup"><span data-stu-id="0cd0d-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="0cd0d-108">參數</span><span class="sxs-lookup"><span data-stu-id="0cd0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd0d-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="0cd0d-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="0cd0d-110">傳遞品質控制訊息之篩選準則的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="0cd0d-111">*問*</span><span class="sxs-lookup"><span data-stu-id="0cd0d-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="0cd0d-112">包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cd0d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cd0d-113">Return value</span></span>

<span data-ttu-id="0cd0d-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0cd0d-115">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0cd0d-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0cd0d-116">Return code</span></span>                                                                                       | <span data-ttu-id="0cd0d-117">Description</span><span class="sxs-lookup"><span data-stu-id="0cd0d-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="0cd0d-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0cd0d-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="0cd0d-119">成功。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="0cd0d-120"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0cd0d-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="0cd0d-121">找不到接受訊息的物件。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cd0d-122">備註</span><span class="sxs-lookup"><span data-stu-id="0cd0d-122">Remarks</span></span>

<span data-ttu-id="0cd0d-123">這個方法會呼叫篩選準則的 [**CTransformFilter：： AlterQuality**](ctransformfilter-alterquality.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="0cd0d-124">如果篩選器不會處理品質訊息，這個方法會在篩選的輸入圖釘上呼叫 [**CBaseInputPin：:P assnotify**](cbaseinputpin-passnotify.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="0cd0d-125">**PassNotify** 方法會將高品質訊息傳遞給上游 (或自訂品質管制員（如果已安裝) ）。</span><span class="sxs-lookup"><span data-stu-id="0cd0d-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cd0d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cd0d-126">Requirements</span></span>



| <span data-ttu-id="0cd0d-127">需求</span><span class="sxs-lookup"><span data-stu-id="0cd0d-127">Requirement</span></span> | <span data-ttu-id="0cd0d-128">值</span><span class="sxs-lookup"><span data-stu-id="0cd0d-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd0d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0cd0d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0cd0d-130"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0cd0d-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0cd0d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="0cd0d-131">Library</span></span><br/> | <dl> <span data-ttu-id="0cd0d-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0cd0d-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




