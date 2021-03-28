---
title: 功能等級9硬體上的使用者剪輯平面
description: 從 Windows 8 開始，Microsoft 高階著色器語言 (HLSL) 支援可搭配 Microsoft Direct3D 11 API 使用的語法，以在功能層級 9 \_ x 和更高版本上指定使用者剪輯平面。
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315571"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="eaaf7-103">功能等級9硬體上的使用者剪輯平面</span><span class="sxs-lookup"><span data-stu-id="eaaf7-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="eaaf7-104">從 Windows 8 開始，Microsoft 高階著色器語言 (HLSL) 支援可搭配 Microsoft Direct3D 11 API 使用的語法，以在 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x 和更高版本上指定使用者剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="eaaf7-105">您可以使用這個剪切平面語法來寫入著色器，然後使用該著色器物件搭配 Direct3D 11 API，以在所有 Direct3D 功能層級上執行。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="eaaf7-106">背景</span><span class="sxs-lookup"><span data-stu-id="eaaf7-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="eaaf7-107">語法</span><span class="sxs-lookup"><span data-stu-id="eaaf7-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="eaaf7-108">在功能層級9和更高的剪輯空間中建立剪輯平面</span><span class="sxs-lookup"><span data-stu-id="eaaf7-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="eaaf7-109">背景讀取</span><span class="sxs-lookup"><span data-stu-id="eaaf7-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="eaaf7-110">10Level9 功能等級</span><span class="sxs-lookup"><span data-stu-id="eaaf7-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="eaaf7-111">裁剪平面數學</span><span class="sxs-lookup"><span data-stu-id="eaaf7-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="eaaf7-112">在視圖空間中裁剪</span><span class="sxs-lookup"><span data-stu-id="eaaf7-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="eaaf7-113">投射矩陣</span><span class="sxs-lookup"><span data-stu-id="eaaf7-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="eaaf7-114">剪輯空間裁剪平面</span><span class="sxs-lookup"><span data-stu-id="eaaf7-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="eaaf7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="eaaf7-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="eaaf7-116">背景</span><span class="sxs-lookup"><span data-stu-id="eaaf7-116">Background</span></span>

<span data-ttu-id="eaaf7-117">您可以透過 [**IDirect3DDevice9：： SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) 和 [**IDirect3DDevice9：： GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) 方法，在 Microsoft Direct3D 9 API 中存取使用者剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="eaaf7-118">在 Microsoft Direct3D 10 和更新版本中，您可以透過 [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) 語義來存取使用者剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="eaaf7-119">但在 Windows 8 之前， \_ direct3d 10 或 direct3d 11 api 中的 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x 硬體無法使用 SV ClipDistance \_ 。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="eaaf7-120">因此，在 Windows 8 之前，使用功能層級 9 x 硬體來存取使用者剪輯平面的唯一方法 \_ 是透過 Direct3D 9 API。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="eaaf7-121">Direct3D Windows Store 應用程式無法使用 Direct3D 9 API。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="eaaf7-122">在這裡，我們將說明您可以在功能層級 9 \_ x 和更高版本上透過 Direct3D 11 API 存取使用者剪輯平面的語法。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="eaaf7-123">應用程式會使用「剪輯」平面來定義3D 世界內的一組隱藏的平面， (擲出) 所有繪製的基本專案。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="eaaf7-124">Windows 不會繪製任何裁剪平面之負角的任何圖元。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="eaaf7-125">然後，應用程式可以使用剪輯平面來呈現平面反射。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaaf7-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaaf7-126">Syntax</span></span>

<span data-ttu-id="eaaf7-127">使用此語法可將剪輯平面宣告為 [函式宣告](dx-graphics-hlsl-function-syntax.md)中的函式屬性。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="eaaf7-128">例如，我們在這裡使用頂點著色器片段上的語法：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

