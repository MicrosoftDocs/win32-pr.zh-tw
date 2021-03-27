---
title: texcoord-ps
description: 將材質座標資料 (UVW1)  (RGBA) 的色彩資料來解讀。
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682547"
---
# <a name="texcoord---ps"></a><span data-ttu-id="047e9-103">texcoord-ps</span><span class="sxs-lookup"><span data-stu-id="047e9-103">texcoord - ps</span></span>

<span data-ttu-id="047e9-104">將材質座標資料 (UVW1)  (RGBA) 的色彩資料來解讀。</span><span class="sxs-lookup"><span data-stu-id="047e9-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="047e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="047e9-105">Syntax</span></span>



| <span data-ttu-id="047e9-106">texcoord dst</span><span class="sxs-lookup"><span data-stu-id="047e9-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="047e9-107">其中</span><span class="sxs-lookup"><span data-stu-id="047e9-107">where</span></span>

-   <span data-ttu-id="047e9-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="047e9-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="047e9-109">備註</span><span class="sxs-lookup"><span data-stu-id="047e9-109">Remarks</span></span>



| <span data-ttu-id="047e9-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="047e9-110">Pixel shader versions</span></span> | <span data-ttu-id="047e9-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="047e9-111">1\_1</span></span> | <span data-ttu-id="047e9-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="047e9-112">1\_2</span></span> | <span data-ttu-id="047e9-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="047e9-113">1\_3</span></span> | <span data-ttu-id="047e9-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="047e9-114">1\_4</span></span> | <span data-ttu-id="047e9-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="047e9-115">2\_0</span></span> | <span data-ttu-id="047e9-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="047e9-116">2\_x</span></span> | <span data-ttu-id="047e9-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="047e9-117">2\_sw</span></span> | <span data-ttu-id="047e9-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="047e9-118">3\_0</span></span> | <span data-ttu-id="047e9-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="047e9-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="047e9-120">texcoord</span><span class="sxs-lookup"><span data-stu-id="047e9-120">texcoord</span></span>              | <span data-ttu-id="047e9-121">x</span><span class="sxs-lookup"><span data-stu-id="047e9-121">x</span></span>    | <span data-ttu-id="047e9-122">x</span><span class="sxs-lookup"><span data-stu-id="047e9-122">x</span></span>    | <span data-ttu-id="047e9-123">x</span><span class="sxs-lookup"><span data-stu-id="047e9-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="047e9-124">此指令會將材質座標集 (UVW1) 對應至目的地暫存器號碼，以 (RGBA) 的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="047e9-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="047e9-125">如果材質座標集包含三個以上的元件，則遺漏的元件會設定為0。</span><span class="sxs-lookup"><span data-stu-id="047e9-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="047e9-126">第四個元件一律設定為1。</span><span class="sxs-lookup"><span data-stu-id="047e9-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="047e9-127">所有值都壓制介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="047e9-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="047e9-128">Texcoord 的優點是，它提供一種方式，將頂點資料以高精確度的方式直接傳遞至圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="047e9-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="047e9-129">不過，當資料寫入目的地暫存器時，將會遺失某些精確度，視暫存器的硬體使用的位數而定。</span><span class="sxs-lookup"><span data-stu-id="047e9-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="047e9-130">此指令未取樣任何紋理。</span><span class="sxs-lookup"><span data-stu-id="047e9-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="047e9-131">只有在此材質階段設定的材質座標是相關的。</span><span class="sxs-lookup"><span data-stu-id="047e9-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="047e9-132">任何材質資料 (例如位置、標準和光源方向) 都可由頂點著色器對應至材質座標。</span><span class="sxs-lookup"><span data-stu-id="047e9-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="047e9-133">這是藉由使用 [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) 將材質與材質暫存器產生關聯，以及指定如何使用 [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)來完成紋理取樣來完成。</span><span class="sxs-lookup"><span data-stu-id="047e9-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="047e9-134">如果使用了 fixed 函數管線，請務必提供 TSS \_ TEXCOORDINDEX 旗標。</span><span class="sxs-lookup"><span data-stu-id="047e9-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="047e9-135">此指令的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="047e9-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="047e9-136">[材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) 包含四個色彩值 (RGBA) 。</span><span class="sxs-lookup"><span data-stu-id="047e9-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="047e9-137">您也可以將資料視為向量資料 (xyzw) 。</span><span class="sxs-lookup"><span data-stu-id="047e9-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="047e9-138">texcoord 將會從紋理座標集 x (xyz) 取得這些值的三個值，而第四個元件 (w) 會設定為1。</span><span class="sxs-lookup"><span data-stu-id="047e9-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="047e9-139">紋理位址會從紋理座標集合 n 複製。</span><span class="sxs-lookup"><span data-stu-id="047e9-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="047e9-140">結果為0和1之間的壓制。</span><span class="sxs-lookup"><span data-stu-id="047e9-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="047e9-141">這個範例只供說明。</span><span class="sxs-lookup"><span data-stu-id="047e9-141">This example is for illustration only.</span></span> <span data-ttu-id="047e9-142">著色器隨附的 C 程式碼尚未針對效能進行優化。</span><span class="sxs-lookup"><span data-stu-id="047e9-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="047e9-143">以下是使用 texcoord 的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="047e9-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="047e9-144">圖元著色器所呈現的輸出如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="047e9-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="047e9-145"> (u，v，w，1) 座標值會對應至 (rgb) 通道。</span><span class="sxs-lookup"><span data-stu-id="047e9-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="047e9-146">Alpha 色板設定為1。</span><span class="sxs-lookup"><span data-stu-id="047e9-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="047e9-147">在圖的角落，座標 (0、0、0、1) 會轉譯為黑色; (1、0、0、1) 為紅色; (0、1、0、1) 為綠色; (1、1、0、1) 包含綠色和紅色，產生黃色。</span><span class="sxs-lookup"><span data-stu-id="047e9-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![範例圖元著色器的呈現輸出圖例](images/pstexcoord.jpg)

<span data-ttu-id="047e9-149">需要額外的程式碼才能使用此著色器，而範例案例如下所示。</span><span class="sxs-lookup"><span data-stu-id="047e9-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="047e9-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="047e9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="047e9-151">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="047e9-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 