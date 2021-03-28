---
title: '紋理座標註冊 (HLSL 與參考) '
description: 此頂點著色器輸出暫存器包含每個頂點的材質座標。
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093204"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="76daa-103">紋理座標註冊 (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="76daa-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="76daa-104">此頂點著色器輸出暫存器包含每個頂點的材質座標。</span><span class="sxs-lookup"><span data-stu-id="76daa-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="76daa-105">暫存器包含的屬性會決定每個註冊的行為。</span><span class="sxs-lookup"><span data-stu-id="76daa-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="76daa-106">屬性</span><span class="sxs-lookup"><span data-stu-id="76daa-106">Property</span></span>        | <span data-ttu-id="76daa-107">描述</span><span class="sxs-lookup"><span data-stu-id="76daa-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="76daa-108">名稱</span><span class="sxs-lookup"><span data-stu-id="76daa-108">Name</span></span>            | <span data-ttu-id="76daa-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="76daa-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="76daa-110">Count</span><span class="sxs-lookup"><span data-stu-id="76daa-110">Count</span></span>           | <span data-ttu-id="76daa-111">八個向量</span><span class="sxs-lookup"><span data-stu-id="76daa-111">Eight vectors</span></span> |
| <span data-ttu-id="76daa-112">I/o 許可權</span><span class="sxs-lookup"><span data-stu-id="76daa-112">I/O permissions</span></span> | <span data-ttu-id="76daa-113">唯寫</span><span class="sxs-lookup"><span data-stu-id="76daa-113">Write-only</span></span>    |



 

<span data-ttu-id="76daa-114">輸出材質座標暫存器是輸出資料暫存器的陣列。</span><span class="sxs-lookup"><span data-stu-id="76daa-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="76daa-115">「註冊」資料會依紋理取樣階段逐一查看並當做材質座標使用，以提供資料給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="76daa-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="76daa-116">寫入材質座標暫存器時，建議您只將許多浮點值傳遞為對應紋理對應的維度。</span><span class="sxs-lookup"><span data-stu-id="76daa-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="76daa-117">控制以修飾詞傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="76daa-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="76daa-118">例如，使用 xy 作為2D 材質地圖。</span><span class="sxs-lookup"><span data-stu-id="76daa-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="76daa-119">如果您使用可程式化的頂點著色器，固定的函式頂點管線旗標（ [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1、D3DTTFF \_ COUNT2、D3DTTFF \_ COUNT3、D3DTTFF \_ COUNT4) ）應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="76daa-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="76daa-120">物件頂點資料提供輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="76daa-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="76daa-121">未使用並排紋理的物件通常會在範圍 \[ 0，1的材質座標 \] 。</span><span class="sxs-lookup"><span data-stu-id="76daa-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="76daa-122">使用平鋪紋理的物件（例如地形）通常具有從 \[ -n、+ n 的材質座標， \] 其中 n 可以是任何浮點數。</span><span class="sxs-lookup"><span data-stu-id="76daa-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="76daa-123">紋理座標插補是在適用于光柵的頂點資料上執行。</span><span class="sxs-lookup"><span data-stu-id="76daa-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="76daa-124">在點陣化期間，材質座標是在物件頂點之間插入，由材質換行所修改，並以紋理大小進行縮放， (也會將材質定址模式) 以產生整數索引。</span><span class="sxs-lookup"><span data-stu-id="76daa-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="76daa-125">然後使用索引來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="76daa-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="76daa-126">您可以使用 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) 中的 MaxTextureRepeat 值，判斷材質可以並排顯示多少次。</span><span class="sxs-lookup"><span data-stu-id="76daa-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="76daa-127">範例</span><span class="sxs-lookup"><span data-stu-id="76daa-127">Example</span></span>

<span data-ttu-id="76daa-128">宣告材質座標註冊。</span><span class="sxs-lookup"><span data-stu-id="76daa-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="76daa-129">將每個頂點的材質座標複製到輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="76daa-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="76daa-130">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="76daa-130">Vertex shader versions</span></span>      | <span data-ttu-id="76daa-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="76daa-131">1\_1</span></span> | <span data-ttu-id="76daa-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76daa-132">2\_0</span></span> | <span data-ttu-id="76daa-133">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="76daa-133">2\_sw</span></span> | <span data-ttu-id="76daa-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="76daa-134">2\_x</span></span> | <span data-ttu-id="76daa-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="76daa-135">3\_0</span></span> | <span data-ttu-id="76daa-136">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="76daa-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="76daa-137">材質座標註冊</span><span class="sxs-lookup"><span data-stu-id="76daa-137">Texture Coordinate Register</span></span> | <span data-ttu-id="76daa-138">x</span><span class="sxs-lookup"><span data-stu-id="76daa-138">x</span></span>    | <span data-ttu-id="76daa-139">x</span><span class="sxs-lookup"><span data-stu-id="76daa-139">x</span></span>    | <span data-ttu-id="76daa-140">x</span><span class="sxs-lookup"><span data-stu-id="76daa-140">x</span></span>     | <span data-ttu-id="76daa-141">x</span><span class="sxs-lookup"><span data-stu-id="76daa-141">x</span></span>    | <span data-ttu-id="76daa-142">x</span><span class="sxs-lookup"><span data-stu-id="76daa-142">x</span></span>    | <span data-ttu-id="76daa-143">x</span><span class="sxs-lookup"><span data-stu-id="76daa-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="76daa-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="76daa-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76daa-145">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="76daa-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 