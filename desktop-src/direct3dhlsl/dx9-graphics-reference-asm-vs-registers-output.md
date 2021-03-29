---
title: 輸出暫存器
description: 輸出暫存器
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990599"
---
# <a name="output-registers"></a><span data-ttu-id="df2a5-103">輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-103">Output Registers</span></span>

-   <span data-ttu-id="df2a5-104">頂點色彩暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-104">Vertex Color Register</span></span>
-   <span data-ttu-id="df2a5-105">霧化暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-105">Fog Register</span></span>
-   <span data-ttu-id="df2a5-106">位置 \_ 註冊</span><span class="sxs-lookup"><span data-stu-id="df2a5-106">Position\_Register</span></span>
-   <span data-ttu-id="df2a5-107">點 \_ 大小暫存器 \_</span><span class="sxs-lookup"><span data-stu-id="df2a5-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="df2a5-108">材質 \_ 座標 \_ 註冊</span><span class="sxs-lookup"><span data-stu-id="df2a5-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="df2a5-109">暫存器名稱的前面會加上小寫字母 o，表示輸出暫存器是僅限寫入的。</span><span class="sxs-lookup"><span data-stu-id="df2a5-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="df2a5-110">頂點色彩註冊-oD0、oD1</span><span class="sxs-lookup"><span data-stu-id="df2a5-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="df2a5-111">oD0 是擴散色彩註冊。</span><span class="sxs-lookup"><span data-stu-id="df2a5-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="df2a5-112">oD1 是反射色彩註冊。</span><span class="sxs-lookup"><span data-stu-id="df2a5-112">oD1 is the specular color register.</span></span> <span data-ttu-id="df2a5-113">OD0 值會插入，並寫入至輸入色彩暫存器 0 (v0) 的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="df2a5-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="df2a5-114">OD1 值會插入並寫入輸入色彩註冊1， (v1) 圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="df2a5-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="df2a5-115">如需圖元著色器色彩暫存器的詳細資訊，請參閱註冊程式。</span><span class="sxs-lookup"><span data-stu-id="df2a5-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="df2a5-116">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="df2a5-116">Vertex shader versions</span></span> | <span data-ttu-id="df2a5-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="df2a5-117">1\_1</span></span> | <span data-ttu-id="df2a5-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-118">2\_0</span></span> | <span data-ttu-id="df2a5-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-119">2\_sw</span></span> | <span data-ttu-id="df2a5-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="df2a5-120">2\_x</span></span> | <span data-ttu-id="df2a5-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-121">3\_0</span></span> | <span data-ttu-id="df2a5-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="df2a5-123">頂點色彩暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-123">Vertex Color Register</span></span>  | <span data-ttu-id="df2a5-124">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-124">x</span></span>    | <span data-ttu-id="df2a5-125">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-125">x</span></span>    | <span data-ttu-id="df2a5-126">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-126">x</span></span>     | <span data-ttu-id="df2a5-127">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="df2a5-128">霧化註冊-oFog</span><span class="sxs-lookup"><span data-stu-id="df2a5-128">Fog Register - oFog</span></span>

<span data-ttu-id="df2a5-129">輸出霧化值會註冊。</span><span class="sxs-lookup"><span data-stu-id="df2a5-129">The output fog value registers.</span></span> <span data-ttu-id="df2a5-130">值是要插入的霧化因數，然後路由傳送至霧化資料表。</span><span class="sxs-lookup"><span data-stu-id="df2a5-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="df2a5-131">只會使用霧化的純量 x 元件。</span><span class="sxs-lookup"><span data-stu-id="df2a5-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="df2a5-132">在傳遞至轉譯器之前，值會在零和1之間壓制。</span><span class="sxs-lookup"><span data-stu-id="df2a5-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="df2a5-133">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="df2a5-133">Vertex shader versions</span></span> | <span data-ttu-id="df2a5-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="df2a5-134">1\_1</span></span> | <span data-ttu-id="df2a5-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-135">2\_0</span></span> | <span data-ttu-id="df2a5-136">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-136">2\_sw</span></span> | <span data-ttu-id="df2a5-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="df2a5-137">2\_x</span></span> | <span data-ttu-id="df2a5-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-138">3\_0</span></span> | <span data-ttu-id="df2a5-139">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="df2a5-140">霧化暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-140">Fog Register</span></span>           | <span data-ttu-id="df2a5-141">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-141">x</span></span>    | <span data-ttu-id="df2a5-142">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-142">x</span></span>    | <span data-ttu-id="df2a5-143">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-143">x</span></span>     | <span data-ttu-id="df2a5-144">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="df2a5-145">位置註冊-oPos</span><span class="sxs-lookup"><span data-stu-id="df2a5-145">Position Register - oPos</span></span>

