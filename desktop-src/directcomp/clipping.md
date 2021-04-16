---
title: '裁剪 (DirectComposition) '
description: 本主題說明 Microsoft DirectComposition 剪輯視覺效果的支援。
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4feb537dfb41053dd1099eca7f122b3284dce95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383794"
---
# <a name="clipping-directcomposition"></a><span data-ttu-id="d7427-103">裁剪 (DirectComposition) </span><span class="sxs-lookup"><span data-stu-id="d7427-103">Clipping (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="d7427-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="d7427-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="d7427-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="d7427-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="d7427-106">裁剪會提供一種方式，藉由將視覺效果或樹狀結構的呈現限制為特定的矩形區域，來只顯示部分的視覺效果或視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="d7427-106">Clipping provides a way to reveal only a portion of a visual or visual tree by limiting the rendering of the visual or tree to a particular rectangular area.</span></span> <span data-ttu-id="d7427-107">本主題說明 Microsoft DirectComposition 剪輯視覺效果的支援。</span><span class="sxs-lookup"><span data-stu-id="d7427-107">This topic describes Microsoft DirectComposition support for clipping visuals.</span></span> <span data-ttu-id="d7427-108">它包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="d7427-108">It includes the following sections:</span></span>

-   [<span data-ttu-id="d7427-109">裁剪矩形</span><span class="sxs-lookup"><span data-stu-id="d7427-109">Clip rectangle</span></span>](#clip-rectangle)
-   [<span data-ttu-id="d7427-110">剪輯物件</span><span class="sxs-lookup"><span data-stu-id="d7427-110">Clip object</span></span>](#clip-object)
-   [<span data-ttu-id="d7427-111">動畫裁剪矩形</span><span class="sxs-lookup"><span data-stu-id="d7427-111">Animated clip rectangle</span></span>](#animated-clip-rectangle)
-   [<span data-ttu-id="d7427-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7427-112">Related topics</span></span>](#related-topics)

## <a name="clip-rectangle"></a><span data-ttu-id="d7427-113">裁剪矩形</span><span class="sxs-lookup"><span data-stu-id="d7427-113">Clip rectangle</span></span>

<span data-ttu-id="d7427-114">視覺物件具有剪輯屬性，可定義視覺效果點陣圖內容中的矩形區域或 *裁剪矩形*。</span><span class="sxs-lookup"><span data-stu-id="d7427-114">A visual object has a Clip property that defines a rectangular region, or *clip rectangle*, within the visual's bitmap content.</span></span> <span data-ttu-id="d7427-115">當視覺效果轉譯至螢幕時，只會在螢幕上繪製剪輯矩形內的點陣圖內容部分，而在裁剪矩形外部延伸的內容則會裁剪 (不會) 繪製出來。</span><span class="sxs-lookup"><span data-stu-id="d7427-115">When the visual is rendered to the screen, only the portion of the bitmap content that is inside the clip rectangle is drawn on the screen, while the content that extends outside the clip rectangle is clipped (not drawn).</span></span> <span data-ttu-id="d7427-116">依預設，[剪輯] 屬性包含所有點陣圖內容。</span><span class="sxs-lookup"><span data-stu-id="d7427-116">By default, the Clip property includes all bitmap content.</span></span>

<span data-ttu-id="d7427-117">視覺效果的剪輯屬性會套用至所有子系和附屬視覺效果。</span><span class="sxs-lookup"><span data-stu-id="d7427-117">A visual's Clip property applies to all child and descendent visuals.</span></span> <span data-ttu-id="d7427-118">換句話說，落在父系剪輯矩形界限外的任何子系或子代內容也會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="d7427-118">In other words, any child or descendent content that falls outside the bounds of the parent's clip rectangle is also clipped.</span></span>

<span data-ttu-id="d7427-119">DirectComposition 會在套用 OffsetX、OffsetY 和2D 轉換屬性之前套用剪輯屬性，但在套用效果和3D 轉換屬性之後。</span><span class="sxs-lookup"><span data-stu-id="d7427-119">DirectComposition applies the Clip property before applying the OffsetX, OffsetY, and 2D Transform properties, but after applying the Effect and 3D Transform properties.</span></span> <span data-ttu-id="d7427-120">這表示2D 轉換、OffsetX 和 OffsetY 將會影響視覺內容和剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-120">This means that 2D Transforms, OffsetX, and OffsetY, will affect both the visual content, and the clip rectangle.</span></span> <span data-ttu-id="d7427-121">而3D 轉換和效果將不會套用至剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-121">Whereas 3D transforms and effects will not apply to the clip rectangle.</span></span>

<span data-ttu-id="d7427-122">例如，套用位移或2D 轉換時，剪輯矩形會受到轉換矩陣的影響。</span><span class="sxs-lookup"><span data-stu-id="d7427-122">For example, when applying an offset or 2D transform, the clip rectangle is affected by the transformation matrix.</span></span> <span data-ttu-id="d7427-123">因此，新增位移和2D 旋轉 (45 度) 以及圓角剪輯矩形將會產生下列結果：</span><span class="sxs-lookup"><span data-stu-id="d7427-123">So adding an offset and a 2D rotate (45 degrees) along with a rounded corner clip rectangle will result in this:</span></span>

![顯示2d 轉換在裁剪矩形上之效果的圖表。](images/clipping2dtransform.png)

<span data-ttu-id="d7427-125">在剪切矩形中套用「3D 轉換」時，剪輯矩形不會受到轉換矩陣的影響。</span><span class="sxs-lookup"><span data-stu-id="d7427-125">When applying a 3D transformation “within” the clip rectangle, the clip rectangle is not affected by the transformation matrix.</span></span> <span data-ttu-id="d7427-126">即使在 Z 軸上套用旋轉 (實際上與先前的範例) 相同，下圖也是結果：</span><span class="sxs-lookup"><span data-stu-id="d7427-126">Even when applying a rotation around the Z axis (effectively the same as the previous example), the following diagram is the result:</span></span>

![圖表顯示3d 轉換不會影響矩形剪輯 (視覺效果在剪輯) 內旋轉。](images/clipping3dtransform.png)

<span data-ttu-id="d7427-128">請注意，在剪輯內旋轉的視覺效果是因為3D 矩陣不會套用至剪輯本身。</span><span class="sxs-lookup"><span data-stu-id="d7427-128">Note that the visual rotated within the clip because the 3D matrix is not applied to the clip itself.</span></span>

<span data-ttu-id="d7427-129">如果 [剪輯] 屬性設定為空白矩形，則會完全裁剪視覺效果;也就是說，視覺效果包含在視覺化樹狀結構中，但不會轉譯任何事物。</span><span class="sxs-lookup"><span data-stu-id="d7427-129">If the Clip property is set to an empty rectangle, the visual is fully clipped; that is, the visual is included in the visual tree, but it does not render anything.</span></span> <span data-ttu-id="d7427-130">如果您不想要在組合中包含特定的視覺效果，請從視覺化樹狀結構中移除該視覺效果，而不是設定空白的剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-130">If you do not want to include a particular visual in a composition, remove the visual from the visual tree instead of setting an empty clip rectangle.</span></span> <span data-ttu-id="d7427-131">移除視覺效果會提高效能。</span><span class="sxs-lookup"><span data-stu-id="d7427-131">Removing the visual results in better performance.</span></span>

<span data-ttu-id="d7427-132">您可以使用 [**IDCompositionVisual：： SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) 方法來設定視覺效果的剪輯屬性。</span><span class="sxs-lookup"><span data-stu-id="d7427-132">You set the Clip property of a visual by using the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) method.</span></span> <span data-ttu-id="d7427-133">這個方法包含多載，可讓您將剪輯屬性的值設定為靜態矩形或剪輯物件。</span><span class="sxs-lookup"><span data-stu-id="d7427-133">This method includes overloads that enable you to set the value of the Clip property to a static rectangle or to a clip object.</span></span> <span data-ttu-id="d7427-134">如果您不需要在視覺效果的存留期內變更剪輯矩形的維度，請使用靜態矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-134">Use a static rectangle if you do not need to change the dimensions of the clip rectangle during the lifetime of the visual.</span></span> <span data-ttu-id="d7427-135">如果您需要變更維度或以動畫顯示剪輯矩形，請使用剪輯物件。</span><span class="sxs-lookup"><span data-stu-id="d7427-135">If you do need to change the dimensions or animate the clip rectangle, use a clip object.</span></span>

## <a name="clip-object"></a><span data-ttu-id="d7427-136">剪輯物件</span><span class="sxs-lookup"><span data-stu-id="d7427-136">Clip object</span></span>

<span data-ttu-id="d7427-137">剪輯物件是元件物件模型， (COM) 物件，代表剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-137">A clip object is a Component Object Model (COM) object that represents a clip rectangle.</span></span> <span data-ttu-id="d7427-138">您可以使用 [**IDCompositionDevice：： CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) 方法建立剪輯物件，然後使用物件的 [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) 介面來設定物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7427-138">You create a clip object by using the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method, and then use the object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the object.</span></span> <span data-ttu-id="d7427-139">新建立的剪輯物件具有左方和頂端屬性的最小可能值，以及右邊和底部屬性的最大可能值，有效地使其成為無作業的剪輯物件。</span><span class="sxs-lookup"><span data-stu-id="d7427-139">A newly created clip object has the minimum possible values for the Left and Top properties, and the maximum possible values for the Right and Bottom properties, effectively making it a no-op clip object.</span></span> <span data-ttu-id="d7427-140">換句話說，物件代表的是包含視覺效果整個點陣圖內容的剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-140">In other words, the object represents a clip rectangle that would include the entire bitmap content of a visual.</span></span>

<span data-ttu-id="d7427-141">剪輯物件包含一組屬性，可讓您指定剪輯物件的圓角。</span><span class="sxs-lookup"><span data-stu-id="d7427-141">A clip object includes a set of properties that enable you to specify rounded corners for the clip object.</span></span> <span data-ttu-id="d7427-142">屬性可讓您設定剪切物件每個角落的 x 半徑和 y 半徑。</span><span class="sxs-lookup"><span data-stu-id="d7427-142">The properties enable you to set the x radius and y radius of each corner of the clipping object.</span></span>

## <a name="animated-clip-rectangle"></a><span data-ttu-id="d7427-143">動畫裁剪矩形</span><span class="sxs-lookup"><span data-stu-id="d7427-143">Animated clip rectangle</span></span>

<span data-ttu-id="d7427-144">您可以藉由將動畫物件套用至剪輯物件的左邊、頂端、右邊和底部屬性，以動畫顯示剪輯矩形。</span><span class="sxs-lookup"><span data-stu-id="d7427-144">You can animate a clip rectangle by applying animation objects to the Left, Top, Right, and Bottom properties of a clip object.</span></span> <span data-ttu-id="d7427-145">使用 [**IDCompositionVisual：： SetClip (IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) 多載方法，以將動畫裁剪矩形套用至視覺效果的剪輯屬性。</span><span class="sxs-lookup"><span data-stu-id="d7427-145">Use the [**IDCompositionVisual::SetClip(IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) overloaded method to apply the animated clip rectangle to the Clip property of a visual.</span></span>

<span data-ttu-id="d7427-146">如需動畫物件的詳細資訊，請參閱 [動畫](animation.md)。</span><span class="sxs-lookup"><span data-stu-id="d7427-146">For more information about animation objects, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7427-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7427-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7427-148">DirectComposition 概念</span><span class="sxs-lookup"><span data-stu-id="d7427-148">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> <dt>

[<span data-ttu-id="d7427-149">如何使用矩形剪輯物件裁剪</span><span class="sxs-lookup"><span data-stu-id="d7427-149">How to Clip with a Rectangle Clip Object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
