---
description: SetDefaultEffect 方法會設定預設效果。 如果轉譯引擎無法轉譯效果，則會替代預設效果。
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'IAMTimeline：： SetDefaultEffect 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995690"
---
# <a name="iamtimelinesetdefaulteffect-method"></a><span data-ttu-id="b2e16-104">IAMTimeline：： SetDefaultEffect 方法</span><span class="sxs-lookup"><span data-stu-id="b2e16-104">IAMTimeline::SetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="b2e16-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b2e16-105">\[Deprecated.</span></span> <span data-ttu-id="b2e16-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b2e16-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2e16-107">`SetDefaultEffect`方法會設定預設效果。</span><span class="sxs-lookup"><span data-stu-id="b2e16-107">The `SetDefaultEffect` method sets the default effect.</span></span> <span data-ttu-id="b2e16-108">如果轉譯引擎無法轉譯效果，則會替代預設效果。</span><span class="sxs-lookup"><span data-stu-id="b2e16-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e16-109">語法</span><span class="sxs-lookup"><span data-stu-id="b2e16-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="b2e16-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2e16-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e16-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="b2e16-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="b2e16-112">預設效果的 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="b2e16-112">Pointer to the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e16-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2e16-113">Return value</span></span>

<span data-ttu-id="b2e16-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b2e16-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2e16-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b2e16-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e16-116">備註</span><span class="sxs-lookup"><span data-stu-id="b2e16-116">Remarks</span></span>

<span data-ttu-id="b2e16-117">如果您未設定預設效果，或您指定為預設值的效果造成錯誤，DES 會使用它自己的預設效果。</span><span class="sxs-lookup"><span data-stu-id="b2e16-117">If you do not set a default effect, or if the effect that you specify as a default causes an error, DES uses its own default effect.</span></span>

> [!Note]  
> <span data-ttu-id="b2e16-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b2e16-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2e16-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b2e16-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2e16-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b2e16-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2e16-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2e16-121">Requirements</span></span>



| <span data-ttu-id="b2e16-122">需求</span><span class="sxs-lookup"><span data-stu-id="b2e16-122">Requirement</span></span> | <span data-ttu-id="b2e16-123">值</span><span class="sxs-lookup"><span data-stu-id="b2e16-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e16-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b2e16-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b2e16-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e16-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2e16-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2e16-126">Library</span></span><br/> | <dl> <span data-ttu-id="b2e16-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2e16-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e16-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2e16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e16-129">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="b2e16-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="b2e16-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b2e16-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