<span data-ttu-id="df2a5-146">輸出位置會註冊。</span><span class="sxs-lookup"><span data-stu-id="df2a5-146">The output position registers.</span></span> <span data-ttu-id="df2a5-147">值是同質剪切空間中的位置。</span><span class="sxs-lookup"><span data-stu-id="df2a5-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="df2a5-148">這個值必須由頂點著色器撰寫。</span><span class="sxs-lookup"><span data-stu-id="df2a5-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="df2a5-149">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="df2a5-149">Vertex shader versions</span></span> | <span data-ttu-id="df2a5-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="df2a5-150">1\_1</span></span> | <span data-ttu-id="df2a5-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-151">2\_0</span></span> | <span data-ttu-id="df2a5-152">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-152">2\_sw</span></span> | <span data-ttu-id="df2a5-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="df2a5-153">2\_x</span></span> | <span data-ttu-id="df2a5-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-154">3\_0</span></span> | <span data-ttu-id="df2a5-155">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="df2a5-156">位置註冊</span><span class="sxs-lookup"><span data-stu-id="df2a5-156">Position Register</span></span>      | <span data-ttu-id="df2a5-157">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-157">x</span></span>    | <span data-ttu-id="df2a5-158">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-158">x</span></span>    | <span data-ttu-id="df2a5-159">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-159">x</span></span>     | <span data-ttu-id="df2a5-160">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="df2a5-161">點大小注冊-選擇</span><span class="sxs-lookup"><span data-stu-id="df2a5-161">Point Size Register - oPts</span></span>

<span data-ttu-id="df2a5-162">輸出點大小暫存器。</span><span class="sxs-lookup"><span data-stu-id="df2a5-162">The output point-size registers.</span></span> <span data-ttu-id="df2a5-163">只會使用點大小的純量 x 部分。</span><span class="sxs-lookup"><span data-stu-id="df2a5-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="df2a5-164">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="df2a5-164">Vertex shader versions</span></span> | <span data-ttu-id="df2a5-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="df2a5-165">1\_1</span></span> | <span data-ttu-id="df2a5-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-166">2\_0</span></span> | <span data-ttu-id="df2a5-167">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-167">2\_sw</span></span> | <span data-ttu-id="df2a5-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="df2a5-168">2\_x</span></span> | <span data-ttu-id="df2a5-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-169">3\_0</span></span> | <span data-ttu-id="df2a5-170">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="df2a5-171">點大小暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-171">Point Size Register</span></span>    | <span data-ttu-id="df2a5-172">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-172">x</span></span>    | <span data-ttu-id="df2a5-173">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-173">x</span></span>    | <span data-ttu-id="df2a5-174">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-174">x</span></span>     | <span data-ttu-id="df2a5-175">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="df2a5-176">材質座標註冊-oT0 至 oT7</span><span class="sxs-lookup"><span data-stu-id="df2a5-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="df2a5-177">輸出材質會協調暫存器。</span><span class="sxs-lookup"><span data-stu-id="df2a5-177">The output texture coordinates registers.</span></span> <span data-ttu-id="df2a5-178">具體來說，這些是輸出資料暫存器的陣列，會透過將資料路由傳送至圖元著色器的材質取樣階段，逐一查看和使用這些暫存器作為材質座標。</span><span class="sxs-lookup"><span data-stu-id="df2a5-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="df2a5-179">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="df2a5-179">Vertex shader versions</span></span>      | <span data-ttu-id="df2a5-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="df2a5-180">1\_1</span></span> | <span data-ttu-id="df2a5-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-181">2\_0</span></span> | <span data-ttu-id="df2a5-182">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-182">2\_sw</span></span> | <span data-ttu-id="df2a5-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="df2a5-183">2\_x</span></span> | <span data-ttu-id="df2a5-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="df2a5-184">3\_0</span></span> | <span data-ttu-id="df2a5-185">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="df2a5-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="df2a5-186">材質座標註冊</span><span class="sxs-lookup"><span data-stu-id="df2a5-186">Texture Coordinate Register</span></span> | <span data-ttu-id="df2a5-187">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-187">x</span></span>    | <span data-ttu-id="df2a5-188">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-188">x</span></span>    | <span data-ttu-id="df2a5-189">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-189">x</span></span>     | <span data-ttu-id="df2a5-190">x</span><span class="sxs-lookup"><span data-stu-id="df2a5-190">x</span></span>    |      |       |



 

