---
title: texm3x3spec-ps
description: 執行3x3 矩陣相乘，並使用結果來執行材質查閱。 這可用於反射反映和環境對應。 texm3x3spec 必須搭配兩個 texm3x3pad ps 指令使用。
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373763"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="e065d-105">texm3x3spec-ps</span><span class="sxs-lookup"><span data-stu-id="e065d-105">texm3x3spec - ps</span></span>

<span data-ttu-id="e065d-106">執行3x3 矩陣相乘，並使用結果來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="e065d-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="e065d-107">這可用於反射反映和環境對應。</span><span class="sxs-lookup"><span data-stu-id="e065d-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="e065d-108">texm3x3spec 必須搭配兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令使用。</span><span class="sxs-lookup"><span data-stu-id="e065d-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e065d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e065d-109">Syntax</span></span>



| <span data-ttu-id="e065d-110">texm3x3spec dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="e065d-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="e065d-111">其中</span><span class="sxs-lookup"><span data-stu-id="e065d-111">where</span></span>

-   <span data-ttu-id="e065d-112">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e065d-112">dst is the destination register.</span></span>
-   <span data-ttu-id="e065d-113">src0 和 src1 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="e065d-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="e065d-114">備註</span><span class="sxs-lookup"><span data-stu-id="e065d-114">Remarks</span></span>



| <span data-ttu-id="e065d-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e065d-115">Pixel shader versions</span></span> | <span data-ttu-id="e065d-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="e065d-116">1\_1</span></span> | <span data-ttu-id="e065d-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="e065d-117">1\_2</span></span> | <span data-ttu-id="e065d-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e065d-118">1\_3</span></span> | <span data-ttu-id="e065d-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="e065d-119">1\_4</span></span> | <span data-ttu-id="e065d-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e065d-120">2\_0</span></span> | <span data-ttu-id="e065d-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e065d-121">2\_x</span></span> | <span data-ttu-id="e065d-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e065d-122">2\_sw</span></span> | <span data-ttu-id="e065d-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e065d-123">3\_0</span></span> | <span data-ttu-id="e065d-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e065d-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e065d-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="e065d-125">texm3x3spec</span></span>           | <span data-ttu-id="e065d-126">x</span><span class="sxs-lookup"><span data-stu-id="e065d-126">x</span></span>    | <span data-ttu-id="e065d-127">x</span><span class="sxs-lookup"><span data-stu-id="e065d-127">x</span></span>    | <span data-ttu-id="e065d-128">x</span><span class="sxs-lookup"><span data-stu-id="e065d-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="e065d-129">此指令會執行3x3 矩陣相乘的最後一個資料列，使用產生的向量做為一般向量以反映眼睛的向量，然後使用反映的向量來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="e065d-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="e065d-130">著色器會從常數暫存器讀取眼睛光線向量。</span><span class="sxs-lookup"><span data-stu-id="e065d-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="e065d-131">3x3 矩陣相乘通常適用于將一般向量定位至所呈現介面的正確正切空間。</span><span class="sxs-lookup"><span data-stu-id="e065d-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="e065d-132">3x3 矩陣是由第三個材質階段的材質座標和上述兩個材質階段所組成。</span><span class="sxs-lookup"><span data-stu-id="e065d-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="e065d-133">產生的貼文反映向量 (u、v、w) 用來取樣最後紋理階段上的材質。</span><span class="sxs-lookup"><span data-stu-id="e065d-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="e065d-134">所有指派給上述兩個材質階段的材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e065d-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="e065d-135">此指令必須搭配兩個 texm3x3pad 指令使用。</span><span class="sxs-lookup"><span data-stu-id="e065d-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="e065d-136">材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="e065d-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="e065d-137">第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="e065d-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="e065d-138">u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e065d-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e065d-139">第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="e065d-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="e065d-140">v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e065d-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e065d-141">Texm3x3spec 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="e065d-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="e065d-142">w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e065d-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e065d-143">然後，texm3x3spec 指令會進行反映計算。</span><span class="sxs-lookup"><span data-stu-id="e065d-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="e065d-144"> (u<sup>'</sup> 、v<sup>'</sup> 、w<sup>'</sup> ) = 2 \* \[ (n \* E) / (n \* n) \] \* n-E</span><span class="sxs-lookup"><span data-stu-id="e065d-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="e065d-145">其中的一般 N 是由</span><span class="sxs-lookup"><span data-stu-id="e065d-145">// where the normal N is given by</span></span>

<span data-ttu-id="e065d-146">N = (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) </span><span class="sxs-lookup"><span data-stu-id="e065d-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="e065d-147">常數暫存器提供了眼睛向量 E</span><span class="sxs-lookup"><span data-stu-id="e065d-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="e065d-148">E = c \# (任何常數暫存器--c0、c1、c2 等等--可以使用) </span><span class="sxs-lookup"><span data-stu-id="e065d-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="e065d-149">最後，texm3x3spec 指令範例 t (m + 2) 使用 (u<sup>'</sup>，v<sup>'</sup>，w<sup>'</sup>) 並將結果儲存在 t (m + 2) 中。</span><span class="sxs-lookup"><span data-stu-id="e065d-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="e065d-150">t (m + 2) <sub>RGBA</sub> = TextureSample (階段 m + 2) 使用 (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 作為座標的<sub>RGBA</sub></span><span class="sxs-lookup"><span data-stu-id="e065d-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="e065d-151">範例</span><span class="sxs-lookup"><span data-stu-id="e065d-151">Examples</span></span>

<span data-ttu-id="e065d-152">以下是已識別材質地圖和材質階段的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="e065d-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="e065d-153">此範例需要下列紋理階段設定。</span><span class="sxs-lookup"><span data-stu-id="e065d-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="e065d-154">階段0會指派具有一般資料的材質對應。</span><span class="sxs-lookup"><span data-stu-id="e065d-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="e065d-155">這通常稱為「凹凸地圖」。</span><span class="sxs-lookup"><span data-stu-id="e065d-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="e065d-156">資料是每個材質的 XYZ) 法線 (。</span><span class="sxs-lookup"><span data-stu-id="e065d-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="e065d-157">階段 n 的材質座標定義此標準地圖的取樣位置。</span><span class="sxs-lookup"><span data-stu-id="e065d-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="e065d-158">紋理座標集合 m 會指派給3x3 矩陣的第1列。</span><span class="sxs-lookup"><span data-stu-id="e065d-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="e065d-159">指派給階段 m 的任何材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e065d-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="e065d-160">紋理座標集合 m + 1 會指派給3x3 矩陣的資料列2。</span><span class="sxs-lookup"><span data-stu-id="e065d-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="e065d-161">指派給階段 m + 1 的任何材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e065d-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="e065d-162">紋理座標集合 m + 2 會指派給3x3 矩陣的第3列。</span><span class="sxs-lookup"><span data-stu-id="e065d-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="e065d-163">階段 m + 2 是指派給磁片區或 cube 材質地圖。</span><span class="sxs-lookup"><span data-stu-id="e065d-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="e065d-164">材質提供色彩資料 (RGBA) 。</span><span class="sxs-lookup"><span data-stu-id="e065d-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="e065d-165">眼睛向量 E 是由常數暫存器 E = c 所指定 \# 。</span><span class="sxs-lookup"><span data-stu-id="e065d-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e065d-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="e065d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e065d-167">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e065d-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




