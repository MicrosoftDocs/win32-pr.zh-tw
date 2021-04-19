---
description: SetMuted 方法會設定物件的已靜音狀態。 靜音物件不會呈現，但會保留在時間軸中。
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'IAMTimelineObj：： SetMuted 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993210"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="45a5e-104">IAMTimelineObj：： SetMuted 方法</span><span class="sxs-lookup"><span data-stu-id="45a5e-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="45a5e-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="45a5e-105">\[Deprecated.</span></span> <span data-ttu-id="45a5e-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="45a5e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="45a5e-107">`SetMuted`方法會設定物件的已靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="45a5e-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="45a5e-108">靜音物件不會呈現，但會保留在時間軸中。</span><span class="sxs-lookup"><span data-stu-id="45a5e-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a5e-109">語法</span><span class="sxs-lookup"><span data-stu-id="45a5e-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="45a5e-110">參數</span><span class="sxs-lookup"><span data-stu-id="45a5e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45a5e-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="45a5e-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="45a5e-112">指定靜音狀態的旗標。</span><span class="sxs-lookup"><span data-stu-id="45a5e-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="45a5e-113">若 **為 TRUE**，表示物件及其所有子系都已靜音。</span><span class="sxs-lookup"><span data-stu-id="45a5e-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45a5e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="45a5e-114">Return value</span></span>

<span data-ttu-id="45a5e-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="45a5e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45a5e-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="45a5e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a5e-117">備註</span><span class="sxs-lookup"><span data-stu-id="45a5e-117">Remarks</span></span>

<span data-ttu-id="45a5e-118">將物件靜音，也會靜音物件中包含的任何子系。</span><span class="sxs-lookup"><span data-stu-id="45a5e-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="45a5e-119">例如，如果您將曲目靜音，該播放軌的轉換、來源和效果也會靜音。</span><span class="sxs-lookup"><span data-stu-id="45a5e-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="45a5e-120">一旦物件不再為靜音，其子系會還原為其先前的狀態，可能是靜音或 unmuted。</span><span class="sxs-lookup"><span data-stu-id="45a5e-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="45a5e-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="45a5e-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="45a5e-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="45a5e-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="45a5e-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="45a5e-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45a5e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="45a5e-124">Requirements</span></span>



| <span data-ttu-id="45a5e-125">需求</span><span class="sxs-lookup"><span data-stu-id="45a5e-125">Requirement</span></span> | <span data-ttu-id="45a5e-126">值</span><span class="sxs-lookup"><span data-stu-id="45a5e-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45a5e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="45a5e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="45a5e-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="45a5e-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="45a5e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="45a5e-129">Library</span></span><br/> | <dl> <span data-ttu-id="45a5e-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45a5e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45a5e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45a5e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a5e-132">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="45a5e-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="45a5e-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="45a5e-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




