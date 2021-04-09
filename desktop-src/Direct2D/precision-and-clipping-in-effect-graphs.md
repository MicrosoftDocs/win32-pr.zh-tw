---
title: 有效圖形中的有效位數和數位裁剪
description: 使用 Direct2D 轉譯效果的應用程式必須謹慎，才能達到所需的品質和可預測性（相對於數值有效位數）。
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90628661ec8cd3f16ff6a6149aecbb7e8be3e5a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023932"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a><span data-ttu-id="999c0-103">有效圖形中的有效位數和數位裁剪</span><span class="sxs-lookup"><span data-stu-id="999c0-103">Precision and numerical clipping in effect graphs</span></span>

<span data-ttu-id="999c0-104">使用 Direct2D 轉譯效果的應用程式必須謹慎，才能達到所需的品質和可預測性（相對於數值有效位數）。</span><span class="sxs-lookup"><span data-stu-id="999c0-104">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <span data-ttu-id="999c0-105">本主題說明 Direct2D 中的最佳作法和相關設定，這些設定在下列情況下很有用：</span><span class="sxs-lookup"><span data-stu-id="999c0-105">This topic describes best practices and relevant settings in Direct2D which are useful if:</span></span>

-   <span data-ttu-id="999c0-106">您的效果圖形依賴高數值有效位數或 \[ 0 （1）範圍以外的色彩 \] ，而您想要確保這些都能隨時可用</span><span class="sxs-lookup"><span data-stu-id="999c0-106">Your effect graph relies on high numerical precision or colors outside of the \[0, 1\] range, and you want to make sure these will always be available</span></span>
-   <span data-ttu-id="999c0-107">或者，您的效果圖形依賴轉譯程式來將中繼色彩夾具至 \[ 0，1個 \] 範圍，而且您想要確保此固定一律會發生</span><span class="sxs-lookup"><span data-stu-id="999c0-107">Or, your effect graph relies on the rendering implementation to clamp intermediate colors to the \[0, 1\] range, and you want to ensure this clamping always occurs</span></span>

<span data-ttu-id="999c0-108">Direct2D 通常會將效果圖形分成各區段，並在個別的步驟中轉譯每個區段。</span><span class="sxs-lookup"><span data-stu-id="999c0-108">Direct2D often divides an effect graph into sections, and renders each section in a separate step.</span></span> <span data-ttu-id="999c0-109">某些步驟的輸出可能會儲存在中繼 Direct3D 紋理中，依預設會有有限的數值範圍和精確度。</span><span class="sxs-lookup"><span data-stu-id="999c0-109">The output of some steps may be stored in intermediate Direct3D textures which by default have limited numerical range and precision.</span></span> <span data-ttu-id="999c0-110">Direct2D 不會保證是否使用這些中繼紋理。</span><span class="sxs-lookup"><span data-stu-id="999c0-110">Direct2D makes no guarantees about if or where these intermediate textures are used.</span></span> <span data-ttu-id="999c0-111">此行為可能會根據 GPU 功能以及 Windows 版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="999c0-111">This behavior may vary according to GPU capabilities as well as between Windows versions.</span></span>

<span data-ttu-id="999c0-112">在 Windows 10 中，Direct2D 會使用較少的中繼紋理，因為它使用著色器連結。</span><span class="sxs-lookup"><span data-stu-id="999c0-112">In Windows 10, Direct2D uses fewer intermediate textures due to its use of shader linking.</span></span> <span data-ttu-id="999c0-113">因此，Direct2D 可能會產生與先前 Windows 版本中的預設設定不同的結果。</span><span class="sxs-lookup"><span data-stu-id="999c0-113">Direct2D may therefore produce different results with default settings than in prior Windows releases.</span></span> <span data-ttu-id="999c0-114">這主要會影響著色器連結可能在效果圖形中的案例，而該圖表也包含產生擴充範圍輸出色彩的效果。</span><span class="sxs-lookup"><span data-stu-id="999c0-114">This primarily affects scenarios where shader linking is possible in an effect graph, and that graph also contains effects that produce extended-range output colors.</span></span>

## <a name="overview-of-effect-rendering-and-intermediates"></a><span data-ttu-id="999c0-115">效果轉譯和中繼的總覽</span><span class="sxs-lookup"><span data-stu-id="999c0-115">Overview of effect rendering and intermediates</span></span>

