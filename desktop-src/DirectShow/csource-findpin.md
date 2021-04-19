---
description: FindPin 方法會使用指定的識別碼抓取 pin。 這個方法會實 IBaseFilter：： FindPin 方法。
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: 'CSource. FindPin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998376"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="a26ae-104">CSource. FindPin 方法</span><span class="sxs-lookup"><span data-stu-id="a26ae-104">CSource.FindPin method</span></span>

<span data-ttu-id="a26ae-105">`FindPin`方法會使用指定的識別碼抓取 pin。</span><span class="sxs-lookup"><span data-stu-id="a26ae-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="a26ae-106">這個方法會實 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) 方法。</span><span class="sxs-lookup"><span data-stu-id="a26ae-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a26ae-107">語法</span><span class="sxs-lookup"><span data-stu-id="a26ae-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="a26ae-108">參數</span><span class="sxs-lookup"><span data-stu-id="a26ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a26ae-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="a26ae-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="a26ae-110">識別 pin 之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="a26ae-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="a26ae-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="a26ae-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a26ae-112">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a26ae-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="a26ae-113">如果方法失敗， \* *ppPin* 會設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a26ae-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a26ae-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a26ae-114">Return value</span></span>

<span data-ttu-id="a26ae-115">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a26ae-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a26ae-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a26ae-116">Return code</span></span>                                                                                       | <span data-ttu-id="a26ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="a26ae-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="a26ae-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a26ae-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a26ae-119">成功。</span><span class="sxs-lookup"><span data-stu-id="a26ae-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a26ae-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="a26ae-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="a26ae-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="a26ae-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="a26ae-122"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a26ae-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a26ae-123">找不到具有此識別碼的 pin。</span><span class="sxs-lookup"><span data-stu-id="a26ae-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a26ae-124">備註</span><span class="sxs-lookup"><span data-stu-id="a26ae-124">Remarks</span></span>

<span data-ttu-id="a26ae-125">第一個 pin 一律名為 "1";第二個 pin 名為 "2";等等。</span><span class="sxs-lookup"><span data-stu-id="a26ae-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="a26ae-126">如需詳細資訊，請參閱 [**CSourceStream：： QueryId**](csourcestream-queryid.md)。</span><span class="sxs-lookup"><span data-stu-id="a26ae-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a26ae-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a26ae-127">Requirements</span></span>



| <span data-ttu-id="a26ae-128">需求</span><span class="sxs-lookup"><span data-stu-id="a26ae-128">Requirement</span></span> | <span data-ttu-id="a26ae-129">值</span><span class="sxs-lookup"><span data-stu-id="a26ae-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a26ae-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a26ae-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a26ae-131"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="a26ae-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a26ae-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="a26ae-132">Library</span></span><br/> | <dl> <span data-ttu-id="a26ae-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a26ae-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a26ae-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a26ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26ae-135">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="a26ae-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




