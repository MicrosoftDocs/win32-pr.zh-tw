---
description: IAMTimelineEffect 介面會提供方法，在 (DES) 的 DirectShow 編輯服務中操作音訊和影片效果。
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: 'IAMTimelineEffect 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996519"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="828bc-103">IAMTimelineEffect 介面</span><span class="sxs-lookup"><span data-stu-id="828bc-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="828bc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="828bc-104">\[Deprecated.</span></span> <span data-ttu-id="828bc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="828bc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="828bc-106">`IAMTimelineEffect`介面提供在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中操作音訊和影片效果的方法。</span><span class="sxs-lookup"><span data-stu-id="828bc-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="828bc-107">效果可以加入至任何公開 [**IAMTimelineEffectable**](iamtimelineeffectable.md) 介面的時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="828bc-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="828bc-108">若要設定效果的屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="828bc-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="828bc-109">DES 效果物件實際上是兩個其他物件之一的包裝函式：</span><span class="sxs-lookup"><span data-stu-id="828bc-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="828bc-110">針對音訊效果，任何 DirectShow 音訊效果篩選。</span><span class="sxs-lookup"><span data-stu-id="828bc-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="828bc-111">適用于影片效果和1輸入 DirectX 轉換物件。</span><span class="sxs-lookup"><span data-stu-id="828bc-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="828bc-112">Microsoft 不再支援協力廠商 DirectX 轉換物件的開發。</span><span class="sxs-lookup"><span data-stu-id="828bc-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="828bc-113">若要指定效果的篩選或 DirectX 轉換物件，請呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="828bc-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="828bc-114">若要建立效果物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 與值時間軸的 \_ 主要 \_ 類型 \_ 效果。</span><span class="sxs-lookup"><span data-stu-id="828bc-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="828bc-115">您可以查詢傳回的介面 [**IAMTimelineObj**](iamtimelineobj.md) 指標 `IAMTimelineEffect` 。</span><span class="sxs-lookup"><span data-stu-id="828bc-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="828bc-116">成員</span><span class="sxs-lookup"><span data-stu-id="828bc-116">Members</span></span>

<span data-ttu-id="828bc-117">**IAMTimelineEffect** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="828bc-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="828bc-118">**IAMTimelineEffect** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="828bc-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="828bc-119">方法</span><span class="sxs-lookup"><span data-stu-id="828bc-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="828bc-120">方法</span><span class="sxs-lookup"><span data-stu-id="828bc-120">Methods</span></span>

<span data-ttu-id="828bc-121">**IAMTimelineEffect** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="828bc-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="828bc-122">方法</span><span class="sxs-lookup"><span data-stu-id="828bc-122">Method</span></span>                                                           | <span data-ttu-id="828bc-123">描述</span><span class="sxs-lookup"><span data-stu-id="828bc-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="828bc-124">**EffectGetPriority**</span><span class="sxs-lookup"><span data-stu-id="828bc-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="828bc-125">抓取效果的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="828bc-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="828bc-126">備註</span><span class="sxs-lookup"><span data-stu-id="828bc-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="828bc-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="828bc-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="828bc-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="828bc-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="828bc-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="828bc-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="828bc-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="828bc-130">Requirements</span></span>



| <span data-ttu-id="828bc-131">需求</span><span class="sxs-lookup"><span data-stu-id="828bc-131">Requirement</span></span> | <span data-ttu-id="828bc-132">值</span><span class="sxs-lookup"><span data-stu-id="828bc-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="828bc-133">標頭</span><span class="sxs-lookup"><span data-stu-id="828bc-133">Header</span></span><br/>  | <dl> <span data-ttu-id="828bc-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="828bc-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="828bc-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="828bc-135">Library</span></span><br/> | <dl> <span data-ttu-id="828bc-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="828bc-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828bc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="828bc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828bc-138">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="828bc-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
