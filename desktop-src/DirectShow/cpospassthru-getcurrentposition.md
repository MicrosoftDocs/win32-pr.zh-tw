---
description: GetCurrentPosition 方法會抓取目前的位置，相對於資料流程的總持續時間。 這個方法會實 IMediaSeeking：： GetCurrentPosition 方法。
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: 'CPosPassThru. GetCurrentPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994754"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="6a787-104">CPosPassThru. GetCurrentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="6a787-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="6a787-105">方法會抓取 `GetCurrentPosition` 目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="6a787-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="6a787-106">這個方法會實 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="6a787-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a787-107">語法</span><span class="sxs-lookup"><span data-stu-id="6a787-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="6a787-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a787-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a787-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="6a787-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="6a787-110">變數的指標，此變數會接收目前的位置，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="6a787-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a787-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a787-111">Return value</span></span>

<span data-ttu-id="6a787-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6a787-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6a787-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="6a787-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6a787-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a787-114">Return code</span></span>                                                                               | <span data-ttu-id="6a787-115">Description</span><span class="sxs-lookup"><span data-stu-id="6a787-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6a787-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a787-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="6a787-117">成功。</span><span class="sxs-lookup"><span data-stu-id="6a787-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6a787-118"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6a787-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="6a787-119">不支援方法。</span><span class="sxs-lookup"><span data-stu-id="6a787-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="6a787-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6a787-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="6a787-121">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="6a787-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a787-122">備註</span><span class="sxs-lookup"><span data-stu-id="6a787-122">Remarks</span></span>

<span data-ttu-id="6a787-123">這個方法會呼叫 [**CPosPassThru：： GetMediaTime**](cpospassthru-getmediatime.md) 方法，以取得最新的位置。</span><span class="sxs-lookup"><span data-stu-id="6a787-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="6a787-124">如果 **GetMediaTime** 失敗，此方法會在連線的 pin 上呼叫 **IMediaSeeking：： GetCurrentPosition** 。</span><span class="sxs-lookup"><span data-stu-id="6a787-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="6a787-125">根據預設， **GetMediaTime** 方法會在基類中失敗。</span><span class="sxs-lookup"><span data-stu-id="6a787-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="6a787-126">如果您的篩選準則快取目前的位置，請覆寫 **GetMediaTime** 以傳回快取的值。</span><span class="sxs-lookup"><span data-stu-id="6a787-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a787-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a787-127">Requirements</span></span>



| <span data-ttu-id="6a787-128">需求</span><span class="sxs-lookup"><span data-stu-id="6a787-128">Requirement</span></span> | <span data-ttu-id="6a787-129">值</span><span class="sxs-lookup"><span data-stu-id="6a787-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a787-130">標頭</span><span class="sxs-lookup"><span data-stu-id="6a787-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6a787-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6a787-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6a787-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a787-132">Library</span></span><br/> | <dl> <span data-ttu-id="6a787-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6a787-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a787-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a787-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a787-135">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="6a787-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