<span data-ttu-id="999c0-116">為了呈現效果圖形，Direct2D 會先尋找「轉換」的基礎圖形，其中的轉換是在效果中使用的圖形節點。</span><span class="sxs-lookup"><span data-stu-id="999c0-116">To render an effect graph, Direct2D first finds the underlying graph of “transforms,” where a transform is a graph node used within an effect.</span></span> <span data-ttu-id="999c0-117">有不同類型的轉換，包括提供 Direct3D 著色器供 Direct2D 使用。</span><span class="sxs-lookup"><span data-stu-id="999c0-117">There are different types of transforms, including those which provide Direct3D shaders for Direct2D to use.</span></span>

<span data-ttu-id="999c0-118">例如，Direct2D 可能會轉譯效果圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="999c0-118">For example, Direct2D may render an effect graph as follows:</span></span>

![具有中繼紋理的效果圖表](images/precision-and-clipping-1.png)

<span data-ttu-id="999c0-120">Direct2D 會尋找機會減少用來呈現效果圖形的數位中繼紋理;此邏輯對應用程式而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="999c0-120">Direct2D looks for opportunities to reduce the number intermediate textures used to render the effect graph; this logic is opaque to applications.</span></span> <span data-ttu-id="999c0-121">例如，您可以使用單一 Direct3D draw 呼叫和沒有中繼紋理來 Direct2D 轉譯下圖：</span><span class="sxs-lookup"><span data-stu-id="999c0-121">For example, the following graph can be rendered by Direct2D using one Direct3D draw call and no intermediate textures:</span></span>

![沒有中繼紋理的效果圖表](images/precision-and-clipping-2.png)

<span data-ttu-id="999c0-123">在 Windows 10 之前，如果在相同效果圖形中使用多個圖元著色器，Direct2D 一律會使用中繼紋理。</span><span class="sxs-lookup"><span data-stu-id="999c0-123">Prior to Windows 10, Direct2D would always use intermediate textures if multiple pixels shaders were used within the same effect graph.</span></span> <span data-ttu-id="999c0-124">大部分的內建效果，只要調整色彩值 (例如亮度或飽和度，) 使用圖元著色器來進行。</span><span class="sxs-lookup"><span data-stu-id="999c0-124">Most built-in effects that simply adjust color values (for example, Brightness or Saturation) do so using pixel shaders.</span></span>

<span data-ttu-id="999c0-125">在 Windows 10 中，Direct2D 現在可以避免在這種情況下使用中繼紋理。</span><span class="sxs-lookup"><span data-stu-id="999c0-125">In Windows 10, Direct2D may now avoid using intermediate textures in such cases.</span></span> <span data-ttu-id="999c0-126">其運作方式是在內部連結連續的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="999c0-126">It does this by internally linking adjacent pixel shaders.</span></span> <span data-ttu-id="999c0-127">例如：</span><span class="sxs-lookup"><span data-stu-id="999c0-127">For example:</span></span>

![具有多個圖元著色器且沒有中繼材質的 windows 10 效果圖形](images/precision-and-clipping-3.png)

<span data-ttu-id="999c0-129">請注意，圖表中並非所有連續的圖元著色器都可以連結在一起，因此只有特定圖形會在 Windows 10 上產生不同的輸出。</span><span class="sxs-lookup"><span data-stu-id="999c0-129">Note that not all adjacent pixel shaders in a graph may be linked together, and therefore only certain graphs will produce different output on Windows 10.</span></span> <span data-ttu-id="999c0-130">如需完整的詳細資訊，請參閱 [效果著色器連結](effect-shader-linking.md)。</span><span class="sxs-lookup"><span data-stu-id="999c0-130">For full details see [Effect Shader Linking](effect-shader-linking.md).</span></span> <span data-ttu-id="999c0-131">主要限制如下：</span><span class="sxs-lookup"><span data-stu-id="999c0-131">The primary restrictions are:</span></span>

-   <span data-ttu-id="999c0-132">如果第一個效果是連接到多個效果的輸入，則效果將不會與使用其輸出的效果相連結。</span><span class="sxs-lookup"><span data-stu-id="999c0-132">An effect will not be linked with effects consuming its output, if the first effect is connected as an input to multiple effects.</span></span>
-   <span data-ttu-id="999c0-133">如果第一個效果將其輸入的輸入在不同的邏輯位置（而非其輸出），效果將不會與效果集合連結做為其輸入。</span><span class="sxs-lookup"><span data-stu-id="999c0-133">An effect will not be linked with an effect set as its input, if the first effect samples its input at a different logical position than its output.</span></span> <span data-ttu-id="999c0-134">例如，色彩矩陣效果可能會與其輸入連結，但不會有卷積效果。</span><span class="sxs-lookup"><span data-stu-id="999c0-134">For example, a Color Matrix effect might be linked with its input, but a Convolution effect will not be.</span></span>

