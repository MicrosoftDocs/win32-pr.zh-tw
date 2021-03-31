---
title: texm3x3tex-ps
description: 執行3x3 矩陣相乘，並使用結果來執行材質查閱。 texm3x3tex 必須搭配兩個 texm3x3pad ps 指令使用。
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373939"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="17d1d-104">texm3x3tex-ps</span><span class="sxs-lookup"><span data-stu-id="17d1d-104">texm3x3tex - ps</span></span>

<span data-ttu-id="17d1d-105">執行3x3 矩陣相乘，並使用結果來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="17d1d-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="17d1d-106">texm3x3tex 必須搭配兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令使用。</span><span class="sxs-lookup"><span data-stu-id="17d1d-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d1d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17d1d-107">Syntax</span></span>



| <span data-ttu-id="17d1d-108">texm3x3tex dst、src</span><span class="sxs-lookup"><span data-stu-id="17d1d-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="17d1d-109">其中</span><span class="sxs-lookup"><span data-stu-id="17d1d-109">where</span></span>

-   <span data-ttu-id="17d1d-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="17d1d-110">dst is the destination register.</span></span>
-   <span data-ttu-id="17d1d-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="17d1d-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d1d-112">備註</span><span class="sxs-lookup"><span data-stu-id="17d1d-112">Remarks</span></span>



| <span data-ttu-id="17d1d-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="17d1d-113">Pixel shader versions</span></span> | <span data-ttu-id="17d1d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="17d1d-114">1\_1</span></span> | <span data-ttu-id="17d1d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="17d1d-115">1\_2</span></span> | <span data-ttu-id="17d1d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="17d1d-116">1\_3</span></span> | <span data-ttu-id="17d1d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="17d1d-117">1\_4</span></span> | <span data-ttu-id="17d1d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17d1d-118">2\_0</span></span> | <span data-ttu-id="17d1d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17d1d-119">2\_x</span></span> | <span data-ttu-id="17d1d-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="17d1d-120">2\_sw</span></span> | <span data-ttu-id="17d1d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17d1d-121">3\_0</span></span> | <span data-ttu-id="17d1d-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="17d1d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="17d1d-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="17d1d-123">texm3x3tex</span></span>            | <span data-ttu-id="17d1d-124">x</span><span class="sxs-lookup"><span data-stu-id="17d1d-124">x</span></span>    | <span data-ttu-id="17d1d-125">x</span><span class="sxs-lookup"><span data-stu-id="17d1d-125">x</span></span>    | <span data-ttu-id="17d1d-126">x</span><span class="sxs-lookup"><span data-stu-id="17d1d-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="17d1d-127">此指令會當做三個指示的最後一個，表示3x3 矩陣乘法運算，後面接著紋理查閱。</span><span class="sxs-lookup"><span data-stu-id="17d1d-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="17d1d-128">3x3 矩陣是由第三個材質階段的材質座標和上述兩個材質階段所組成。</span><span class="sxs-lookup"><span data-stu-id="17d1d-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="17d1d-129">產生的三個元件向量 (u、v、w) 用來取樣第3階段中的材質。</span><span class="sxs-lookup"><span data-stu-id="17d1d-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="17d1d-130">所有指派給上述兩個材質階段的材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="17d1d-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="17d1d-131">3x3 矩陣相乘通常適用于將一般向量定位至所呈現介面的正確正切空間。</span><span class="sxs-lookup"><span data-stu-id="17d1d-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="17d1d-132">此指令必須搭配 texm3x3pad 指令使用。</span><span class="sxs-lookup"><span data-stu-id="17d1d-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="17d1d-133">材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="17d1d-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="17d1d-134">以下是有關3x3 乘法如何完成的更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="17d1d-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="17d1d-135">第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="17d1d-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="17d1d-136">u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="17d1d-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="17d1d-137">第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="17d1d-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="17d1d-138">v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="17d1d-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="17d1d-139">Texm3x3spec 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="17d1d-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="17d1d-140">w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="17d1d-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="17d1d-141">最後，texm3x3tex 指令範例 t (m + 2) 使用 (u<sup>'</sup>，v<sup>'</sup>，w<sup>'</sup>) 並將結果儲存在 t (m + 2) 中。</span><span class="sxs-lookup"><span data-stu-id="17d1d-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="17d1d-142">t (m + 2) <sub>rgba</sub> = TextureSample (階段 m + 2) 使用 (u<sup>'</sup> ，v<sup>'</sup> ，w<sup>'</sup> ) 作為座標的<sub>RGBA</sub> 。</span><span class="sxs-lookup"><span data-stu-id="17d1d-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="17d1d-143">範例</span><span class="sxs-lookup"><span data-stu-id="17d1d-143">Examples</span></span>

<span data-ttu-id="17d1d-144">以下是已識別材質地圖和識別材質階段的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="17d1d-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="17d1d-145">此範例需要下列紋理階段設定。</span><span class="sxs-lookup"><span data-stu-id="17d1d-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="17d1d-146">階段0會指派具有一般資料的材質對應。</span><span class="sxs-lookup"><span data-stu-id="17d1d-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="17d1d-147">這通常稱為「凹凸地圖」。</span><span class="sxs-lookup"><span data-stu-id="17d1d-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="17d1d-148">資料是每個材質的 XYZ) 法線 (。</span><span class="sxs-lookup"><span data-stu-id="17d1d-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="17d1d-149">材質座標集合0定義如何取樣此標準地圖。</span><span class="sxs-lookup"><span data-stu-id="17d1d-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="17d1d-150">紋理座標集合1會指派給3x3 矩陣的第1列。</span><span class="sxs-lookup"><span data-stu-id="17d1d-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="17d1d-151">指派給階段1的任何材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="17d1d-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="17d1d-152">紋理座標集合2會指派給3x3 矩陣的第2列。</span><span class="sxs-lookup"><span data-stu-id="17d1d-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="17d1d-153">指派給階段2的任何材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="17d1d-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="17d1d-154">紋理座標集合3會指派給3x3 矩陣的第3列。</span><span class="sxs-lookup"><span data-stu-id="17d1d-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="17d1d-155">必須將磁片區或 cube 材質設定為第3階段，才能依轉換的3D 向量進行查閱。</span><span class="sxs-lookup"><span data-stu-id="17d1d-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17d1d-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="17d1d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d1d-157">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="17d1d-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




