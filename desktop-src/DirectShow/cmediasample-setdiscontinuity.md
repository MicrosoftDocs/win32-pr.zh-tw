---
description: SetDiscontinuity 方法會指定此範例是否表示資料流程中的中斷。 這個方法會實 IMediaSample：： SetDiscontinuity 方法。
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: 'CMediaSample. SetDiscontinuity 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982936"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="681fb-104">CMediaSample. SetDiscontinuity 方法</span><span class="sxs-lookup"><span data-stu-id="681fb-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="681fb-105">`SetDiscontinuity`方法會指定此範例是否表示資料流程中的中斷。</span><span class="sxs-lookup"><span data-stu-id="681fb-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="681fb-106">這個方法會實 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法。</span><span class="sxs-lookup"><span data-stu-id="681fb-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="681fb-107">語法</span><span class="sxs-lookup"><span data-stu-id="681fb-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="681fb-108">參數</span><span class="sxs-lookup"><span data-stu-id="681fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681fb-109">*bDiscont*</span><span class="sxs-lookup"><span data-stu-id="681fb-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="681fb-110">指定此範例是否為不中斷的布林值。</span><span class="sxs-lookup"><span data-stu-id="681fb-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="681fb-111">若 **為 TRUE**，則表示媒體範例與上一個範例不連續。</span><span class="sxs-lookup"><span data-stu-id="681fb-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="681fb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="681fb-112">Return value</span></span>

<span data-ttu-id="681fb-113">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="681fb-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="681fb-114">備註</span><span class="sxs-lookup"><span data-stu-id="681fb-114">Remarks</span></span>

<span data-ttu-id="681fb-115">這個方法會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定不中斷屬性。</span><span class="sxs-lookup"><span data-stu-id="681fb-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="681fb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="681fb-116">Requirements</span></span>



| <span data-ttu-id="681fb-117">需求</span><span class="sxs-lookup"><span data-stu-id="681fb-117">Requirement</span></span> | <span data-ttu-id="681fb-118">值</span><span class="sxs-lookup"><span data-stu-id="681fb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="681fb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="681fb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="681fb-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="681fb-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="681fb-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="681fb-121">Library</span></span><br/> | <dl> <span data-ttu-id="681fb-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="681fb-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="681fb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="681fb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681fb-124">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="681fb-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