<span data-ttu-id="df2a5-191">寫入材質座標暫存器時，建議您只將許多浮點值傳遞為對應紋理對應的維度。</span><span class="sxs-lookup"><span data-stu-id="df2a5-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="df2a5-192">控制以修飾詞傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="df2a5-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="df2a5-193">例如，使用 xy 作為2D 材質地圖。</span><span class="sxs-lookup"><span data-stu-id="df2a5-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="df2a5-194">針對材質階段啟用紋理投影時，全部四個浮點值都必須寫入對應的材質暫存器。</span><span class="sxs-lookup"><span data-stu-id="df2a5-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="df2a5-195">使用可程式化 \* 管線時，任何 D3DTTFF 材質轉換旗標都應為零。</span><span class="sxs-lookup"><span data-stu-id="df2a5-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="df2a5-196">材質座標範圍</span><span class="sxs-lookup"><span data-stu-id="df2a5-196">Texture Coordinate Range</span></span>

<span data-ttu-id="df2a5-197">物件頂點資料提供輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="df2a5-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="df2a5-198">未使用並排顯示紋理的物件通常會在範圍 \[ 0，1的材質座標 \] 。</span><span class="sxs-lookup"><span data-stu-id="df2a5-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="df2a5-199">使用磚紋理的物件（例如地形）通常會有從 \[ -?, +？ where？的材質座標。 \]</span><span class="sxs-lookup"><span data-stu-id="df2a5-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="df2a5-200">可以是大型浮點數。</span><span class="sxs-lookup"><span data-stu-id="df2a5-200">can be a large floating point number.</span></span>

<span data-ttu-id="df2a5-201">紋理座標插補是在適用于光柵的頂點資料上執行。</span><span class="sxs-lookup"><span data-stu-id="df2a5-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="df2a5-202">在點陣化期間，材質座標是在物件頂點之間插入，由材質換行所修改並以紋理大小縮放 (也會納入考慮材質位址模式) 以產生整數索引。</span><span class="sxs-lookup"><span data-stu-id="df2a5-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="df2a5-203">然後使用索引來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="df2a5-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="df2a5-204">MaxTextureRepeat 可以用來判斷材質可以並排顯示多少次。</span><span class="sxs-lookup"><span data-stu-id="df2a5-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="df2a5-205">如果使用 texcoord 或 texcrd) 直接將材質座標讀入圖元著色器 (，則材質座標範圍取決於指示和圖元著色器版本。</span><span class="sxs-lookup"><span data-stu-id="df2a5-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df2a5-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="df2a5-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df2a5-207">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="df2a5-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




