---
description: 當物件從輸出圖釘接收媒體範例時，會呼叫接收方法。 衍生的類別必須執行此方法。
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: 'CPullPin 的 Receive 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994814"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="d7ad5-104">CPullPin 接收方法</span><span class="sxs-lookup"><span data-stu-id="d7ad5-104">CPullPin.Receive method</span></span>

<span data-ttu-id="d7ad5-105">`Receive`當物件從輸出圖釘接收媒體範例時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="d7ad5-106">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ad5-107">語法</span><span class="sxs-lookup"><span data-stu-id="d7ad5-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d7ad5-108">參數</span><span class="sxs-lookup"><span data-stu-id="d7ad5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ad5-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="d7ad5-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ad5-110">媒體範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ad5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7ad5-111">Return value</span></span>

<span data-ttu-id="d7ad5-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d7ad5-113">傳回 S 以外的值 \_ 將會停止資料提取執行緒。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ad5-114">備註</span><span class="sxs-lookup"><span data-stu-id="d7ad5-114">Remarks</span></span>

<span data-ttu-id="d7ad5-115">每當有新的範例從輸出圖釘抵達時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="d7ad5-116">以與 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法相同的方式來撰寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="d7ad5-117">範例上的時間戳記會指定位元組位移，相對於 [**CPullPin：： Seek**](cpullpin-seek.md) 方法中指定的原始開始位置。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="d7ad5-118">開始位置會向下舍入至最接近的對齊界限，而停止位置會進位到最接近的對齊界限。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="d7ad5-119">此外，如果停止位置超過總持續時間，則會改用持續時間。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="d7ad5-120">所有時間戳記都會以位元組位移乘以10000000（定義為常數單位）來提供。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="d7ad5-121">因此，notionally 一秒是1個位元組。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="d7ad5-122">若要尋找實際的位元組位移，請呼叫 [**IMediaSample：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) ，並依單位除以結果。</span><span class="sxs-lookup"><span data-stu-id="d7ad5-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ad5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7ad5-123">Requirements</span></span>



| <span data-ttu-id="d7ad5-124">需求</span><span class="sxs-lookup"><span data-stu-id="d7ad5-124">Requirement</span></span> | <span data-ttu-id="d7ad5-125">值</span><span class="sxs-lookup"><span data-stu-id="d7ad5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ad5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d7ad5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d7ad5-127"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ad5-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="d7ad5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7ad5-128">Library</span></span><br/> | <dl> <span data-ttu-id="d7ad5-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d7ad5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ad5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7ad5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ad5-131">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="d7ad5-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




