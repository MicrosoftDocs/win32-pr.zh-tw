---
title: '常數 float register (HLSL 與參考) '
description: 四個元件浮點常數的頂點著色器輸入暫存器。 使用 def-vs 或 SetVertexShaderConstantF 設定常數暫存器。
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 856c9567070a071a123b28279342fd9cbbb0f6af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375613"
---
# <a name="constant-float-register-hlsl-vs-reference"></a><span data-ttu-id="66bdd-104">常數 float register (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="66bdd-104">Constant float register (HLSL VS reference)</span></span>

<span data-ttu-id="66bdd-105">四個元件浮點常數的頂點著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="66bdd-105">Vertex shader input register for a four component floating-point constant.</span></span> <span data-ttu-id="66bdd-106">使用 [def-vs](def---vs.md) 或 [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)設定常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="66bdd-106">Set a constant register with either [def - vs](def---vs.md) or [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).</span></span>

<span data-ttu-id="66bdd-107">常數暫存器檔案是唯讀的，從頂點著色器的角度來看。</span><span class="sxs-lookup"><span data-stu-id="66bdd-107">The constant register file is read-only from the perspective of the vertex shader.</span></span> <span data-ttu-id="66bdd-108">任何單一指令都只能存取一個常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="66bdd-108">Any single instruction may access only one constant register.</span></span> <span data-ttu-id="66bdd-109">不過，該指令中的每個來源可能會獨立 swizzle，並在讀取時對該向量進行否定。</span><span class="sxs-lookup"><span data-stu-id="66bdd-109">However, each source in that instruction may independently swizzle and negate that vector as it is read.</span></span>

<span data-ttu-id="66bdd-110">在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。</span><span class="sxs-lookup"><span data-stu-id="66bdd-110">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="66bdd-111">針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="66bdd-111">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="66bdd-112">使用 defx 宣告之常數的存留期只限于該著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="66bdd-112">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="66bdd-113">相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。</span><span class="sxs-lookup"><span data-stu-id="66bdd-113">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="66bdd-114">在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。</span><span class="sxs-lookup"><span data-stu-id="66bdd-114">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="66bdd-115">針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。</span><span class="sxs-lookup"><span data-stu-id="66bdd-115">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="66bdd-116">每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。</span><span class="sxs-lookup"><span data-stu-id="66bdd-116">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

<span data-ttu-id="66bdd-117">常數暫存器會指定為絕對或相對：</span><span class="sxs-lookup"><span data-stu-id="66bdd-117">A constant register is designated as either absolute or relative:</span></span>


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



<span data-ttu-id="66bdd-118">您可以使用絕對索引或從位址暫存器中的相對索引，讀取常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="66bdd-118">The constant register can be read, therefore, either by using an absolute index or with a relative index from an address register.</span></span> <span data-ttu-id="66bdd-119">從超出範圍的暫存器讀取會傳回 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="66bdd-119">Reads from out-of-range registers return (0.0, 0.0, 0.0, 0.0).</span></span>

## <a name="examples"></a><span data-ttu-id="66bdd-120">範例</span><span class="sxs-lookup"><span data-stu-id="66bdd-120">Examples</span></span>

<span data-ttu-id="66bdd-121">以下是在著色器中宣告兩個浮點常數的範例。</span><span class="sxs-lookup"><span data-stu-id="66bdd-121">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="66bdd-122">每次呼叫 [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) 時，就會載入這些常數。</span><span class="sxs-lookup"><span data-stu-id="66bdd-122">These constants are loaded every time [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) is called.</span></span>

<span data-ttu-id="66bdd-123">以下是使用 API 的範例。</span><span class="sxs-lookup"><span data-stu-id="66bdd-123">Here is an example using the API.</span></span>


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



<span data-ttu-id="66bdd-124">如果您要使用 API 來設定常數值，則不需要著色器宣告。</span><span class="sxs-lookup"><span data-stu-id="66bdd-124">If you are setting constant values with the API, there is no shader declaration required.</span></span>



| <span data-ttu-id="66bdd-125">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="66bdd-125">Vertex shader versions</span></span> | <span data-ttu-id="66bdd-126">1\_1</span><span class="sxs-lookup"><span data-stu-id="66bdd-126">1\_1</span></span> | <span data-ttu-id="66bdd-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="66bdd-127">2\_0</span></span> | <span data-ttu-id="66bdd-128">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="66bdd-128">2\_sw</span></span> | <span data-ttu-id="66bdd-129">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="66bdd-129">2\_x</span></span> | <span data-ttu-id="66bdd-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="66bdd-130">3\_0</span></span> | <span data-ttu-id="66bdd-131">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="66bdd-131">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="66bdd-132">常數暫存器</span><span class="sxs-lookup"><span data-stu-id="66bdd-132">Constant Register</span></span>      | <span data-ttu-id="66bdd-133">x</span><span class="sxs-lookup"><span data-stu-id="66bdd-133">x</span></span>    | <span data-ttu-id="66bdd-134">x</span><span class="sxs-lookup"><span data-stu-id="66bdd-134">x</span></span>    | <span data-ttu-id="66bdd-135">x</span><span class="sxs-lookup"><span data-stu-id="66bdd-135">x</span></span>     | <span data-ttu-id="66bdd-136">x</span><span class="sxs-lookup"><span data-stu-id="66bdd-136">x</span></span>    | <span data-ttu-id="66bdd-137">x</span><span class="sxs-lookup"><span data-stu-id="66bdd-137">x</span></span>    | <span data-ttu-id="66bdd-138">x</span><span class="sxs-lookup"><span data-stu-id="66bdd-138">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="66bdd-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="66bdd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66bdd-140">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="66bdd-140">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 