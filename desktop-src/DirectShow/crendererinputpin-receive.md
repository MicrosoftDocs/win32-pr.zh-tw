---
description: Receive 方法會接收資料流程中的下一個媒體範例。 這個方法會覆寫 CBaseInputPin：： Receive 方法。
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: 'CRendererInputPin 的 Receive 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993661"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="0eac9-104">CRendererInputPin 接收方法</span><span class="sxs-lookup"><span data-stu-id="0eac9-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="0eac9-105">`Receive`方法會接收資料流程中的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="0eac9-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="0eac9-106">這個方法會覆寫 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0eac9-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eac9-107">語法</span><span class="sxs-lookup"><span data-stu-id="0eac9-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="0eac9-108">參數</span><span class="sxs-lookup"><span data-stu-id="0eac9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eac9-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="0eac9-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0eac9-110">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0eac9-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eac9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0eac9-111">Return value</span></span>

<span data-ttu-id="0eac9-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0eac9-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eac9-113">備註</span><span class="sxs-lookup"><span data-stu-id="0eac9-113">Remarks</span></span>

<span data-ttu-id="0eac9-114">這個方法會呼叫篩選器的 [**CBaseRenderer：： Receive**](cbaserenderer-receive.md) 方法，它會處理呈現。</span><span class="sxs-lookup"><span data-stu-id="0eac9-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="0eac9-115">如果該方法失敗，則 pin 會傳送 EC \_ ERRORABORT 事件。</span><span class="sxs-lookup"><span data-stu-id="0eac9-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eac9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0eac9-116">Requirements</span></span>



| <span data-ttu-id="0eac9-117">需求</span><span class="sxs-lookup"><span data-stu-id="0eac9-117">Requirement</span></span> | <span data-ttu-id="0eac9-118">值</span><span class="sxs-lookup"><span data-stu-id="0eac9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eac9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0eac9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0eac9-120"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0eac9-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0eac9-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="0eac9-121">Library</span></span><br/> | <dl> <span data-ttu-id="0eac9-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0eac9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eac9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0eac9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eac9-124">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="0eac9-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




