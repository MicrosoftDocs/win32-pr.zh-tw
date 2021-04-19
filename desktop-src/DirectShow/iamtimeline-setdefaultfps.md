---
description: SetDefaultFPS 方法會設定預設輸出畫面播放速率（以每秒的畫面格速率為單位）。 群組會使用此值做為其預設的畫面播放速率。 若要設定群組的畫面播放速率，請在群組上呼叫 IAMTimelineGroup：： SetOutputFPS 方法。
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: 'IAMTimeline：： SetDefaultFPS 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 20c352f40234672ceeb2d4c25ea9db04e89f712d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983144"
---
# <a name="iamtimelinesetdefaultfps-method"></a><span data-ttu-id="da4e1-105">IAMTimeline：： SetDefaultFPS 方法</span><span class="sxs-lookup"><span data-stu-id="da4e1-105">IAMTimeline::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="da4e1-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="da4e1-106">\[Deprecated.</span></span> <span data-ttu-id="da4e1-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="da4e1-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da4e1-108">`SetDefaultFPS`方法會設定預設輸出畫面播放速率（以每秒畫面格速率為單位）。</span><span class="sxs-lookup"><span data-stu-id="da4e1-108">The `SetDefaultFPS` method sets the default output frame rate, in frames per second.</span></span> <span data-ttu-id="da4e1-109">群組會使用此值做為其預設的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="da4e1-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="da4e1-110">若要設定群組的畫面播放速率，請在群組上呼叫 [**IAMTimelineGroup：： SetOutputFPS**](iamtimelinegroup-setoutputfps.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="da4e1-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4e1-111">語法</span><span class="sxs-lookup"><span data-stu-id="da4e1-111">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="da4e1-112">參數</span><span class="sxs-lookup"><span data-stu-id="da4e1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4e1-113">*FPS*</span><span class="sxs-lookup"><span data-stu-id="da4e1-113">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="da4e1-114">預設畫面播放速率（以每秒畫面格速率為單位）。</span><span class="sxs-lookup"><span data-stu-id="da4e1-114">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4e1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="da4e1-115">Return value</span></span>

<span data-ttu-id="da4e1-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="da4e1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da4e1-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da4e1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da4e1-118">備註</span><span class="sxs-lookup"><span data-stu-id="da4e1-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="da4e1-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="da4e1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="da4e1-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="da4e1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="da4e1-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="da4e1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da4e1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="da4e1-122">Requirements</span></span>



| <span data-ttu-id="da4e1-123">需求</span><span class="sxs-lookup"><span data-stu-id="da4e1-123">Requirement</span></span> | <span data-ttu-id="da4e1-124">值</span><span class="sxs-lookup"><span data-stu-id="da4e1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da4e1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="da4e1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="da4e1-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="da4e1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="da4e1-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="da4e1-127">Library</span></span><br/> | <dl> <span data-ttu-id="da4e1-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da4e1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4e1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da4e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4e1-130">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="da4e1-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="da4e1-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="da4e1-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