## <a name="built-in-effect-behavior"></a><span data-ttu-id="999c0-135">內建效果行為</span><span class="sxs-lookup"><span data-stu-id="999c0-135">Built-in effect behavior</span></span>

<span data-ttu-id="999c0-136">許多內建效果可能會 \[ 在 unpremultiplied 色彩空間中的0（1）之外產生色彩 \] ，即使它們的輸入色彩在該範圍內也一樣。</span><span class="sxs-lookup"><span data-stu-id="999c0-136">Many built-in effects may produce colors outside of the \[0, 1\] range in the unpremultiplied color space, even when their input colors are within that range.</span></span> <span data-ttu-id="999c0-137">發生這種情況時，這類色彩可能會受到數位裁剪的影響。</span><span class="sxs-lookup"><span data-stu-id="999c0-137">When this happens, such colors may be subject to numerical clipping.</span></span> <span data-ttu-id="999c0-138">請注意，即使內建效果通常會在預乘空間中產生色彩，但請務必考慮 unpremultiplied 空間中的色彩範圍。</span><span class="sxs-lookup"><span data-stu-id="999c0-138">Note that it’s important to consider the color range in unpremultiplied space, even though built-in effects typically produce colors in premultiplied space.</span></span> <span data-ttu-id="999c0-139">這可確保色彩維持在範圍內，即使其他效果接著 unpremultiply 它們也是如此。</span><span class="sxs-lookup"><span data-stu-id="999c0-139">This ensures that colors stay within range, even if other effects subsequently unpremultiply them.</span></span>

<span data-ttu-id="999c0-140">可能會發出這些超出範圍色彩的某些效果會提供 "ClampOutput" 屬性。</span><span class="sxs-lookup"><span data-stu-id="999c0-140">Some of the effects which may emit these out-of-range colors offer a “ClampOutput” property.</span></span> <span data-ttu-id="999c0-141">這些包括：</span><span class="sxs-lookup"><span data-stu-id="999c0-141">These include:</span></span>

-   [<span data-ttu-id="999c0-142">色彩矩陣</span><span class="sxs-lookup"><span data-stu-id="999c0-142">Color Matrix</span></span>](color-matrix.md)
-   [<span data-ttu-id="999c0-143">算術複合</span><span class="sxs-lookup"><span data-stu-id="999c0-143">Arithmetic Composite</span></span>](arithmetic-composite.md)
-   [<span data-ttu-id="999c0-144">>convolve</span><span class="sxs-lookup"><span data-stu-id="999c0-144">Convolve</span></span>](convolve-matrix.md)
-   [<span data-ttu-id="999c0-145">傳送效果</span><span class="sxs-lookup"><span data-stu-id="999c0-145">Transfer effects</span></span>](built-in-effects.md)

<span data-ttu-id="999c0-146">在這些效果上將 ClampOutput 屬性設定為 TRUE，可確保不論是否有著色器連結等因素，都能達成一致的結果。</span><span class="sxs-lookup"><span data-stu-id="999c0-146">Setting the ClampOutput property to TRUE on these effects ensures a consistent result will be achieved regardless of factors such as shader linking.</span></span> <span data-ttu-id="999c0-147">請注意，固定會發生在 unpremultiplied 空間中。</span><span class="sxs-lookup"><span data-stu-id="999c0-147">Note that clamping occurs in unpremultiplied space.</span></span>

