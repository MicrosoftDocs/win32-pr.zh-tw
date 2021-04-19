---
description: IAMTimelineTrans 介面提供在 (DES) 的 DirectShow 編輯服務中操作轉換的方法。
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: 'IAMTimelineTrans 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995496"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="3be7b-103">IAMTimelineTrans 介面</span><span class="sxs-lookup"><span data-stu-id="3be7b-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="3be7b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3be7b-104">\[Deprecated.</span></span> <span data-ttu-id="3be7b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3be7b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3be7b-106">`IAMTimelineTrans`介面提供在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中操作轉換的方法。</span><span class="sxs-lookup"><span data-stu-id="3be7b-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="3be7b-107">轉換是指一個影片圖層和以較低優先順序呈現的所有影片層級之間的進展。</span><span class="sxs-lookup"><span data-stu-id="3be7b-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="3be7b-108">轉換可以新增至任何可公開 [**IAMTimelineTransable**](iamtimelinetransable.md) 介面的時間軸物件。</span><span class="sxs-lookup"><span data-stu-id="3be7b-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="3be7b-109">若要設定轉換的屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="3be7b-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="3be7b-110">DES 轉換物件實際上是 DirectX 轉換物件的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="3be7b-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="3be7b-111">任何2輸入的 DirectX 轉換物件都可以用來執行轉換的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="3be7b-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="3be7b-112">Microsoft 不再支援協力廠商 DirectX 轉換物件的開發。</span><span class="sxs-lookup"><span data-stu-id="3be7b-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="3be7b-113">若要指定轉換的 DirectX 轉換物件，請呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3be7b-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="3be7b-114">若要建立轉換物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) ，其值時間軸 \_ 主要 \_ 類型 \_ 轉換。</span><span class="sxs-lookup"><span data-stu-id="3be7b-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="3be7b-115">您可以查詢傳回的介面 [**IAMTimelineObj**](iamtimelineobj.md) 指標 `IAMTimelineTrans` 。</span><span class="sxs-lookup"><span data-stu-id="3be7b-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="3be7b-116">成員</span><span class="sxs-lookup"><span data-stu-id="3be7b-116">Members</span></span>

<span data-ttu-id="3be7b-117">**IAMTimelineTrans** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3be7b-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3be7b-118">**IAMTimelineTrans** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3be7b-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="3be7b-119">方法</span><span class="sxs-lookup"><span data-stu-id="3be7b-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3be7b-120">方法</span><span class="sxs-lookup"><span data-stu-id="3be7b-120">Methods</span></span>

<span data-ttu-id="3be7b-121">**IAMTimelineTrans** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3be7b-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="3be7b-122">方法</span><span class="sxs-lookup"><span data-stu-id="3be7b-122">Method</span></span>                                                  | <span data-ttu-id="3be7b-123">描述</span><span class="sxs-lookup"><span data-stu-id="3be7b-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="3be7b-124">**GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="3be7b-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="3be7b-125">抓取剪下點。</span><span class="sxs-lookup"><span data-stu-id="3be7b-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="3be7b-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="3be7b-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="3be7b-127">以 [**REFTIME**](reftime.md) 值形式捕獲剪下點。</span><span class="sxs-lookup"><span data-stu-id="3be7b-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="3be7b-128">**GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="3be7b-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="3be7b-129">判斷轉換是否轉譯為剪下。</span><span class="sxs-lookup"><span data-stu-id="3be7b-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="3be7b-130">**GetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="3be7b-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="3be7b-131">抓取值，這個值表示是否交換轉換輸入。</span><span class="sxs-lookup"><span data-stu-id="3be7b-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="3be7b-132">**SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="3be7b-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="3be7b-133">設定剪下點。</span><span class="sxs-lookup"><span data-stu-id="3be7b-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="3be7b-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="3be7b-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="3be7b-135">將剪點設定為 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="3be7b-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="3be7b-136">**SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="3be7b-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="3be7b-137">指定轉換是否轉譯為剪下。</span><span class="sxs-lookup"><span data-stu-id="3be7b-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="3be7b-138">**SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="3be7b-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="3be7b-139">指定是否交換轉換輸入。</span><span class="sxs-lookup"><span data-stu-id="3be7b-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="3be7b-140">備註</span><span class="sxs-lookup"><span data-stu-id="3be7b-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3be7b-141">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3be7b-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3be7b-142">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3be7b-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3be7b-143">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3be7b-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3be7b-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="3be7b-144">Requirements</span></span>



| <span data-ttu-id="3be7b-145">需求</span><span class="sxs-lookup"><span data-stu-id="3be7b-145">Requirement</span></span> | <span data-ttu-id="3be7b-146">值</span><span class="sxs-lookup"><span data-stu-id="3be7b-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3be7b-147">標頭</span><span class="sxs-lookup"><span data-stu-id="3be7b-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3be7b-148"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3be7b-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3be7b-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="3be7b-149">Library</span></span><br/> | <dl> <span data-ttu-id="3be7b-150"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3be7b-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3be7b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3be7b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be7b-152">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="3be7b-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
