---
description: EffectsEnabled 方法會判斷是否已啟用效果。 如果已停用效果，它們會保留在時間軸中，但不會呈現。
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'IAMTimeline：： EffectsEnabled 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994241"
---
# <a name="iamtimelineeffectsenabled-method"></a><span data-ttu-id="ce34f-104">IAMTimeline：： EffectsEnabled 方法</span><span class="sxs-lookup"><span data-stu-id="ce34f-104">IAMTimeline::EffectsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="ce34f-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ce34f-105">\[Deprecated.</span></span> <span data-ttu-id="ce34f-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ce34f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ce34f-107">`EffectsEnabled`方法會判斷是否已啟用效果。</span><span class="sxs-lookup"><span data-stu-id="ce34f-107">The `EffectsEnabled` method determines whether effects are enabled.</span></span> <span data-ttu-id="ce34f-108">如果已停用效果，它們會保留在時間軸中，但不會呈現。</span><span class="sxs-lookup"><span data-stu-id="ce34f-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce34f-109">語法</span><span class="sxs-lookup"><span data-stu-id="ce34f-109">Syntax</span></span>


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="ce34f-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce34f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce34f-111">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="ce34f-111">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="ce34f-112">接收布林值，指出是否已啟用效果。</span><span class="sxs-lookup"><span data-stu-id="ce34f-112">Receives a Boolean value indicating whether effects are enabled.</span></span> <span data-ttu-id="ce34f-113">若 **為 TRUE**，則會啟用效果。</span><span class="sxs-lookup"><span data-stu-id="ce34f-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="ce34f-114">如果 **為 FALSE**，則會停用效果。</span><span class="sxs-lookup"><span data-stu-id="ce34f-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce34f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce34f-115">Return value</span></span>

<span data-ttu-id="ce34f-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ce34f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce34f-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce34f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce34f-118">備註</span><span class="sxs-lookup"><span data-stu-id="ce34f-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce34f-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ce34f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce34f-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ce34f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ce34f-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ce34f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce34f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce34f-122">Requirements</span></span>



| <span data-ttu-id="ce34f-123">需求</span><span class="sxs-lookup"><span data-stu-id="ce34f-123">Requirement</span></span> | <span data-ttu-id="ce34f-124">值</span><span class="sxs-lookup"><span data-stu-id="ce34f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce34f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ce34f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ce34f-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce34f-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ce34f-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce34f-127">Library</span></span><br/> | <dl> <span data-ttu-id="ce34f-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce34f-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce34f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce34f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce34f-130">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="ce34f-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="ce34f-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ce34f-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