<span data-ttu-id="999c0-148">其他內建效果也可能會產生超出0的輸出色彩 \[ ， \] unpremultiplied 空間中的1個範圍，即使在該範圍內有任何) ，也可能會產生色彩圖元 (和 "Color" 屬性。</span><span class="sxs-lookup"><span data-stu-id="999c0-148">Other built-in effects may also produce output colors beyond the \[0, 1\] range in unpremultiplied space, even when their colors pixels (and “Color” properties if any) are within that range.</span></span> <span data-ttu-id="999c0-149">這些包括：</span><span class="sxs-lookup"><span data-stu-id="999c0-149">These include:</span></span>

-   <span data-ttu-id="999c0-150">在插補模式屬性為立方或高品質的三種情況下， ([轉換和調整效果](built-in-effects.md)) </span><span class="sxs-lookup"><span data-stu-id="999c0-150">[Transforming and Scaling effects](built-in-effects.md) (When the Interpolation Mode property is Cubic or High Quality Cubic)</span></span>
-   [<span data-ttu-id="999c0-151">光源效果</span><span class="sxs-lookup"><span data-stu-id="999c0-151">Lighting effects</span></span>](built-in-effects.md)
-   <span data-ttu-id="999c0-152">覆迭邊緣屬性為 TRUE 時， [Edge 偵測](edge-detection-effect.md) () </span><span class="sxs-lookup"><span data-stu-id="999c0-152">[Edge detection](edge-detection-effect.md) (When the Overlay Edges property is TRUE)</span></span>
-   [<span data-ttu-id="999c0-153">曝光</span><span class="sxs-lookup"><span data-stu-id="999c0-153">Exposure</span></span>](exposure-effect.md)
-   <span data-ttu-id="999c0-154">當 Mode 屬性為加號時，[複合](composite.md) () </span><span class="sxs-lookup"><span data-stu-id="999c0-154">[Composite](composite.md) (When the Mode property is Plus)</span></span>
-   [<span data-ttu-id="999c0-155">溫度和色調</span><span class="sxs-lookup"><span data-stu-id="999c0-155">Temperature and Tint</span></span>](temperature-and-tint-effect.md)
-   [<span data-ttu-id="999c0-156">懷舊</span><span class="sxs-lookup"><span data-stu-id="999c0-156">Sepia</span></span>](sepia-effect.md)
-   [<span data-ttu-id="999c0-157">飽和度</span><span class="sxs-lookup"><span data-stu-id="999c0-157">Saturation</span></span>](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a><span data-ttu-id="999c0-158">在效果圖形內強制進行數位裁剪</span><span class="sxs-lookup"><span data-stu-id="999c0-158">Forcing numerical clipping within an effect graph</span></span>

<span data-ttu-id="999c0-159">使用上方所列的效果沒有 ClampOutput 屬性時，應用程式應該考慮強制執行數值固定。</span><span class="sxs-lookup"><span data-stu-id="999c0-159">While using effects listed above which do not have a ClampOutput property, applications should consider forcing numerical clamping.</span></span> <span data-ttu-id="999c0-160">這可以藉由在圖形中插入個其圖元的額外效果來完成。</span><span class="sxs-lookup"><span data-stu-id="999c0-160">This can be done by inserting an additional effect into the graph that clamps its pixels.</span></span> <span data-ttu-id="999c0-161">您可以使用色彩矩陣效果，並將其 ' ClampOutput ' 屬性設定為 TRUE，並將 ' ColorMatrix ' 屬性保留為預設 (傳遞) 值。</span><span class="sxs-lookup"><span data-stu-id="999c0-161">A Color Matrix effect may be used, with its ‘ClampOutput’ property set to TRUE and leaving the ‘ColorMatrix’ property as the default (pass-through) value.</span></span>

<span data-ttu-id="999c0-162">達到一致結果的第二個選項，是要求 Direct2D 使用具有較高精確度的中繼紋理。</span><span class="sxs-lookup"><span data-stu-id="999c0-162">A second option to achieve consistent results is to request that Direct2D use intermediate textures which have greater precision.</span></span> <span data-ttu-id="999c0-163">如下所述。</span><span class="sxs-lookup"><span data-stu-id="999c0-163">This is described below.</span></span>

## <a name="controlling-precision-of-intermediate-textures"></a><span data-ttu-id="999c0-164">控制中繼紋理的精確度</span><span class="sxs-lookup"><span data-stu-id="999c0-164">Controlling precision of intermediate textures</span></span>

<span data-ttu-id="999c0-165">Direct2D 提供數種方式來控制圖形的精確度。</span><span class="sxs-lookup"><span data-stu-id="999c0-165">Direct2D provides a few ways to control the precision of a graph.</span></span> <span data-ttu-id="999c0-166">在 Direct2D 中使用高精確度格式之前，應用程式必須確定 GPU 可充分支援這些格式。</span><span class="sxs-lookup"><span data-stu-id="999c0-166">Before using high precision formats in Direct2D, applications must ensure they are supported sufficiently by the GPU.</span></span> <span data-ttu-id="999c0-167">若要檢查這一點，請使用 [**ID2D1DeviceCoNtext：： IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported)。</span><span class="sxs-lookup"><span data-stu-id="999c0-167">To check this, use [**ID2D1DeviceContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).</span></span>

<span data-ttu-id="999c0-168">應用程式可以使用變形 (軟體模擬) 來建立 Direct3D 裝置，以保證所有緩衝區精確度都支援獨立于裝置上的實際 GPU 硬體。</span><span class="sxs-lookup"><span data-stu-id="999c0-168">Applications may create a Direct3D device using WARP (software emulation) to guarantee that all buffer precisions are supported independent of the actual GPU hardware on the device.</span></span> <span data-ttu-id="999c0-169">這在儲存至磁片的情況下，建議您將效果套用到相片。</span><span class="sxs-lookup"><span data-stu-id="999c0-169">This is recommended in scenarios such as applying effects to a photo while saving to disk.</span></span> <span data-ttu-id="999c0-170">即使 Direct2D 在 GPU 上支援高精確度的緩衝區格式，在此案例中，建議在功能層級6.x 的 Gpu 上使用變形，因為著色器算術的精確度有限，並取樣一些低功率行動 Gpu。</span><span class="sxs-lookup"><span data-stu-id="999c0-170">Even if Direct2D supports high precision buffer formats on the GPU, using WARP is recommended in this scenario on feature level 9.X GPUs, due to the limited precision of shader arithmetic and sampling on some low-power mobile GPUs.</span></span>

<span data-ttu-id="999c0-171">在以下每個案例中，所要求的精確度實際上是 Direct2D 將使用的最小有效位數。</span><span class="sxs-lookup"><span data-stu-id="999c0-171">In each case below, the requested precision is actually the minimum precision Direct2D will use.</span></span> <span data-ttu-id="999c0-172">如果不需要中繼，則可以使用較高的有效位數。</span><span class="sxs-lookup"><span data-stu-id="999c0-172">Higher precision may be used if intermediates are not required.</span></span> <span data-ttu-id="999c0-173">Direct2D 可能也會共用相同圖表的不同部分或完全不同圖形的中繼紋理。</span><span class="sxs-lookup"><span data-stu-id="999c0-173">Direct2D may also share intermediate textures for different parts of the same graph or different graphs entirely.</span></span> <span data-ttu-id="999c0-174">在此情況下，Direct2D 會使用針對所有相關作業要求的最大精確度。</span><span class="sxs-lookup"><span data-stu-id="999c0-174">In this case Direct2D uses the maximum precision requested for all involved operations.</span></span>

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a><span data-ttu-id="999c0-175">從 ID2D1DeviceCoNtext：： SetRenderingControls 的精確度選取範圍</span><span class="sxs-lookup"><span data-stu-id="999c0-175">Precision selection from ID2D1DeviceContext::SetRenderingControls</span></span>

<span data-ttu-id="999c0-176">控制 Direct2d 中繼材質精確度的最簡單方式是使用 [**ID2D1DeviceCoNtext：： SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))。</span><span class="sxs-lookup"><span data-stu-id="999c0-176">The simplest way to control the precision of Direct2D’s intermediate textures is to use [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)).</span></span> <span data-ttu-id="999c0-177">這會控制所有中繼紋理的精確度，只要不是手動手動設定效果或轉換的精確度也一樣。</span><span class="sxs-lookup"><span data-stu-id="999c0-177">This controls the precision of all intermediate textures, as long as a precision is not also set manually on effects or transforms directly.</span></span>


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a><span data-ttu-id="999c0-178">輸入和轉譯目標的精確度選取範圍</span><span class="sxs-lookup"><span data-stu-id="999c0-178">Precision selection from inputs and render targets</span></span>

