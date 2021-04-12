---
title: DirectComposition 詞彙
description: 本主題定義 Microsoft DirectComposition 條款。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315565"
---
# <a name="directcomposition-glossary"></a><span data-ttu-id="b78c2-103">DirectComposition 詞彙</span><span class="sxs-lookup"><span data-stu-id="b78c2-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="b78c2-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="b78c2-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="b78c2-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="b78c2-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="b78c2-106">本主題定義 Microsoft DirectComposition 條款。</span><span class="sxs-lookup"><span data-stu-id="b78c2-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="b78c2-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**動畫函數**</span><span class="sxs-lookup"><span data-stu-id="b78c2-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-108">指定如何在一段時間內變更單一物件屬性值的結構。</span><span class="sxs-lookup"><span data-stu-id="b78c2-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**動畫物件**</span><span class="sxs-lookup"><span data-stu-id="b78c2-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-110">物件，表示用來建立另一個物件之屬性動畫的函式。</span><span class="sxs-lookup"><span data-stu-id="b78c2-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**動畫區段**</span><span class="sxs-lookup"><span data-stu-id="b78c2-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-112">動畫函數的基本計時定義;它們是建立更複雜和更高層級動畫函式的基本類型。</span><span class="sxs-lookup"><span data-stu-id="b78c2-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**背景緩衝區**</span><span class="sxs-lookup"><span data-stu-id="b78c2-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-114">應用程式可直接寫入的記憶體矩形。</span><span class="sxs-lookup"><span data-stu-id="b78c2-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="b78c2-115">背景緩衝區永遠不會直接顯示在監視器上。</span><span class="sxs-lookup"><span data-stu-id="b78c2-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**批**</span><span class="sxs-lookup"><span data-stu-id="b78c2-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-117">以原子方式處理的 DirectComposition 方法呼叫群組。</span><span class="sxs-lookup"><span data-stu-id="b78c2-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="b78c2-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-119">位於系統或視訊記憶體中的色彩緩衝區（不論有無 Alpha 色板）。</span><span class="sxs-lookup"><span data-stu-id="b78c2-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**框線模式**</span><span class="sxs-lookup"><span data-stu-id="b78c2-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-121">Microsoft DirectComposition 視覺效果的屬性，此屬性會影響點陣圖轉換時，點陣圖邊緣的組成方式，讓邊緣不會與整數座標組齊軸。</span><span class="sxs-lookup"><span data-stu-id="b78c2-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="b78c2-122">它也會影響在具有圓角的剪輯角落以及已轉換之剪輯邊緣的內容裁剪方式，讓邊緣與整數座標不對齊軸。</span><span class="sxs-lookup"><span data-stu-id="b78c2-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**剪輯物件**</span><span class="sxs-lookup"><span data-stu-id="b78c2-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-124">表示剪輯矩形的物件。</span><span class="sxs-lookup"><span data-stu-id="b78c2-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**裁剪矩形**</span><span class="sxs-lookup"><span data-stu-id="b78c2-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-126">一組座標，定義轉譯點陣圖時在螢幕上繪製的視覺效果點陣圖內容區域。</span><span class="sxs-lookup"><span data-stu-id="b78c2-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**斗篷**</span><span class="sxs-lookup"><span data-stu-id="b78c2-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-128">若要暫時防止桌面視窗管理員 (DWM) 將視窗繪製至顯示器。</span><span class="sxs-lookup"><span data-stu-id="b78c2-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="b78c2-129">應用程式通常會在 DirectComposition 使用組合中的視窗點陣圖時，遮蓋視窗。</span><span class="sxs-lookup"><span data-stu-id="b78c2-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**提交**</span><span class="sxs-lookup"><span data-stu-id="b78c2-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-131">將一批命令提交至 DirectCompositionDirectComposition 以進行處理。</span><span class="sxs-lookup"><span data-stu-id="b78c2-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**複合模式**</span><span class="sxs-lookup"><span data-stu-id="b78c2-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-133">有幾種方式可以將兩個位圖混合 (來源和目的地) ，以達成特定效果。</span><span class="sxs-lookup"><span data-stu-id="b78c2-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**組成**</span><span class="sxs-lookup"><span data-stu-id="b78c2-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-135">在應用程式 UI 中套用各種轉換、效果和動畫來產生預期的視覺效果結果，結合和操作的點陣圖集合。</span><span class="sxs-lookup"><span data-stu-id="b78c2-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**撰寫目標視窗**</span><span class="sxs-lookup"><span data-stu-id="b78c2-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-137">視覺化樹狀結構所系結的視窗，也是繪製產生的組合。</span><span class="sxs-lookup"><span data-stu-id="b78c2-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**影響**</span><span class="sxs-lookup"><span data-stu-id="b78c2-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-139">修改視覺化樹狀結構點陣圖如何進行柵格化的作業，通常是藉由套用圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="b78c2-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**效果群組**</span><span class="sxs-lookup"><span data-stu-id="b78c2-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-141">一組點陣圖效果，會一起套用以修改視覺效果子樹狀結構的點陣化。</span><span class="sxs-lookup"><span data-stu-id="b78c2-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**框架**</span><span class="sxs-lookup"><span data-stu-id="b78c2-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-143">組合引擎的反復專案，會產生視覺化樹狀結構的點陣化。</span><span class="sxs-lookup"><span data-stu-id="b78c2-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**前端緩衝區**</span><span class="sxs-lookup"><span data-stu-id="b78c2-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-145">由圖形介面卡轉譯並顯示在監視器上的記憶體矩形。</span><span class="sxs-lookup"><span data-stu-id="b78c2-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**插補模式**</span><span class="sxs-lookup"><span data-stu-id="b78c2-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-147">屬性，決定點陣圖在轉換時的組成方式，讓點陣圖中的圖元與螢幕上的圖元之間沒有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="b78c2-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**根視覺效果**</span><span class="sxs-lookup"><span data-stu-id="b78c2-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-149">視覺化樹狀結構中所有其他視覺效果的來源視覺效果。</span><span class="sxs-lookup"><span data-stu-id="b78c2-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**交換鏈**</span><span class="sxs-lookup"><span data-stu-id="b78c2-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-151">一或多個後置緩衝區的集合，可連續呈現給前端緩衝區</span><span class="sxs-lookup"><span data-stu-id="b78c2-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**表面**</span><span class="sxs-lookup"><span data-stu-id="b78c2-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-153">顯示記憶體的線性區域表示，通常位於顯示配接器的顯示記憶體中，雖然表面可以存在於系統記憶體中。</span><span class="sxs-lookup"><span data-stu-id="b78c2-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**變換**</span><span class="sxs-lookup"><span data-stu-id="b78c2-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-155">矩陣，表示二維或三維空間中的座標轉換。</span><span class="sxs-lookup"><span data-stu-id="b78c2-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**轉換群組**</span><span class="sxs-lookup"><span data-stu-id="b78c2-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-157">在套用至視覺效果之前，其矩陣會以集合中指定的順序相乘的轉換集合。</span><span class="sxs-lookup"><span data-stu-id="b78c2-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**視覺**</span><span class="sxs-lookup"><span data-stu-id="b78c2-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-159">物件，其中包含點陣圖物件的選擇性參考，以及決定點陣圖如何轉譯至螢幕的一組屬性。</span><span class="sxs-lookup"><span data-stu-id="b78c2-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**視覺物件**</span><span class="sxs-lookup"><span data-stu-id="b78c2-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-161">請參閱 [*視覺效果*](/windows)。</span><span class="sxs-lookup"><span data-stu-id="b78c2-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**視覺化子樹**</span><span class="sxs-lookup"><span data-stu-id="b78c2-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-163">視覺化樹狀結構的一部分，其中包含特定視覺效果及其所有子系和附屬視覺效果。</span><span class="sxs-lookup"><span data-stu-id="b78c2-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**視覺化樹狀結構**</span><span class="sxs-lookup"><span data-stu-id="b78c2-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-165">用來建立組合的視覺效果階層式集合。</span><span class="sxs-lookup"><span data-stu-id="b78c2-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="b78c2-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**無視窗交換鏈**</span><span class="sxs-lookup"><span data-stu-id="b78c2-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="b78c2-167">與 DirectComposition 視覺物件（而非視窗）相關聯的交換鏈。</span><span class="sxs-lookup"><span data-stu-id="b78c2-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 