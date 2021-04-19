---
description: 通知方法會收到要求品質變更的通知。
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: 'CBaseVideoRenderer： Notify 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995253"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="55a31-103">CBaseVideoRenderer。通知方法</span><span class="sxs-lookup"><span data-stu-id="55a31-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="55a31-104">`Notify`方法會收到要求品質變更的通知。</span><span class="sxs-lookup"><span data-stu-id="55a31-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a31-105">語法</span><span class="sxs-lookup"><span data-stu-id="55a31-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="55a31-106">參數</span><span class="sxs-lookup"><span data-stu-id="55a31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a31-107">*pSelf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55a31-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a31-108">傳送品質通知的篩選準則指標。</span><span class="sxs-lookup"><span data-stu-id="55a31-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="55a31-109">*q* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55a31-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55a31-110">品質通知結構。</span><span class="sxs-lookup"><span data-stu-id="55a31-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a31-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="55a31-111">Return value</span></span>

<span data-ttu-id="55a31-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="55a31-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a31-113">備註</span><span class="sxs-lookup"><span data-stu-id="55a31-113">Remarks</span></span>

<span data-ttu-id="55a31-114">此成員函式會在影片轉譯器上 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。</span><span class="sxs-lookup"><span data-stu-id="55a31-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="55a31-115">當品質必須剪下時，通常會由篩選圖形管理員呼叫這項功能。</span><span class="sxs-lookup"><span data-stu-id="55a31-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="55a31-116">當音訊播放品質已增加到必須降低影片播放品質的點時，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="55a31-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="55a31-117">`Notify` 將 **m \_ trThrottle** 資料成員設定為要依 [**ThrottleWait**](cbasevideorenderer-throttlewait.md)在框架之間插入的延遲值。</span><span class="sxs-lookup"><span data-stu-id="55a31-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55a31-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="55a31-118">Requirements</span></span>



| <span data-ttu-id="55a31-119">需求</span><span class="sxs-lookup"><span data-stu-id="55a31-119">Requirement</span></span> | <span data-ttu-id="55a31-120">值</span><span class="sxs-lookup"><span data-stu-id="55a31-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a31-121">標頭</span><span class="sxs-lookup"><span data-stu-id="55a31-121">Header</span></span><br/>  | <dl> <span data-ttu-id="55a31-122"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55a31-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55a31-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="55a31-123">Library</span></span><br/> | <dl> <span data-ttu-id="55a31-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="55a31-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a31-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55a31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a31-126">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="55a31-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