<span data-ttu-id="999c0-179">應用程式可能也會依賴效果圖形輸入的精確度，來控制中繼紋理的精確度。</span><span class="sxs-lookup"><span data-stu-id="999c0-179">Applications may also rely on the precision of the inputs to an effect graph to control the precision of intermediate textures.</span></span> <span data-ttu-id="999c0-180">只要沒有使用 [**ID2D1DeviceCoNtext：： SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))指定緩衝區有效位數，而且不會直接在效果和轉換上手動設定，就會有這種情況。</span><span class="sxs-lookup"><span data-stu-id="999c0-180">This is true as long as a buffer precision is not specified using [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)), and is not set manually on effects and transform directly.</span></span>

<span data-ttu-id="999c0-181">效果的輸入精確度會透過圖形傳播，以選取下游中繼的精確度。</span><span class="sxs-lookup"><span data-stu-id="999c0-181">The precisions of inputs to effects are propagated through the graph to select the precision of downstream intermediates.</span></span> <span data-ttu-id="999c0-182">當效果圖形中的不同分支符合時，就會使用任何輸入的最大有效位數。</span><span class="sxs-lookup"><span data-stu-id="999c0-182">Where different branches in the effect graph meet, the greatest precision of any input is used.</span></span>

<span data-ttu-id="999c0-183">根據 Direct2D 點陣圖所選取的有效位數取決於其像素格式。</span><span class="sxs-lookup"><span data-stu-id="999c0-183">The precision selected based on a Direct2D bitmap is determined from its pixel format.</span></span> <span data-ttu-id="999c0-184">針對 [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) 所選取的精確度，是由用來建立 **ID2D1ImageSource** 之基礎 IWICBitmapSource 的 WIC 像素格式所決定。</span><span class="sxs-lookup"><span data-stu-id="999c0-184">The precision selected for an [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) is determined from the WIC pixel format of the underlying IWICBitmapSource used to create the **ID2D1ImageSource**.</span></span> <span data-ttu-id="999c0-185">請注意，Direct2D 不允許使用 Direct2D 和 GPU 不支援的精確度來建立具有 WIC 來源的影像來源。</span><span class="sxs-lookup"><span data-stu-id="999c0-185">Note that Direct2D doesn’t allow image sources to be created with WIC sources using precisions unsupported by Direct2D and the GPU.</span></span>