<span data-ttu-id="eaaf7-129">這是頂點著色器片段的範例，表示兩個裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="eaaf7-130">它會顯示您需要將新的 **clipplanes** 屬性放在括弧內的括弧內，緊接在頂點著色器的傳回值之前。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="eaaf7-131">在 **clipplanes** 屬性之後的括弧內，您可以提供最多6個 **float4** 常數的清單，以定義每個使用中剪輯平面的平面係數。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="eaaf7-132">此範例也顯示您需要讓每個平面的係數都位於常數緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="eaaf7-133">沒有可動態停用剪切平面的語法。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="eaaf7-134">您必須重新編譯沒有 **clipplanes** 屬性的另一個相同著色器，否則您的應用程式可以將常數緩衝區中的係數設定為零，如此平面就不會再影響任何幾何。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="eaaf7-135">此語法適用于任何4.0 或更新版本的頂點著色器目標，其中包括 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 1 和 vs \_ 4 \_ 0 \_ 層級 \_ 9 \_ 3。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="eaaf7-136">在功能層級9和更高的剪輯空間中建立剪輯平面</span><span class="sxs-lookup"><span data-stu-id="eaaf7-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="eaaf7-137">在這裡，我們將示範如何在 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x 和更高的剪輯空間中建立剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="eaaf7-138">背景讀取</span><span class="sxs-lookup"><span data-stu-id="eaaf7-138">Background reading</span></span>

<span data-ttu-id="eaaf7-139">「使用 DirectX 10 進行3D 遊戲程式設計簡介」。 Luna 將說明您需要的圖形數學背景 (第1、2和 3) ，以及在頂點著色器中發生的各種空間和空間轉換 (區段5.6 和 5.8) 。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="eaaf7-140">10Level9 功能等級</span><span class="sxs-lookup"><span data-stu-id="eaaf7-140">10Level9 feature levels</span></span>

