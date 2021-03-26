---
title: texkill-ps
description: 如果紋理座標 (UVW) 的前三個元件中有任何一個小於零，則取消轉譯目前的圖元。
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313616"
---
# <a name="texkill---ps"></a><span data-ttu-id="16a74-103">texkill-ps</span><span class="sxs-lookup"><span data-stu-id="16a74-103">texkill - ps</span></span>

<span data-ttu-id="16a74-104">如果紋理座標 (UVW) 的前三個元件中有任何一個小於零，則取消轉譯目前的圖元。</span><span class="sxs-lookup"><span data-stu-id="16a74-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16a74-105">Syntax</span></span>



| <span data-ttu-id="16a74-106">texkill dst</span><span class="sxs-lookup"><span data-stu-id="16a74-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="16a74-107">其中</span><span class="sxs-lookup"><span data-stu-id="16a74-107">where</span></span>

-   <span data-ttu-id="16a74-108">dst 是目的地註冊</span><span class="sxs-lookup"><span data-stu-id="16a74-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="16a74-109">備註</span><span class="sxs-lookup"><span data-stu-id="16a74-109">Remarks</span></span>



| <span data-ttu-id="16a74-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="16a74-110">Pixel shader versions</span></span> | <span data-ttu-id="16a74-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="16a74-111">1\_1</span></span> | <span data-ttu-id="16a74-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="16a74-112">1\_2</span></span> | <span data-ttu-id="16a74-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="16a74-113">1\_3</span></span> | <span data-ttu-id="16a74-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="16a74-114">1\_4</span></span> | <span data-ttu-id="16a74-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16a74-115">2\_0</span></span> | <span data-ttu-id="16a74-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16a74-116">2\_x</span></span> | <span data-ttu-id="16a74-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="16a74-117">2\_sw</span></span> | <span data-ttu-id="16a74-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16a74-118">3\_0</span></span> | <span data-ttu-id="16a74-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="16a74-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="16a74-120">texkill</span><span class="sxs-lookup"><span data-stu-id="16a74-120">texkill</span></span>               | <span data-ttu-id="16a74-121">x</span><span class="sxs-lookup"><span data-stu-id="16a74-121">x</span></span>    | <span data-ttu-id="16a74-122">x</span><span class="sxs-lookup"><span data-stu-id="16a74-122">x</span></span>    | <span data-ttu-id="16a74-123">x</span><span class="sxs-lookup"><span data-stu-id="16a74-123">x</span></span>    | <span data-ttu-id="16a74-124">x</span><span class="sxs-lookup"><span data-stu-id="16a74-124">x</span></span>    | <span data-ttu-id="16a74-125">x</span><span class="sxs-lookup"><span data-stu-id="16a74-125">x</span></span>    | <span data-ttu-id="16a74-126">x</span><span class="sxs-lookup"><span data-stu-id="16a74-126">x</span></span>    | <span data-ttu-id="16a74-127">x</span><span class="sxs-lookup"><span data-stu-id="16a74-127">x</span></span>     | <span data-ttu-id="16a74-128">x</span><span class="sxs-lookup"><span data-stu-id="16a74-128">x</span></span>    | <span data-ttu-id="16a74-129">x</span><span class="sxs-lookup"><span data-stu-id="16a74-129">x</span></span>     |



 

<span data-ttu-id="16a74-130">此指令對應于 HLSL 的 [**剪輯**](dx-graphics-hlsl-clip.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="16a74-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="16a74-131">texkill 不會取樣任何材質。</span><span class="sxs-lookup"><span data-stu-id="16a74-131">texkill does not sample any texture.</span></span> <span data-ttu-id="16a74-132">它會在目的地暫存器編號所指定紋理座標的前三個元件上運作。</span><span class="sxs-lookup"><span data-stu-id="16a74-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="16a74-133">針對 ps \_ 1 \_ 4，texkill 會操作目的地登錄的前三個元件中的資料。</span><span class="sxs-lookup"><span data-stu-id="16a74-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="16a74-134">您可以使用此指令在轉譯器中執行任意的剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="16a74-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="16a74-135">使用頂點著色器時，應用程式會負責套用「透視圖」轉換。</span><span class="sxs-lookup"><span data-stu-id="16a74-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="16a74-136">這可能會造成任意裁剪平面的問題，因為如果它包含 anisomorphic 縮放比例，也需要轉換剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="16a74-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="16a74-137">因此，最好提供要用於任意 clipper 的 unprojected 頂點位置，也就是由 texkill 運算子識別的材質座標集合。</span><span class="sxs-lookup"><span data-stu-id="16a74-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="16a74-138">此指令的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="16a74-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="16a74-139">texkill tn</span><span class="sxs-lookup"><span data-stu-id="16a74-139">texkill tn</span></span>  
<span data-ttu-id="16a74-140">圖元遮罩的完成方式如下：</span><span class="sxs-lookup"><span data-stu-id="16a74-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="16a74-141">如果 ( TextureCoordinates 的 x、y、z 元件 (階段 n) <sub>UVWQ</sub>< 0 ) </span><span class="sxs-lookup"><span data-stu-id="16a74-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="16a74-142">取消圖元呈現</span><span class="sxs-lookup"><span data-stu-id="16a74-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="16a74-143">針對圖元著色器 1 \_ 1、1 \_ 2 和 1 \_ 3，texkill 會在目的地暫存器編號所指定的材質座標設定上運作。</span><span class="sxs-lookup"><span data-stu-id="16a74-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="16a74-144">不過，在第1版中， \_ texkill 會針對 [材質座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) 暫存器中包含的資料 (tn) 或在已指定為目的地的暫存登錄 (rn) 中操作。</span><span class="sxs-lookup"><span data-stu-id="16a74-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="16a74-145">當啟用取樣時，由於會在 texkill 所產生的任何邊緣上，對多邊形邊緣所達成的任何消除鋸齒效果，都不會沿著任何邊緣達成。</span><span class="sxs-lookup"><span data-stu-id="16a74-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="16a74-146">圖元著色器每圖元執行一次。</span><span class="sxs-lookup"><span data-stu-id="16a74-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="16a74-147">這個範例只供說明。</span><span class="sxs-lookup"><span data-stu-id="16a74-147">This example is for illustration only.</span></span>

<span data-ttu-id="16a74-148">此範例會遮罩具有負材質座標的圖元。</span><span class="sxs-lookup"><span data-stu-id="16a74-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="16a74-149">圖元色彩會從頂點資料中提供的頂點色彩插補。</span><span class="sxs-lookup"><span data-stu-id="16a74-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="16a74-150">紋理座標的範圍是從-0.5 到0.5 （u），以及 v 中的0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="16a74-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="16a74-151">此指示會使負 u 值遭到遮罩。下圖顯示套用至四個未套用 texkill 指令之四色的頂點色彩。</span><span class="sxs-lookup"><span data-stu-id="16a74-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="16a74-152">下圖顯示 texkill 指令的結果。</span><span class="sxs-lookup"><span data-stu-id="16a74-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="16a74-153">紋理座標中的圖元色彩會以 0 (，其中 x 從-0.5 到 0.0) 會被遮罩。背景色彩 (白色) 用來遮罩圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="16a74-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![將頂點色彩套用至不含 texkill 指令之四色輸出的圖例](images/pstexkill-in.jpg)![已套用 texkill 指令的輸出圖例](images/pstexkill-out.jpg)

<span data-ttu-id="16a74-156">紋理座標資料會在此範例中的頂點資料宣告中宣告。</span><span class="sxs-lookup"><span data-stu-id="16a74-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="16a74-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="16a74-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16a74-158">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="16a74-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