<span data-ttu-id="999c0-186">Direct2D 無法根據輸入來指派有效位數的有效位數。</span><span class="sxs-lookup"><span data-stu-id="999c0-186">It is possible that Direct2D cannot assign an effect a precision based on its inputs.</span></span> <span data-ttu-id="999c0-187">當效果沒有任何輸入，或使用 [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) 時（沒有特定精確度），就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="999c0-187">This happens when an effect has no inputs, or when an [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) is used, which has no specific precision.</span></span> <span data-ttu-id="999c0-188">在此情況下，中繼紋理的有效位數是由點陣圖集合中的內容目前轉譯目標所決定。</span><span class="sxs-lookup"><span data-stu-id="999c0-188">In this case, the precision of intermediate textures is determined from the bitmap set as the context’s current render target.</span></span>

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a><span data-ttu-id="999c0-189">直接在效果和轉換上選取精確度</span><span class="sxs-lookup"><span data-stu-id="999c0-189">Precision selection directly on the effect and transforms</span></span>

<span data-ttu-id="999c0-190">您也可以在效果圖形中的明確位置設定中繼紋理的最小有效位數。</span><span class="sxs-lookup"><span data-stu-id="999c0-190">The minimum precision for intermediate textures may also be set at explicit locations within an effect graph.</span></span> <span data-ttu-id="999c0-191">這只建議用於 advanced 案例。</span><span class="sxs-lookup"><span data-stu-id="999c0-191">This is only recommended for advanced scenarios.</span></span>

<span data-ttu-id="999c0-192">您可以使用效果上的屬性來設定最小有效位數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="999c0-192">The minimum precision may be set using a property on an effect as follows:</span></span>


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



<span data-ttu-id="999c0-193">在效果的執行中，可以使用 ID2D1RenderInfo：： SetOutputPrecision 來設定最小有效位數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="999c0-193">Within an effect implementation, the minimum precision may be set using ID2D1RenderInfo::SetOutputPrecision as follows:</span></span>


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



<span data-ttu-id="999c0-194">請注意，在效果上設定的有效位數會傳播至相同效果圖形中的下游效果，除非這些下游效果設定了不同的精確度。</span><span class="sxs-lookup"><span data-stu-id="999c0-194">Note that the precision set on an effect will propagate to downstream effects in the same effect graph, unless a different precision is set on those downstream effects.</span></span> <span data-ttu-id="999c0-195">在效果內轉換中設定的有效位數不會影響下游轉換節點的有效位數。</span><span class="sxs-lookup"><span data-stu-id="999c0-195">The precision set on a transform within an effect does not affect the precision for downstream transform nodes.</span></span>

<span data-ttu-id="999c0-196">以下是完整的遞迴邏輯，用來判斷儲存指定轉換節點輸出之中繼緩衝區的最小有效位數：</span><span class="sxs-lookup"><span data-stu-id="999c0-196">Below is the full recursive logic used to determine the minimum precision for an intermediate buffer storing the output of a given transform node:</span></span>

![中繼緩衝區的最小精確度邏輯](images/precision-and-clipping-4.png)

 

 