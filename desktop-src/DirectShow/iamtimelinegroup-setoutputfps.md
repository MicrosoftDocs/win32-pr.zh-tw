---
description: SetOutputFPS 方法會設定此群組的未壓縮輸出畫面播放速率。
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'IAMTimelineGroup：： SetOutputFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996445"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="e9b4e-103">IAMTimelineGroup：： SetOutputFPS 方法</span><span class="sxs-lookup"><span data-stu-id="e9b4e-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="e9b4e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-104">\[Deprecated.</span></span> <span data-ttu-id="e9b4e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e9b4e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e9b4e-106">`SetOutputFPS`方法會為此群組設定未壓縮的輸出畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b4e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e9b4e-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="e9b4e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e9b4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b4e-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="e9b4e-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b4e-110">此群組的輸出畫面播放速率（以每秒畫面數為單位）。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="e9b4e-111">此值不能等於零，而且小數點之後不可超過七位數。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b4e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9b4e-112">Return value</span></span>

<span data-ttu-id="e9b4e-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9b4e-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b4e-115">備註</span><span class="sxs-lookup"><span data-stu-id="e9b4e-115">Remarks</span></span>

<span data-ttu-id="e9b4e-116">從此群組轉譯的輸出會以指定的畫面播放速率執行，而對來源資料所做的所有編輯則會四捨五入至最接近的框架界限（依畫面播放速率所定義）。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="e9b4e-117">為了達到最佳效能，所有群組、影片和音訊都使用相同的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="e9b4e-118">[**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)方法會覆寫畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="e9b4e-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9b4e-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e9b4e-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9b4e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9b4e-122">Requirements</span></span>



| <span data-ttu-id="e9b4e-123">需求</span><span class="sxs-lookup"><span data-stu-id="e9b4e-123">Requirement</span></span> | <span data-ttu-id="e9b4e-124">值</span><span class="sxs-lookup"><span data-stu-id="e9b4e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b4e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e9b4e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9b4e-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9b4e-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e9b4e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9b4e-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9b4e-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9b4e-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b4e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9b4e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b4e-130">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="e9b4e-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="e9b4e-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




