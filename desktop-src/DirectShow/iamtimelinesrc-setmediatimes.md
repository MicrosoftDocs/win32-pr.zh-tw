---
description: SetMediaTimes 方法會設定媒體停止和開始時間。
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'IAMTimelineSrc：： SetMediaTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996398"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="da627-103">IAMTimelineSrc：： SetMediaTimes 方法</span><span class="sxs-lookup"><span data-stu-id="da627-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="da627-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="da627-104">\[Deprecated.</span></span> <span data-ttu-id="da627-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="da627-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da627-106">`SetMediaTimes`方法會設定媒體停止和開始時間。</span><span class="sxs-lookup"><span data-stu-id="da627-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="da627-107">語法</span><span class="sxs-lookup"><span data-stu-id="da627-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="da627-108">參數</span><span class="sxs-lookup"><span data-stu-id="da627-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da627-109">*開始*</span><span class="sxs-lookup"><span data-stu-id="da627-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="da627-110">媒體開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="da627-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="da627-111">*停止*</span><span class="sxs-lookup"><span data-stu-id="da627-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="da627-112">媒體停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="da627-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da627-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da627-113">Return value</span></span>

<span data-ttu-id="da627-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="da627-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da627-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da627-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da627-116">備註</span><span class="sxs-lookup"><span data-stu-id="da627-116">Remarks</span></span>

<span data-ttu-id="da627-117">媒體時間是相對於原始媒體檔案的停止和開始時間。</span><span class="sxs-lookup"><span data-stu-id="da627-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="da627-118">當您將影片或音訊來源新增至時間軸時，一律設定媒體時間。</span><span class="sxs-lookup"><span data-stu-id="da627-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="da627-119">否則，可能會發生轉譯問題。</span><span class="sxs-lookup"><span data-stu-id="da627-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="da627-120">停止時間必須大於開始時間。</span><span class="sxs-lookup"><span data-stu-id="da627-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="da627-121">若要從影片來源使用仍然的框架，請將停止時間設定為比開始時間更多的小數數量，例如100毫微秒。</span><span class="sxs-lookup"><span data-stu-id="da627-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="da627-122">將其設定為相同的值會導致轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="da627-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="da627-123">如果時間軸的持續時間不符合媒體持續時間，則來源會據以伸展或縮小。</span><span class="sxs-lookup"><span data-stu-id="da627-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="da627-124">這會使剪輯的播放速度比撰寫的速率慢或更快。</span><span class="sxs-lookup"><span data-stu-id="da627-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="da627-125"> (音調變化會在音訊來源中發生 ) 。如需詳細資訊，請參閱 [DirectShow 編輯服務的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="da627-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="da627-126">您可以藉由呼叫 [**SetMediaLength**](iamtimelinesrc-setmedialength.md) 方法來指定原始程式檔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="da627-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="da627-127">如果您設定超過持續時間的媒體停止時間，DES 會截斷停止時間。</span><span class="sxs-lookup"><span data-stu-id="da627-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="da627-128">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="da627-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="da627-129">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="da627-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="da627-130">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="da627-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da627-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="da627-131">Requirements</span></span>



| <span data-ttu-id="da627-132">需求</span><span class="sxs-lookup"><span data-stu-id="da627-132">Requirement</span></span> | <span data-ttu-id="da627-133">值</span><span class="sxs-lookup"><span data-stu-id="da627-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da627-134">標頭</span><span class="sxs-lookup"><span data-stu-id="da627-134">Header</span></span><br/>  | <dl> <span data-ttu-id="da627-135"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="da627-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="da627-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="da627-136">Library</span></span><br/> | <dl> <span data-ttu-id="da627-137"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da627-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da627-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da627-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da627-139">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="da627-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="da627-140">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="da627-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




