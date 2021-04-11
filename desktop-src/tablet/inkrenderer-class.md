---
description: 表示從筆墨到顯示視窗的對應管理。 使用 InkRenderer 物件在視窗中顯示筆墨。 您也可以使用它來調整筆劃的位置並調整其大小。
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: 'InkRenderer 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195321"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="d557d-105">InkRenderer 類別</span><span class="sxs-lookup"><span data-stu-id="d557d-105">InkRenderer class</span></span>

<span data-ttu-id="d557d-106">表示從筆墨到顯示視窗的對應管理。</span><span class="sxs-lookup"><span data-stu-id="d557d-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="d557d-107">使用 **InkRenderer** 物件在視窗中顯示筆墨。</span><span class="sxs-lookup"><span data-stu-id="d557d-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="d557d-108">您也可以使用它來調整筆劃的位置並調整其大小。</span><span class="sxs-lookup"><span data-stu-id="d557d-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="d557d-109">**InkRenderer** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d557d-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="d557d-110">介面</span><span class="sxs-lookup"><span data-stu-id="d557d-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="d557d-111">方法</span><span class="sxs-lookup"><span data-stu-id="d557d-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="d557d-112">介面</span><span class="sxs-lookup"><span data-stu-id="d557d-112">Interfaces</span></span>

<span data-ttu-id="d557d-113">**InkRenderer** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="d557d-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="d557d-114">介面</span><span class="sxs-lookup"><span data-stu-id="d557d-114">Interface</span></span>        | <span data-ttu-id="d557d-115">描述</span><span class="sxs-lookup"><span data-stu-id="d557d-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="d557d-116">**IInkRenderer**</span><span class="sxs-lookup"><span data-stu-id="d557d-116">**IInkRenderer**</span></span> | <span data-ttu-id="d557d-117">這個物件會實 **IInkRenderer** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="d557d-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d557d-118">方法</span><span class="sxs-lookup"><span data-stu-id="d557d-118">Methods</span></span>

<span data-ttu-id="d557d-119">**InkRenderer** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d557d-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="d557d-120">方法</span><span class="sxs-lookup"><span data-stu-id="d557d-120">Method</span></span>                                                                     | <span data-ttu-id="d557d-121">描述</span><span class="sxs-lookup"><span data-stu-id="d557d-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d557d-122">**Draw**</span><span class="sxs-lookup"><span data-stu-id="d557d-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="d557d-123">在裝置內容上繪製筆觸。</span><span class="sxs-lookup"><span data-stu-id="d557d-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d557d-124">**DrawStroke**</span><span class="sxs-lookup"><span data-stu-id="d557d-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="d557d-125">在指定的 windows 裝置內容上繪製筆劃。</span><span class="sxs-lookup"><span data-stu-id="d557d-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d557d-126">**GetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="d557d-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="d557d-127">抓取用來呈現筆墨的物件轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d557d-128">**GetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="d557d-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="d557d-129">抓取用來呈現筆墨的視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d557d-130">**InkSpaceToPixel**</span><span class="sxs-lookup"><span data-stu-id="d557d-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="d557d-131">將筆墨空間座標中的位置轉換成圖元空間。</span><span class="sxs-lookup"><span data-stu-id="d557d-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="d557d-132">**InkSpaceToPixelFromPoints**</span><span class="sxs-lookup"><span data-stu-id="d557d-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="d557d-133">將筆墨空間座標中的點陣列轉換成圖元空間。</span><span class="sxs-lookup"><span data-stu-id="d557d-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="d557d-134">**Measure**</span><span class="sxs-lookup"><span data-stu-id="d557d-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="d557d-135">計算裝置內容上的矩形，如果它們是使用 **InkRenderer** 物件繪製，則會包含筆劃集合。</span><span class="sxs-lookup"><span data-stu-id="d557d-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="d557d-136">**MeasureStroke**</span><span class="sxs-lookup"><span data-stu-id="d557d-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="d557d-137">計算裝置內容上的矩形，如果它們是使用 **InkRenderer** 物件繪製，則會包含筆劃。</span><span class="sxs-lookup"><span data-stu-id="d557d-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="d557d-138">**移動**</span><span class="sxs-lookup"><span data-stu-id="d557d-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="d557d-139">將翻譯套用至筆墨空間座標的視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="d557d-140">**PixelToInkSpace**</span><span class="sxs-lookup"><span data-stu-id="d557d-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="d557d-141">將圖元座標中的位置轉換成筆墨空間。</span><span class="sxs-lookup"><span data-stu-id="d557d-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d557d-142">**PixelToInkSpaceFromPoints**</span><span class="sxs-lookup"><span data-stu-id="d557d-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="d557d-143">將圖元空間座標中的點陣列轉換成筆墨空間。</span><span class="sxs-lookup"><span data-stu-id="d557d-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="d557d-144">**旋轉**</span><span class="sxs-lookup"><span data-stu-id="d557d-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="d557d-145">將旋轉套用至視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="d557d-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="d557d-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="d557d-147">調整 X 和 Y 維度中的 view 轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d557d-148">**SetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="d557d-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="d557d-149">設定用來呈現筆墨的物件轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="d557d-150">**SetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="d557d-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="d557d-151">設定用來呈現筆墨的視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="d557d-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="d557d-152">備註</span><span class="sxs-lookup"><span data-stu-id="d557d-152">Remarks</span></span>

<span data-ttu-id="d557d-153">也可以透過 **InkRenderer** 物件來進行列印。</span><span class="sxs-lookup"><span data-stu-id="d557d-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="d557d-154">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="d557d-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="d557d-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="d557d-155">Requirements</span></span>



| <span data-ttu-id="d557d-156">需求</span><span class="sxs-lookup"><span data-stu-id="d557d-156">Requirement</span></span> | <span data-ttu-id="d557d-157">值</span><span class="sxs-lookup"><span data-stu-id="d557d-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d557d-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d557d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d557d-159">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d557d-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d557d-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d557d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d557d-161">都不支援</span><span class="sxs-lookup"><span data-stu-id="d557d-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d557d-162">標頭</span><span class="sxs-lookup"><span data-stu-id="d557d-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="d557d-163"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d557d-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d557d-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="d557d-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="d557d-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d557d-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d557d-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d557d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d557d-167">**轉譯器屬性**</span><span class="sxs-lookup"><span data-stu-id="d557d-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="d557d-168">**InkDrawingAttributes 類別**</span><span class="sxs-lookup"><span data-stu-id="d557d-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="d557d-169">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="d557d-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="d557d-170">[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d557d-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

