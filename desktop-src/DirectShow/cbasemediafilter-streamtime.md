---
description: StreamTime 方法會抓取目前的資料流程時間。
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: 'CBaseMediaFilter. StreamTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983962"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="eddd5-103">CBaseMediaFilter. StreamTime 方法</span><span class="sxs-lookup"><span data-stu-id="eddd5-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="eddd5-104">`StreamTime`方法會捕獲目前的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="eddd5-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="eddd5-105">語法</span><span class="sxs-lookup"><span data-stu-id="eddd5-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="eddd5-106">參數</span><span class="sxs-lookup"><span data-stu-id="eddd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eddd5-107">*rtStream* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="eddd5-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="eddd5-108">[**CRefTime**](creftime.md)物件的參考，該物件會接收目前的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="eddd5-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eddd5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eddd5-109">Return value</span></span>

<span data-ttu-id="eddd5-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="eddd5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eddd5-111">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="eddd5-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="eddd5-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eddd5-112">Return code</span></span>                                                                                      | <span data-ttu-id="eddd5-113">Description</span><span class="sxs-lookup"><span data-stu-id="eddd5-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="eddd5-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eddd5-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="eddd5-115">成功。</span><span class="sxs-lookup"><span data-stu-id="eddd5-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="eddd5-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="eddd5-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="eddd5-117">沒有可用的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="eddd5-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eddd5-118">備註</span><span class="sxs-lookup"><span data-stu-id="eddd5-118">Remarks</span></span>

<span data-ttu-id="eddd5-119">資料流程時間定義為目前的參考時間 (如參考時鐘所指定) 減去 [**CBaseMediaFilter：： m \_ tStart**](cbasemediafilter-m-tstart.md)) 所指定的開始時間 (。</span><span class="sxs-lookup"><span data-stu-id="eddd5-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="eddd5-120">媒體範例的時間戳記會指定應呈現的資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="eddd5-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="eddd5-121">如果時間戳記小於目前資料流程時間的樣本尚未轉譯，則會延遲。</span><span class="sxs-lookup"><span data-stu-id="eddd5-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="eddd5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="eddd5-122">Requirements</span></span>



| <span data-ttu-id="eddd5-123">需求</span><span class="sxs-lookup"><span data-stu-id="eddd5-123">Requirement</span></span> | <span data-ttu-id="eddd5-124">值</span><span class="sxs-lookup"><span data-stu-id="eddd5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eddd5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="eddd5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eddd5-126"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eddd5-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eddd5-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="eddd5-127">Library</span></span><br/> | <dl> <span data-ttu-id="eddd5-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eddd5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eddd5-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eddd5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddd5-130">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="eddd5-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




