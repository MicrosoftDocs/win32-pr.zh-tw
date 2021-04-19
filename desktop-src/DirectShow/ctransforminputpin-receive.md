---
description: Receive 方法會接收資料流程中的下一個媒體範例。 這個方法會實 IMemInputPin：： Receive 方法。
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: 'CTransformInputPin 的 Receive 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984458"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="597c8-104">CTransformInputPin 接收方法</span><span class="sxs-lookup"><span data-stu-id="597c8-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="597c8-105">`Receive`方法會接收資料流程中的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="597c8-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="597c8-106">這個方法會實 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。</span><span class="sxs-lookup"><span data-stu-id="597c8-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="597c8-107">語法</span><span class="sxs-lookup"><span data-stu-id="597c8-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="597c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="597c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="597c8-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="597c8-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="597c8-110">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="597c8-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="597c8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="597c8-111">Return value</span></span>

<span data-ttu-id="597c8-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="597c8-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="597c8-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="597c8-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="597c8-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="597c8-114">Return code</span></span>                                                                             | <span data-ttu-id="597c8-115">Description</span><span class="sxs-lookup"><span data-stu-id="597c8-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="597c8-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="597c8-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="597c8-117">Pin 目前正在排清;已拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="597c8-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="597c8-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="597c8-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="597c8-119">成功。</span><span class="sxs-lookup"><span data-stu-id="597c8-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="597c8-120">備註</span><span class="sxs-lookup"><span data-stu-id="597c8-120">Remarks</span></span>

<span data-ttu-id="597c8-121">這個方法會呼叫釘選的 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法，它會檢查 pin 的串流狀態，並檢查媒體類型中的格式變更。</span><span class="sxs-lookup"><span data-stu-id="597c8-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="597c8-122">然後，它會呼叫篩選器的 [**CTransformFilter：： Receive**](ctransformfilter-receive.md) 方法，該方法會處理範例並將它傳遞給下游。</span><span class="sxs-lookup"><span data-stu-id="597c8-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="597c8-123">如果此方法傳回之後，篩選準則需要存取範例，則應該在範例上呼叫 **IUnknown：： AddRef** 方法來保存參考計數。</span><span class="sxs-lookup"><span data-stu-id="597c8-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="597c8-124">例如，某些解碼器篩選器需要目前的範例，才能解碼下一個範例。</span><span class="sxs-lookup"><span data-stu-id="597c8-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="597c8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="597c8-125">Requirements</span></span>



| <span data-ttu-id="597c8-126">需求</span><span class="sxs-lookup"><span data-stu-id="597c8-126">Requirement</span></span> | <span data-ttu-id="597c8-127">值</span><span class="sxs-lookup"><span data-stu-id="597c8-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="597c8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="597c8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="597c8-129"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="597c8-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="597c8-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="597c8-130">Library</span></span><br/> | <dl> <span data-ttu-id="597c8-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="597c8-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




