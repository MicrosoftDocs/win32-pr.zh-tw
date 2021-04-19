---
description: GetPreviewMode 方法會抓取群組的預覽模式。
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'IAMTimelineGroup：： GetPreviewMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991254"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a><span data-ttu-id="92cca-103">IAMTimelineGroup：： GetPreviewMode 方法</span><span class="sxs-lookup"><span data-stu-id="92cca-103">IAMTimelineGroup::GetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="92cca-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="92cca-104">\[Deprecated.</span></span> <span data-ttu-id="92cca-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="92cca-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="92cca-106">方法會抓取 `GetPreviewMode` 群組的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="92cca-106">The `GetPreviewMode` method retrieves the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="92cca-107">語法</span><span class="sxs-lookup"><span data-stu-id="92cca-107">Syntax</span></span>


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a><span data-ttu-id="92cca-108">參數</span><span class="sxs-lookup"><span data-stu-id="92cca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92cca-109">*pfPreview*</span><span class="sxs-lookup"><span data-stu-id="92cca-109">*pfPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="92cca-110">接收指出預覽模式的布林值。</span><span class="sxs-lookup"><span data-stu-id="92cca-110">Receives a Boolean value indicating the preview mode.</span></span> <span data-ttu-id="92cca-111">若 **為 TRUE**，則群組處於預覽模式。</span><span class="sxs-lookup"><span data-stu-id="92cca-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="92cca-112">如果 **為 FALSE**，則表示群組處於撰寫模式。</span><span class="sxs-lookup"><span data-stu-id="92cca-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92cca-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="92cca-113">Return value</span></span>

<span data-ttu-id="92cca-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="92cca-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92cca-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92cca-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92cca-116">備註</span><span class="sxs-lookup"><span data-stu-id="92cca-116">Remarks</span></span>

<span data-ttu-id="92cca-117">在預覽模式中，會在慢速效果或轉換期間卸載框架，讓影片與音訊保持同步。</span><span class="sxs-lookup"><span data-stu-id="92cca-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="92cca-118">這樣的影片看起來可能不穩定。</span><span class="sxs-lookup"><span data-stu-id="92cca-118">The video might look choppy as a result.</span></span> <span data-ttu-id="92cca-119">在 [撰寫中] 模式中，每個畫面格都會呈現。</span><span class="sxs-lookup"><span data-stu-id="92cca-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="92cca-120">撰寫模式適合用來寫入檔案;在螢幕上預覽時，影片可能會與音訊不同步。</span><span class="sxs-lookup"><span data-stu-id="92cca-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might become out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="92cca-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="92cca-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="92cca-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="92cca-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="92cca-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="92cca-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92cca-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="92cca-124">Requirements</span></span>



| <span data-ttu-id="92cca-125">需求</span><span class="sxs-lookup"><span data-stu-id="92cca-125">Requirement</span></span> | <span data-ttu-id="92cca-126">值</span><span class="sxs-lookup"><span data-stu-id="92cca-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92cca-127">標頭</span><span class="sxs-lookup"><span data-stu-id="92cca-127">Header</span></span><br/>  | <dl> <span data-ttu-id="92cca-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="92cca-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="92cca-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="92cca-129">Library</span></span><br/> | <dl> <span data-ttu-id="92cca-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="92cca-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92cca-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92cca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92cca-132">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="92cca-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="92cca-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="92cca-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




