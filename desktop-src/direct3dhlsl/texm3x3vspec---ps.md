---
title: texm3x3vspec-ps
description: 執行3x3 矩陣相乘，並使用結果來執行材質查閱。
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932823"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="bf789-103">texm3x3vspec-ps</span><span class="sxs-lookup"><span data-stu-id="bf789-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="bf789-104">執行3x3 矩陣相乘，並使用結果來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="bf789-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="bf789-105">這可用於反射向量和環境對應，其中的眼睛光線不是常數。</span><span class="sxs-lookup"><span data-stu-id="bf789-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="bf789-106">texm3x3vspec 必須搭配兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令使用。</span><span class="sxs-lookup"><span data-stu-id="bf789-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="bf789-107">如果眼睛向量是常數，則 [texm3x3spec 的 ps](texm3x3spec---ps.md) 指令會執行相同的矩陣乘法和紋理查閱。</span><span class="sxs-lookup"><span data-stu-id="bf789-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf789-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf789-108">Syntax</span></span>



| <span data-ttu-id="bf789-109">texm3x3vspec dst、src</span><span class="sxs-lookup"><span data-stu-id="bf789-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="bf789-110">其中</span><span class="sxs-lookup"><span data-stu-id="bf789-110">where</span></span>

-   <span data-ttu-id="bf789-111">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="bf789-111">dst is the destination register.</span></span>
-   <span data-ttu-id="bf789-112">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="bf789-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf789-113">備註</span><span class="sxs-lookup"><span data-stu-id="bf789-113">Remarks</span></span>



