---
description: EffectSwapPriorities 方法會切換兩個效果的優先權層級。
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'IAMTimelineEffectable：： EffectSwapPriorities 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980241"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="ac8e6-103">IAMTimelineEffectable：： EffectSwapPriorities 方法</span><span class="sxs-lookup"><span data-stu-id="ac8e6-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="ac8e6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-104">\[Deprecated.</span></span> <span data-ttu-id="ac8e6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ac8e6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ac8e6-106">`EffectSwapPriorities`方法會切換兩個效果的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="ac8e6-107">由於有兩個優先權值，此方法會交換那些優先順序的效果。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="ac8e6-108">當方法傳回時，第一個優先權層級的效果會是第二個優先權層級，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8e6-109">語法</span><span class="sxs-lookup"><span data-stu-id="ac8e6-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="ac8e6-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac8e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac8e6-111">*PriorityA*</span><span class="sxs-lookup"><span data-stu-id="ac8e6-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="ac8e6-112">要交換效果的第一個優先權層級。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="ac8e6-113">*PriorityB*</span><span class="sxs-lookup"><span data-stu-id="ac8e6-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="ac8e6-114">交換效果的第二個優先權層級。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac8e6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac8e6-115">Return value</span></span>

<span data-ttu-id="ac8e6-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac8e6-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac8e6-118">備註</span><span class="sxs-lookup"><span data-stu-id="ac8e6-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac8e6-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ac8e6-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ac8e6-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ac8e6-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac8e6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac8e6-122">Requirements</span></span>



| <span data-ttu-id="ac8e6-123">需求</span><span class="sxs-lookup"><span data-stu-id="ac8e6-123">Requirement</span></span> | <span data-ttu-id="ac8e6-124">值</span><span class="sxs-lookup"><span data-stu-id="ac8e6-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8e6-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ac8e6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ac8e6-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac8e6-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ac8e6-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac8e6-127">Library</span></span><br/> | <dl> <span data-ttu-id="ac8e6-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac8e6-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac8e6-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac8e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac8e6-130">**IAMTimelineEffectable 介面**</span><span class="sxs-lookup"><span data-stu-id="ac8e6-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="ac8e6-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ac8e6-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




