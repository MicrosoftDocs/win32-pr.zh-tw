---
description: 代表繪製時要套用至筆墨的屬性。
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: 'InkDrawingAttributes 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320139"
---
# <a name="inkdrawingattributes-class"></a><span data-ttu-id="a449a-103">InkDrawingAttributes 類別</span><span class="sxs-lookup"><span data-stu-id="a449a-103">InkDrawingAttributes class</span></span>

<span data-ttu-id="a449a-104">代表繪製時要套用至筆墨的屬性。</span><span class="sxs-lookup"><span data-stu-id="a449a-104">Represents the attributes that are applied to ink when it is drawn.</span></span>

<span data-ttu-id="a449a-105">**InkDrawingAttributes** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a449a-105">**InkDrawingAttributes** has these types of members:</span></span>

-   [<span data-ttu-id="a449a-106">介面</span><span class="sxs-lookup"><span data-stu-id="a449a-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="a449a-107">方法</span><span class="sxs-lookup"><span data-stu-id="a449a-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="a449a-108">屬性</span><span class="sxs-lookup"><span data-stu-id="a449a-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="a449a-109">介面</span><span class="sxs-lookup"><span data-stu-id="a449a-109">Interfaces</span></span>

<span data-ttu-id="a449a-110">**InkDrawingAttributes** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="a449a-110">The **InkDrawingAttributes** class defines these interfaces.</span></span>



| <span data-ttu-id="a449a-111">介面</span><span class="sxs-lookup"><span data-stu-id="a449a-111">Interface</span></span>                 | <span data-ttu-id="a449a-112">描述</span><span class="sxs-lookup"><span data-stu-id="a449a-112">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="a449a-113">**IInkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="a449a-113">**IInkDrawingAttributes**</span></span> | <span data-ttu-id="a449a-114">這個物件會實 **IInkDrawingAttributes** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="a449a-114">This object implements the **IInkDrawingAttributes** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="a449a-115">方法</span><span class="sxs-lookup"><span data-stu-id="a449a-115">Methods</span></span>

<span data-ttu-id="a449a-116">**InkDrawingAttributes** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a449a-116">The **InkDrawingAttributes** class has these methods.</span></span>



| <span data-ttu-id="a449a-117">方法</span><span class="sxs-lookup"><span data-stu-id="a449a-117">Method</span></span>                         | <span data-ttu-id="a449a-118">描述</span><span class="sxs-lookup"><span data-stu-id="a449a-118">Description</span></span>                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a449a-119">**克隆**</span><span class="sxs-lookup"><span data-stu-id="a449a-119">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | <span data-ttu-id="a449a-120">建立重複的 [**InkDisp**](inkdisp-class.md)、 **InkDrawingAttributes** 或 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a449a-120">Creates a duplicate [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes**, or [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a449a-121">屬性</span><span class="sxs-lookup"><span data-stu-id="a449a-121">Properties</span></span>

<span data-ttu-id="a449a-122">**InkDrawingAttributes** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a449a-122">The **InkDrawingAttributes** class has these properties.</span></span>



| <span data-ttu-id="a449a-123">屬性</span><span class="sxs-lookup"><span data-stu-id="a449a-123">Property</span></span>                                                                           | <span data-ttu-id="a449a-124">存取類型</span><span class="sxs-lookup"><span data-stu-id="a449a-124">Access type</span></span>           | <span data-ttu-id="a449a-125">Description</span><span class="sxs-lookup"><span data-stu-id="a449a-125">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a449a-126">**效果**</span><span class="sxs-lookup"><span data-stu-id="a449a-126">**AntiAliased**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | <span data-ttu-id="a449a-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-127">Read/write</span></span><br/> | <span data-ttu-id="a449a-128">取得或設定值，這個值會指定沿著筆墨邊緣的前景和背景色彩是否經過混合，以增加筆墨筆劃的平滑。</span><span class="sxs-lookup"><span data-stu-id="a449a-128">Gets or sets the value that specifies whether the foreground and background colors along the edge of the ink are blended to increase the smoothness of an ink stroke.</span></span><br/> |
| [<span data-ttu-id="a449a-129">**色彩**</span><span class="sxs-lookup"><span data-stu-id="a449a-129">**Color**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | <span data-ttu-id="a449a-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-130">Read/write</span></span><br/> | <span data-ttu-id="a449a-131">取得或設定使用這個 **InkDrawingAttributes** 物件繪製的筆墨色彩。</span><span class="sxs-lookup"><span data-stu-id="a449a-131">Gets or sets the color of the ink drawn with this **InkDrawingAttributes** object.</span></span><br/>                                                                                    |
| [<span data-ttu-id="a449a-132">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="a449a-132">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="a449a-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="a449a-133">Read-only</span></span><br/>  | <span data-ttu-id="a449a-134">取得儲存在 **InkDrawingAttributes** 物件中之應用程式定義資料的集合。</span><span class="sxs-lookup"><span data-stu-id="a449a-134">Gets the collection of application-defined data that is stored in the **InkDrawingAttributes** object.</span></span><br/>                                                                |
| [<span data-ttu-id="a449a-135">**FitToCurve**</span><span class="sxs-lookup"><span data-stu-id="a449a-135">**FitToCurve**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | <span data-ttu-id="a449a-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-136">Read/write</span></span><br/> | <span data-ttu-id="a449a-137">取得或設定值，這個值會指定是否將筆墨轉譯為一連串的曲線，而不是畫筆取樣點之間的線條。</span><span class="sxs-lookup"><span data-stu-id="a449a-137">Gets or sets the value that specifies whether ink is rendered as a series of curves instead of as lines between pen sample points.</span></span><br/>                                    |
| [<span data-ttu-id="a449a-138">**高度**</span><span class="sxs-lookup"><span data-stu-id="a449a-138">**Height**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | <span data-ttu-id="a449a-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-139">Read/write</span></span><br/> | <span data-ttu-id="a449a-140">取得或設定使用這個 **InkDrawingAttributes** 物件繪製筆墨時，畫筆的高度。</span><span class="sxs-lookup"><span data-stu-id="a449a-140">Gets or sets the height of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                        |
| [<span data-ttu-id="a449a-141">**IgnorePressure**</span><span class="sxs-lookup"><span data-stu-id="a449a-141">**IgnorePressure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | <span data-ttu-id="a449a-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-142">Read/write</span></span><br/> | <span data-ttu-id="a449a-143">取得或設定值，這個值會指定是否會在 tablet 介面上增加畫筆提示的壓力，以自動放大繪圖筆墨。</span><span class="sxs-lookup"><span data-stu-id="a449a-143">Gets or sets the value that specifies whether drawn ink automatically becomes wider with increased pressure of the pen tip on the tablet surface.</span></span><br/>                     |
| [<span data-ttu-id="a449a-144">**PenTip**</span><span class="sxs-lookup"><span data-stu-id="a449a-144">**PenTip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | <span data-ttu-id="a449a-145">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-145">Read/write</span></span><br/> | <span data-ttu-id="a449a-146">取得或設定在使用這個 **InkDrawingAttributes** 物件繪製筆墨時，要使用 (球或矩形) 的畫筆提示。</span><span class="sxs-lookup"><span data-stu-id="a449a-146">Gets or sets the pen tip to use (ball or rectangle) when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                       |
| [<span data-ttu-id="a449a-147">**RasterOperation**</span><span class="sxs-lookup"><span data-stu-id="a449a-147">**RasterOperation**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | <span data-ttu-id="a449a-148">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-148">Read/write</span></span><br/> | <span data-ttu-id="a449a-149">取得或設定畫筆色彩如何在繪製筆墨時，與顯示上現有的背景色彩互動。</span><span class="sxs-lookup"><span data-stu-id="a449a-149">Gets or sets how the pen color interacts with the existing background colors on the display when the ink is drawn.</span></span><br/>                                                    |
| [<span data-ttu-id="a449a-150">**透明度**</span><span class="sxs-lookup"><span data-stu-id="a449a-150">**Transparency**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | <span data-ttu-id="a449a-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-151">Read/write</span></span><br/> | <span data-ttu-id="a449a-152">取得或設定繪製筆墨的透明度值。</span><span class="sxs-lookup"><span data-stu-id="a449a-152">Gets or sets the transparency value of drawn ink.</span></span> <span data-ttu-id="a449a-153">值的範圍從零 (完全不透明) 至 255 (完全透明) 。</span><span class="sxs-lookup"><span data-stu-id="a449a-153">Values range from zero (totally opaque) to 255 (totally transparent).</span></span><br/>                                               |
| [<span data-ttu-id="a449a-154">**寬度**</span><span class="sxs-lookup"><span data-stu-id="a449a-154">**Width**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | <span data-ttu-id="a449a-155">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a449a-155">Read/write</span></span><br/> | <span data-ttu-id="a449a-156">取得或設定使用這個 **InkDrawingAttributes** 物件繪製筆墨時畫筆的寬度。</span><span class="sxs-lookup"><span data-stu-id="a449a-156">Gets or sets the width of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="a449a-157">備註</span><span class="sxs-lookup"><span data-stu-id="a449a-157">Remarks</span></span>

<span data-ttu-id="a449a-158">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="a449a-158">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="a449a-159">這些繪圖屬性可以與筆劃或游標相關聯，並指定色彩、寬度和透明度等設定。</span><span class="sxs-lookup"><span data-stu-id="a449a-159">These drawing attributes can be associated with a stroke or a cursor and specify settings such as color, width, and transparency.</span></span>

<span data-ttu-id="a449a-160">若要指定筆劃的繪圖屬性，請使用 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)屬性。</span><span class="sxs-lookup"><span data-stu-id="a449a-160">To specify the drawing attributes of a stroke, use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span> <span data-ttu-id="a449a-161">若要指定筆劃集合內所有筆劃的繪製屬性，請呼叫 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合的 [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)方法。</span><span class="sxs-lookup"><span data-stu-id="a449a-161">To specify the drawing attributes of all of the strokes within a collection of strokes, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

<span data-ttu-id="a449a-162">每個 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件和 [InkPicture](inkpicture-control-reference.md) 控制項都可以針對相同的資料指標指定一組不同的繪圖屬性。</span><span class="sxs-lookup"><span data-stu-id="a449a-162">Each [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control can specify a different set of drawing attributes for the same cursor.</span></span> <span data-ttu-id="a449a-163">您可以使用 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)屬性來取得或設定資料指標的繪製屬性。</span><span class="sxs-lookup"><span data-stu-id="a449a-163">Use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object to get or set the drawing attributes of a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="a449a-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="a449a-164">Requirements</span></span>



| <span data-ttu-id="a449a-165">需求</span><span class="sxs-lookup"><span data-stu-id="a449a-165">Requirement</span></span> | <span data-ttu-id="a449a-166">值</span><span class="sxs-lookup"><span data-stu-id="a449a-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a449a-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a449a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a449a-168">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a449a-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a449a-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a449a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a449a-170">都不支援</span><span class="sxs-lookup"><span data-stu-id="a449a-170">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a449a-171">標頭</span><span class="sxs-lookup"><span data-stu-id="a449a-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="a449a-172"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a449a-172"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a449a-173">程式庫</span><span class="sxs-lookup"><span data-stu-id="a449a-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="a449a-174"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a449a-174"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a449a-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a449a-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a449a-176">**DrawingAttributes 屬性**</span><span class="sxs-lookup"><span data-stu-id="a449a-176">**DrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

<span data-ttu-id="a449a-177">**DrawingAttributes 屬性**</span><span class="sxs-lookup"><span data-stu-id="a449a-177">**DrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="a449a-178">**DrawingAttributes 屬性**</span><span class="sxs-lookup"><span data-stu-id="a449a-178">**DrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="a449a-179">**System.windows.controls.inkcanvas.defaultdrawingattributes 屬性**</span><span class="sxs-lookup"><span data-stu-id="a449a-179">**DefaultDrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

<span data-ttu-id="a449a-180">**System.windows.controls.inkcanvas.defaultdrawingattributes 屬性**</span><span class="sxs-lookup"><span data-stu-id="a449a-180">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="a449a-181">**System.windows.controls.inkcanvas.defaultdrawingattributes 屬性**</span><span class="sxs-lookup"><span data-stu-id="a449a-181">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="a449a-182">**ModifyDrawingAttributes 方法**</span><span class="sxs-lookup"><span data-stu-id="a449a-182">**ModifyDrawingAttributes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[<span data-ttu-id="a449a-183">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="a449a-183">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="a449a-184">**InkDisp 類別**</span><span class="sxs-lookup"><span data-stu-id="a449a-184">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

[<span data-ttu-id="a449a-185">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="a449a-185">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

