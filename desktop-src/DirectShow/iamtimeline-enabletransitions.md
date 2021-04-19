---
description: EnableTransitions 方法會啟用或停用時間軸中的所有轉換。
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'IAMTimeline：： EnableTransitions 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987064"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="deb17-103">IAMTimeline：： EnableTransitions 方法</span><span class="sxs-lookup"><span data-stu-id="deb17-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="deb17-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="deb17-104">\[Deprecated.</span></span> <span data-ttu-id="deb17-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="deb17-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="deb17-106">`EnableTransitions`方法會啟用或停用時間軸中的所有轉換。</span><span class="sxs-lookup"><span data-stu-id="deb17-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="deb17-107">如果轉換已停用，則轉譯引擎會將它們視為剪下;也就是說，轉譯的輸出會立即從一個播放軌跳到下一個曲目。</span><span class="sxs-lookup"><span data-stu-id="deb17-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="deb17-108">預設的剪點是過渡期間的一半。</span><span class="sxs-lookup"><span data-stu-id="deb17-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="deb17-109">您可以在轉換上呼叫 [**IAMTimelineTrans：： SetCutPoint**](iamtimelinetrans-setcutpoint.md) 方法來變更剪下點。</span><span class="sxs-lookup"><span data-stu-id="deb17-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="deb17-110">停用的轉換不會從時間軸中移除。</span><span class="sxs-lookup"><span data-stu-id="deb17-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb17-111">語法</span><span class="sxs-lookup"><span data-stu-id="deb17-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="deb17-112">參數</span><span class="sxs-lookup"><span data-stu-id="deb17-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb17-113">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="deb17-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="deb17-114">指定是否要啟用或停用轉換的布林值。</span><span class="sxs-lookup"><span data-stu-id="deb17-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="deb17-115">若 **為 TRUE**，則會啟用轉換。</span><span class="sxs-lookup"><span data-stu-id="deb17-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="deb17-116">如果 **為 FALSE**，則會停用轉換。</span><span class="sxs-lookup"><span data-stu-id="deb17-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb17-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="deb17-117">Return value</span></span>

<span data-ttu-id="deb17-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="deb17-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="deb17-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="deb17-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="deb17-120">備註</span><span class="sxs-lookup"><span data-stu-id="deb17-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="deb17-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="deb17-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="deb17-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="deb17-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="deb17-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="deb17-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="deb17-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="deb17-124">Requirements</span></span>



| <span data-ttu-id="deb17-125">需求</span><span class="sxs-lookup"><span data-stu-id="deb17-125">Requirement</span></span> | <span data-ttu-id="deb17-126">值</span><span class="sxs-lookup"><span data-stu-id="deb17-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deb17-127">標頭</span><span class="sxs-lookup"><span data-stu-id="deb17-127">Header</span></span><br/>  | <dl> <span data-ttu-id="deb17-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="deb17-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="deb17-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="deb17-129">Library</span></span><br/> | <dl> <span data-ttu-id="deb17-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb17-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deb17-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deb17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb17-132">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="deb17-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="deb17-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="deb17-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




