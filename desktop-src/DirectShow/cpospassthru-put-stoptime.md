---
description: Put \_ StopTime 方法會設定播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaPosition：:p 的 \_ StopTime 方法。
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: 'CPosPassThru.put_StopTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999396"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="3be07-104">CPosPassThru. put \_ StopTime 方法</span><span class="sxs-lookup"><span data-stu-id="3be07-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="3be07-105">`put_StopTime`方法會設定播放將停止的時間（相對於資料流程的持續時間）。</span><span class="sxs-lookup"><span data-stu-id="3be07-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="3be07-106">這個方法會實 [**IMediaPosition：:p 的 \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) 方法。</span><span class="sxs-lookup"><span data-stu-id="3be07-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be07-107">語法</span><span class="sxs-lookup"><span data-stu-id="3be07-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="3be07-108">參數</span><span class="sxs-lookup"><span data-stu-id="3be07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be07-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="3be07-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3be07-110">以 **秒為單位的停止** 時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3be07-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3be07-111">Return value</span></span>

<span data-ttu-id="3be07-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3be07-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3be07-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3be07-113">Requirements</span></span>



| <span data-ttu-id="3be07-114">需求</span><span class="sxs-lookup"><span data-stu-id="3be07-114">Requirement</span></span> | <span data-ttu-id="3be07-115">值</span><span class="sxs-lookup"><span data-stu-id="3be07-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be07-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3be07-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3be07-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3be07-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3be07-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3be07-118">Library</span></span><br/> | <dl> <span data-ttu-id="3be07-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3be07-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be07-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3be07-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be07-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="3be07-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




