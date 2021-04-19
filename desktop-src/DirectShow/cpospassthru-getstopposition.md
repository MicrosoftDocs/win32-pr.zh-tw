---
description: GetStopPosition 方法會捕獲播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaSeeking：： GetStopPosition 方法。
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: 'CPosPassThru. GetStopPosition 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999725"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="4fa45-104">CPosPassThru. GetStopPosition 方法</span><span class="sxs-lookup"><span data-stu-id="4fa45-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="4fa45-105">`GetStopPosition`方法會抓取播放將停止的時間，相對於資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="4fa45-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="4fa45-106">這個方法會實 [**IMediaSeeking：： GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="4fa45-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa45-107">語法</span><span class="sxs-lookup"><span data-stu-id="4fa45-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="4fa45-108">參數</span><span class="sxs-lookup"><span data-stu-id="4fa45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa45-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="4fa45-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa45-110">接收停止時間之變數的指標，以目前時間格式的單位為單位。</span><span class="sxs-lookup"><span data-stu-id="4fa45-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa45-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fa45-111">Return value</span></span>

<span data-ttu-id="4fa45-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4fa45-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa45-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fa45-113">Requirements</span></span>



| <span data-ttu-id="4fa45-114">需求</span><span class="sxs-lookup"><span data-stu-id="4fa45-114">Requirement</span></span> | <span data-ttu-id="4fa45-115">值</span><span class="sxs-lookup"><span data-stu-id="4fa45-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa45-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4fa45-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4fa45-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4fa45-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4fa45-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="4fa45-118">Library</span></span><br/> | <dl> <span data-ttu-id="4fa45-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4fa45-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa45-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fa45-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa45-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="4fa45-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




