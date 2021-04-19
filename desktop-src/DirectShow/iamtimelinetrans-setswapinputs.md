---
description: SetSwapInputs 方法會指定是否交換轉換輸入。
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'IAMTimelineTrans：： SetSwapInputs 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995480"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="449bb-103">IAMTimelineTrans：： SetSwapInputs 方法</span><span class="sxs-lookup"><span data-stu-id="449bb-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="449bb-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="449bb-104">\[Deprecated.</span></span> <span data-ttu-id="449bb-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="449bb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="449bb-106">`SetSwapInputs`方法會指定是否交換轉換輸入。</span><span class="sxs-lookup"><span data-stu-id="449bb-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="449bb-107">根據預設，轉換會從所有較低優先順序層級的複合轉換成轉換所在的圖層。</span><span class="sxs-lookup"><span data-stu-id="449bb-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="449bb-108">您可以反轉這項進展，讓轉換從它所在的圖層移回較低優先順序層級的組合。</span><span class="sxs-lookup"><span data-stu-id="449bb-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="449bb-109">如需詳細資訊，請參閱 [轉換方向](transition-direction.md)。</span><span class="sxs-lookup"><span data-stu-id="449bb-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="449bb-110">語法</span><span class="sxs-lookup"><span data-stu-id="449bb-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="449bb-111">參數</span><span class="sxs-lookup"><span data-stu-id="449bb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="449bb-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="449bb-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="449bb-113">指定是否交換輸入。</span><span class="sxs-lookup"><span data-stu-id="449bb-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="449bb-114">如果 **為 FALSE**，則轉換會從所有較低優先順序層級到轉換圖層的複合。</span><span class="sxs-lookup"><span data-stu-id="449bb-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="449bb-115">若 **為 TRUE**，則轉換會以相反的方向進行。</span><span class="sxs-lookup"><span data-stu-id="449bb-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="449bb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="449bb-116">Return value</span></span>

<span data-ttu-id="449bb-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="449bb-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="449bb-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="449bb-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="449bb-119">備註</span><span class="sxs-lookup"><span data-stu-id="449bb-119">Remarks</span></span>

<span data-ttu-id="449bb-120">這個方法不會變更視覺效果的方向。</span><span class="sxs-lookup"><span data-stu-id="449bb-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="449bb-121">例如，從左至右的抹除仍會由左至右。</span><span class="sxs-lookup"><span data-stu-id="449bb-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="449bb-122">若要變更方向，請使用 [**IPropertySetter**](ipropertysetter.md)介面設定 **進度** 屬性。</span><span class="sxs-lookup"><span data-stu-id="449bb-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="449bb-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="449bb-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="449bb-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="449bb-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="449bb-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="449bb-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="449bb-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="449bb-126">Requirements</span></span>



| <span data-ttu-id="449bb-127">需求</span><span class="sxs-lookup"><span data-stu-id="449bb-127">Requirement</span></span> | <span data-ttu-id="449bb-128">值</span><span class="sxs-lookup"><span data-stu-id="449bb-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="449bb-129">標頭</span><span class="sxs-lookup"><span data-stu-id="449bb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="449bb-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="449bb-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="449bb-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="449bb-131">Library</span></span><br/> | <dl> <span data-ttu-id="449bb-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="449bb-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="449bb-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="449bb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449bb-134">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="449bb-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="449bb-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="449bb-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




