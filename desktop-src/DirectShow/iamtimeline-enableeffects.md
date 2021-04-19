---
description: EnableEffects 方法會啟用或停用時間軸中的所有效果。 如果已停用效果，它們會保留在時間軸中，但不會呈現。
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'IAMTimeline：： EnableEffects 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e090f115083e2d1433e60d7a8707ded9b89ba433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000757"
---
# <a name="iamtimelineenableeffects-method"></a><span data-ttu-id="52376-104">IAMTimeline：： EnableEffects 方法</span><span class="sxs-lookup"><span data-stu-id="52376-104">IAMTimeline::EnableEffects method</span></span>

> [!Note]  
> <span data-ttu-id="52376-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="52376-105">\[Deprecated.</span></span> <span data-ttu-id="52376-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="52376-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52376-107">`EnableEffects`方法會啟用或停用時間軸中的所有效果。</span><span class="sxs-lookup"><span data-stu-id="52376-107">The `EnableEffects` method enables or disables all effects in the timeline.</span></span> <span data-ttu-id="52376-108">如果已停用效果，它們會保留在時間軸中，但不會呈現。</span><span class="sxs-lookup"><span data-stu-id="52376-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="52376-109">語法</span><span class="sxs-lookup"><span data-stu-id="52376-109">Syntax</span></span>


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="52376-110">參數</span><span class="sxs-lookup"><span data-stu-id="52376-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52376-111">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="52376-111">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="52376-112">指定是否要啟用或停用效果的布林值。</span><span class="sxs-lookup"><span data-stu-id="52376-112">Boolean value that specifies whether to enable or disable effects.</span></span> <span data-ttu-id="52376-113">若 **為 TRUE**，則會啟用效果。</span><span class="sxs-lookup"><span data-stu-id="52376-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="52376-114">如果 **為 FALSE**，則會停用效果。</span><span class="sxs-lookup"><span data-stu-id="52376-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52376-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="52376-115">Return value</span></span>

<span data-ttu-id="52376-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="52376-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52376-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="52376-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="52376-118">備註</span><span class="sxs-lookup"><span data-stu-id="52376-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52376-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="52376-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52376-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="52376-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52376-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="52376-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52376-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="52376-122">Requirements</span></span>



| <span data-ttu-id="52376-123">需求</span><span class="sxs-lookup"><span data-stu-id="52376-123">Requirement</span></span> | <span data-ttu-id="52376-124">值</span><span class="sxs-lookup"><span data-stu-id="52376-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52376-125">標頭</span><span class="sxs-lookup"><span data-stu-id="52376-125">Header</span></span><br/>  | <dl> <span data-ttu-id="52376-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="52376-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52376-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="52376-127">Library</span></span><br/> | <dl> <span data-ttu-id="52376-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52376-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52376-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52376-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52376-130">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="52376-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="52376-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="52376-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