<span data-ttu-id="eaaf7-141">在 Direct3D 10 和更新版本中，您可以裁剪任何有意義的空間，通常是在世界空間或視野空間中。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="eaaf7-142">但是，Direct3D 9 會使用剪輯空間，也就是在分割投影空間之前的觀點。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="eaaf7-143">當頂點著色器將這些向量傳遞給 [圖形管線](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)中後續的階段時，它們會在剪輯空間中。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="eaaf7-144">當您撰寫 Windows Store 應用程式時，您必須使用10Level9 功能等級 ([功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) ，讓應用程式可以在功能層級 9 \_ x 和更高的硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="eaaf7-145">因為您的應用程式支援功能層級 9 \_ x 和更高版本，所以您也必須使用在剪輯空間中套用剪輯平面的一般功能。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="eaaf7-146">當您使用 vs \_ 4 \_ 0 \_ 層級 9 1 或更新版本來編譯頂點著色器時 \_ \_ ，該頂點著色器可以使用 **clipplanes** 屬性。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="eaaf7-147">Direct3D 10 或更新版本的物件具有發出頂點的點乘積，其中包含屬性中指定的每個 **float4** 全域常數。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="eaaf7-148">Direct3D 9 物件有足夠的中繼資料，可讓10Level9 執行時間發出適當的 [**IDirect3DDevice9：： SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane)呼叫。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="eaaf7-149">裁剪平面數學</span><span class="sxs-lookup"><span data-stu-id="eaaf7-149">Clip plane math</span></span>

<span data-ttu-id="eaaf7-150">剪輯平面是由具有4個元件的向量所定義。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="eaaf7-151">前三個元件會定義 x、y、z 向量，以從我們想要裁剪的空間中的原點 emanates。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="eaaf7-152">此向量表示平面，垂直至向量並透過原點執行。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="eaaf7-153">Windows 會將所有圖元保留在平面的向量端，並將所有圖元剪到平面後方。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="eaaf7-154">第四個元件會將平面推回，並讓 Windows 更少 (負面 w 會導致視窗沿著向量線裁剪更) 。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="eaaf7-155">如果 x、y、z 元件 (正規化) 向量來撰寫一個單位，則會將平面推回的平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="eaaf7-156">圖形處理器 (GPU) 執行以判斷裁剪的數學，是頂點向量 (x、y、z、1) 和裁剪平面向量之間的簡單點乘積。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="eaaf7-157">此數學運算會在裁剪平面向量上建立投射長度。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="eaaf7-158">負點產品會顯示要在平面裁剪端的頂點。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="eaaf7-159">在視圖空間中裁剪</span><span class="sxs-lookup"><span data-stu-id="eaaf7-159">Clipping in view space</span></span>

<span data-ttu-id="eaaf7-160">以下是視圖空間中的頂點：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-160">Here is our vertex in view space:</span></span>

![視圖空間中的頂點](images/vertex-clip.png)

<span data-ttu-id="eaaf7-162">以下是我們在視野空間中的剪輯平面：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-162">Here is our clip plane in view space:</span></span>

![視圖空間中的剪切平面](images/clip-plane-view.png)

<span data-ttu-id="eaaf7-164">以下是頂點的點乘積和查看空間中的剪切平面：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="eaaf7-165">ClipDistance = **v** ·**C**  = *v* ₓ *C* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="eaaf7-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="eaaf7-166">此數學運算適用于 Direct3D 10 或更新版本的物件，但不適用於 Direct3D 9 物件。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="eaaf7-167">針對 Direct3D 9，我們必須先在剪輯空間中進行投影轉換。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="eaaf7-168">投射矩陣</span><span class="sxs-lookup"><span data-stu-id="eaaf7-168">Projection matrix</span></span>

<span data-ttu-id="eaaf7-169">投射矩陣會將頂點從 view space 轉換 (其中原點是檢視器的眼睛、+ x 朝右、+ y 已啟動，而 + z 則是直接) 在剪輯空間中。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="eaaf7-170">投射矩陣準備硬體裁剪和 [點陣化階段](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage)的頂點。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="eaaf7-171">以下是標準的透視圖矩陣 (其他投射需要不同的數學) ：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="eaaf7-172">   視窗寬度/高度的 r 比例</span><span class="sxs-lookup"><span data-stu-id="eaaf7-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="eaaf7-173">*α*   視圖角度</span><span class="sxs-lookup"><span data-stu-id="eaaf7-173">*α*  viewing angle</span></span>  
<span data-ttu-id="eaaf7-174">   從檢視器到目前平面的 f 距離</span><span class="sxs-lookup"><span data-stu-id="eaaf7-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="eaaf7-175">   從檢視器到接近平面的距離</span><span class="sxs-lookup"><span data-stu-id="eaaf7-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="eaaf7-176">![投射矩陣](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="eaaf7-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="eaaf7-177">下一個矩陣是前一個矩陣的簡化版本。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="eaaf7-178">我們會將矩陣簡化，讓我們可以在稍後的矩陣乘法運算中使用。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![簡化的投射矩陣](images/projection-matrix2.png)

<span data-ttu-id="eaaf7-180">現在，我們將 view space 頂點轉換成具有矩陣乘積的剪切空間：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![矩陣相乘](images/matrix-multiply.png)

<span data-ttu-id="eaaf7-182">在我們的矩陣乘法運算中，我們的 x 和 y 元件只會稍微調整，但 z 和 w 元件的變化很大。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="eaaf7-183">我們的剪輯平面無法提供我們所需的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="eaaf7-184">剪輯空間裁剪平面</span><span class="sxs-lookup"><span data-stu-id="eaaf7-184">Clip space clip plane</span></span>

<span data-ttu-id="eaaf7-185">在這裡，我們想要建立一個具有剪輯空間頂點的點乘積的剪輯空間裁剪平面，讓我們擁有與 v ·相同的值。 在 [[查看空間](#clipping-in-view-space)] 區段的剪切中的 C。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![裁剪平面](images/clip-space-clip-plane.png)

<span data-ttu-id="eaaf7-187">**v** ·**C**  = **v P** ·**C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="eaaf7-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="eaaf7-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>c w v y v z c z c  +  \*\* <sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>P <sub>z</sub></sub>  +  *v*<sub>z</sub>z *c*<sub>p <sub>w</sub></sub></span><span class="sxs-lookup"><span data-stu-id="eaaf7-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="eaaf7-189">現在我們可以將頂點元件的前面數學運算分成四個不同的方程式：</span><span class="sxs-lookup"><span data-stu-id="eaaf7-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![剪輯平面產品的 x 頂點元件](images/clip-space-clip-plane-equ1.png)

![剪輯平面產品的 y 頂點元件](images/clip-space-clip-plane-equ2.png)

![剪輯平面產品的 w 頂點元件](images/clip-space-clip-plane-equ3.png)

![剪切平面產品的 z 頂點元件](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="eaaf7-194">我們的視圖空間裁剪平面和投射矩陣會衍生出來，並為我們提供剪輯空間裁剪平面。</span><span class="sxs-lookup"><span data-stu-id="eaaf7-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![剪輯空間裁剪平面](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="eaaf7-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="eaaf7-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaaf7-197">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="eaaf7-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="eaaf7-198">函式宣告語法</span><span class="sxs-lookup"><span data-stu-id="eaaf7-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 