| <span data-ttu-id="bf789-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="bf789-114">Pixel shader versions</span></span> | <span data-ttu-id="bf789-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="bf789-115">1\_1</span></span> | <span data-ttu-id="bf789-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="bf789-116">1\_2</span></span> | <span data-ttu-id="bf789-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bf789-117">1\_3</span></span> | <span data-ttu-id="bf789-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="bf789-118">1\_4</span></span> | <span data-ttu-id="bf789-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf789-119">2\_0</span></span> | <span data-ttu-id="bf789-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bf789-120">2\_x</span></span> | <span data-ttu-id="bf789-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bf789-121">2\_sw</span></span> | <span data-ttu-id="bf789-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf789-122">3\_0</span></span> | <span data-ttu-id="bf789-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="bf789-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bf789-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="bf789-124">texm3x3vspec</span></span>          | <span data-ttu-id="bf789-125">x</span><span class="sxs-lookup"><span data-stu-id="bf789-125">x</span></span>    | <span data-ttu-id="bf789-126">x</span><span class="sxs-lookup"><span data-stu-id="bf789-126">x</span></span>    | <span data-ttu-id="bf789-127">x</span><span class="sxs-lookup"><span data-stu-id="bf789-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="bf789-128">此指令會執行3x3 矩陣乘法運算的最後一個資料列，將產生的向量視為一般向量以反映眼睛的向量，然後使用反映的向量作為紋理查閱的材質位址。</span><span class="sxs-lookup"><span data-stu-id="bf789-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="bf789-129">它的運作方式就像 [texm3x3spec-ps](texm3x3spec---ps.md)，不同之處在于，會從紋理座標的第四個元件取得眼睛光線向量。</span><span class="sxs-lookup"><span data-stu-id="bf789-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="bf789-130">3x3 矩陣相乘通常適用于將一般向量定位至所呈現介面的正確正切空間。</span><span class="sxs-lookup"><span data-stu-id="bf789-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="bf789-131">3x3 矩陣是由第三個材質階段的材質座標和上述兩個材質階段所組成。</span><span class="sxs-lookup"><span data-stu-id="bf789-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="bf789-132">產生的後置反映向量 (UVW) 用來取樣第3階段中的材質。</span><span class="sxs-lookup"><span data-stu-id="bf789-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="bf789-133">所有指派給上述兩個材質階段的材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bf789-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="bf789-134">此指令必須搭配 texm3x3pad 指令使用。</span><span class="sxs-lookup"><span data-stu-id="bf789-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="bf789-135">材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="bf789-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="bf789-136">第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="bf789-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="bf789-137">u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bf789-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="bf789-138">第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="bf789-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="bf789-139">v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bf789-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="bf789-140">Texm3x3spec 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="bf789-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="bf789-141">w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bf789-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="bf789-142">Texm3x3vspec 指令也會進行反映計算。</span><span class="sxs-lookup"><span data-stu-id="bf789-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="bf789-143"> (u<sup>'</sup> 、v<sup>'</sup> 、w<sup>'</sup> ) = 2 \* \[ (n \* E) / (n \* n) \] \* n-E</span><span class="sxs-lookup"><span data-stu-id="bf789-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="bf789-144">其中的一般 N 是由</span><span class="sxs-lookup"><span data-stu-id="bf789-144">// where the normal N is given by</span></span>

<span data-ttu-id="bf789-145">N = (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) </span><span class="sxs-lookup"><span data-stu-id="bf789-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="bf789-146">而眼睛向量 E 的指定方式為</span><span class="sxs-lookup"><span data-stu-id="bf789-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="bf789-147">E = (TextureCoordinates (階段 m) <sub>Q</sub> ，</span><span class="sxs-lookup"><span data-stu-id="bf789-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="bf789-148">TextureCoordinates (階段 m + 1) <sub>Q</sub> ，</span><span class="sxs-lookup"><span data-stu-id="bf789-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="bf789-149">TextureCoordinates (階段 m + 2) <sub>Q</sub> ) </span><span class="sxs-lookup"><span data-stu-id="bf789-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="bf789-150">最後，texm3x3vspec 指令範例 t (m + 2) 使用 (u<sup>'</sup>，v<sup>'</sup>，w<sup>'</sup>) 並將結果儲存在 t (m + 2) 中。</span><span class="sxs-lookup"><span data-stu-id="bf789-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="bf789-151">t (m + 2) <sub>RGBA</sub> = TextureSample (階段 m + 2) 使用 (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 作為座標的<sub>RGBA</sub></span><span class="sxs-lookup"><span data-stu-id="bf789-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="bf789-152">範例</span><span class="sxs-lookup"><span data-stu-id="bf789-152">Examples</span></span>

<span data-ttu-id="bf789-153">以下是已識別材質地圖和識別材質階段的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="bf789-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="bf789-154">此範例需要下列紋理階段設定。</span><span class="sxs-lookup"><span data-stu-id="bf789-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="bf789-155">階段0會指派具有一般資料的材質對應。</span><span class="sxs-lookup"><span data-stu-id="bf789-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="bf789-156">這通常稱為「凹凸地圖」。</span><span class="sxs-lookup"><span data-stu-id="bf789-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="bf789-157">資料是每個材質的 XYZ) 法線 (。</span><span class="sxs-lookup"><span data-stu-id="bf789-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="bf789-158">階段 n 的材質座標定義如何取樣此標準地圖。</span><span class="sxs-lookup"><span data-stu-id="bf789-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="bf789-159">紋理座標集合 m 會指派給3x3 矩陣的第1列。</span><span class="sxs-lookup"><span data-stu-id="bf789-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="bf789-160">指派給階段 m 的任何材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bf789-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="bf789-161">紋理座標集合 m + 1 會指派給3x3 矩陣的資料列2。</span><span class="sxs-lookup"><span data-stu-id="bf789-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="bf789-162">指派給階段 m + 1 的任何材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bf789-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="bf789-163">紋理座標集合 m + 2 會指派給3x3 矩陣的第3列。</span><span class="sxs-lookup"><span data-stu-id="bf789-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="bf789-164">階段 m + 2 是指派給磁片區或 cube 材質地圖。</span><span class="sxs-lookup"><span data-stu-id="bf789-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="bf789-165">材質提供色彩資料 (RGBA) 。</span><span class="sxs-lookup"><span data-stu-id="bf789-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="bf789-166">眼睛向量 E 會傳遞至第四個元件中的指示， (q) 的材質座標資料階段 m、m + 1 和 m + 2。</span><span class="sxs-lookup"><span data-stu-id="bf789-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf789-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf789-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf789-168">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="bf789-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




