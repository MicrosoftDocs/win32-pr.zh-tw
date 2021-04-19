---
description: SetSyncPoint 方法會指定此範例的開頭是否為同步處理點。 這個方法會實 IMediaSample：： SetSyncPoint 方法。
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: 'CMediaSample. SetSyncPoint 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991538"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="b8d32-104">CMediaSample. SetSyncPoint 方法</span><span class="sxs-lookup"><span data-stu-id="b8d32-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="b8d32-105">`SetSyncPoint`方法會指定此範例的開頭是否為同步處理點。</span><span class="sxs-lookup"><span data-stu-id="b8d32-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="b8d32-106">這個方法會實 [**IMediaSample：： SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) 方法。</span><span class="sxs-lookup"><span data-stu-id="b8d32-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d32-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8d32-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="b8d32-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8d32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d32-109">*bIsSyncPoint*</span><span class="sxs-lookup"><span data-stu-id="b8d32-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d32-110">指定這是否為同步處理點的布林值。</span><span class="sxs-lookup"><span data-stu-id="b8d32-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="b8d32-111">若 **為 TRUE**，表示這是同步處理點。</span><span class="sxs-lookup"><span data-stu-id="b8d32-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d32-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8d32-112">Return value</span></span>

<span data-ttu-id="b8d32-113">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b8d32-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d32-114">備註</span><span class="sxs-lookup"><span data-stu-id="b8d32-114">Remarks</span></span>

<span data-ttu-id="b8d32-115">這個方法會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定同步處理點屬性。</span><span class="sxs-lookup"><span data-stu-id="b8d32-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d32-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8d32-116">Requirements</span></span>



| <span data-ttu-id="b8d32-117">需求</span><span class="sxs-lookup"><span data-stu-id="b8d32-117">Requirement</span></span> | <span data-ttu-id="b8d32-118">值</span><span class="sxs-lookup"><span data-stu-id="b8d32-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d32-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b8d32-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d32-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b8d32-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b8d32-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8d32-121">Library</span></span><br/> | <dl> <span data-ttu-id="b8d32-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b8d32-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d32-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8d32-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d32-124">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="b8d32-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




