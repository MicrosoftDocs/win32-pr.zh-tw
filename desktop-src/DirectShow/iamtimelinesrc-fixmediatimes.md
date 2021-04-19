---
description: FixMediaTimes 方法會將指定的時間值四捨五入到最接近的框架界限（如輸出畫面播放速率所定義）。 一般情況下，應用程式不需要呼叫此方法。
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'IAMTimelineSrc：： FixMediaTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999081"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="1c854-104">IAMTimelineSrc：： FixMediaTimes 方法</span><span class="sxs-lookup"><span data-stu-id="1c854-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="1c854-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1c854-105">\[Deprecated.</span></span> <span data-ttu-id="1c854-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1c854-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1c854-107">方法會將 `FixMediaTimes` 指定的時間值四捨五入到最接近的框架界限（如輸出畫面播放速率所定義）。</span><span class="sxs-lookup"><span data-stu-id="1c854-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="1c854-108">一般情況下，應用程式不需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="1c854-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c854-109">語法</span><span class="sxs-lookup"><span data-stu-id="1c854-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="1c854-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c854-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c854-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="1c854-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="1c854-112">變數的指標，該變數包含開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="1c854-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="1c854-113">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="1c854-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="1c854-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="1c854-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="1c854-115">包含停止時間之變數的指標，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="1c854-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="1c854-116">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="1c854-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c854-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c854-117">Return value</span></span>

<span data-ttu-id="1c854-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1c854-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c854-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1c854-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c854-120">備註</span><span class="sxs-lookup"><span data-stu-id="1c854-120">Remarks</span></span>

<span data-ttu-id="1c854-121">這個方法類似于 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md) 方法，但會保留媒體時間與時間軸時間的原始比例。</span><span class="sxs-lookup"><span data-stu-id="1c854-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="1c854-122">只將時間四捨五入到最接近的框架界限可能會扭曲此比例。</span><span class="sxs-lookup"><span data-stu-id="1c854-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="1c854-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="1c854-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1c854-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1c854-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1c854-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="1c854-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c854-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c854-126">Requirements</span></span>



| <span data-ttu-id="1c854-127">需求</span><span class="sxs-lookup"><span data-stu-id="1c854-127">Requirement</span></span> | <span data-ttu-id="1c854-128">值</span><span class="sxs-lookup"><span data-stu-id="1c854-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c854-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1c854-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1c854-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c854-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1c854-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c854-131">Library</span></span><br/> | <dl> <span data-ttu-id="1c854-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c854-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c854-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c854-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c854-134">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="1c854-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="1c854-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="1c854-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




