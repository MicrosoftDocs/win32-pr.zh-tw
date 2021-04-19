---
description: Receive 方法會接收媒體範例、處理它，然後將它傳遞給下游篩選器。
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: 'CTransInPlaceFilter 的 Receive 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995407"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="2badd-103">CTransInPlaceFilter 接收方法</span><span class="sxs-lookup"><span data-stu-id="2badd-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="2badd-104">`Receive`方法會接收媒體範例、進行處理，並將其傳遞至下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="2badd-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2badd-105">語法</span><span class="sxs-lookup"><span data-stu-id="2badd-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="2badd-106">參數</span><span class="sxs-lookup"><span data-stu-id="2badd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2badd-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="2badd-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2badd-108">範例上 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2badd-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2badd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2badd-109">Return value</span></span>

<span data-ttu-id="2badd-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2badd-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2badd-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="2badd-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2badd-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2badd-112">Return code</span></span>                                                                                  | <span data-ttu-id="2badd-113">Description</span><span class="sxs-lookup"><span data-stu-id="2badd-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="2badd-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2badd-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2badd-115">Success</span><span class="sxs-lookup"><span data-stu-id="2badd-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="2badd-116"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="2badd-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="2badd-117">未預期的錯誤</span><span class="sxs-lookup"><span data-stu-id="2badd-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2badd-118">備註</span><span class="sxs-lookup"><span data-stu-id="2badd-118">Remarks</span></span>

<span data-ttu-id="2badd-119">篩選的輸入 pin 會在收到範例時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2badd-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="2badd-120">篩選準則會呼叫 [**轉換**](ctransinplacefilter-transform.md) 方法，而衍生類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="2badd-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="2badd-121">**轉換** 方法會處理資料。</span><span class="sxs-lookup"><span data-stu-id="2badd-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="2badd-122">如果篩選只使用一個配置器，它會將 *pSample* 直接傳遞至 **轉換** 方法。</span><span class="sxs-lookup"><span data-stu-id="2badd-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="2badd-123">否則，它會複製 *pSample* 並傳遞複本。</span><span class="sxs-lookup"><span data-stu-id="2badd-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="2badd-124">如果 **轉換** 方法傳回 \_ FALSE，則方法會卸載 `Receive` 範例。</span><span class="sxs-lookup"><span data-stu-id="2badd-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="2badd-125">在第一個捨棄的範例中，篩選準則會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="2badd-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="2badd-126">否則，如果 **轉換** 方法傳回 S \_ OK，則篩選會傳遞輸出範例。</span><span class="sxs-lookup"><span data-stu-id="2badd-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="2badd-127">若要這樣做，它會對下游輸入 pin 呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。</span><span class="sxs-lookup"><span data-stu-id="2badd-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2badd-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2badd-128">Requirements</span></span>



| <span data-ttu-id="2badd-129">需求</span><span class="sxs-lookup"><span data-stu-id="2badd-129">Requirement</span></span> | <span data-ttu-id="2badd-130">值</span><span class="sxs-lookup"><span data-stu-id="2badd-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2badd-131">標頭</span><span class="sxs-lookup"><span data-stu-id="2badd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2badd-132"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2badd-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2badd-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="2badd-133">Library</span></span><br/> | <dl> <span data-ttu-id="2badd-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2badd-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2badd-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2badd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2badd-136">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="2badd-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




