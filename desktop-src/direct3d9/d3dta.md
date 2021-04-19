---
description: 材質引數常數會當做 D3DTEXTURESTAGESTATETYPE 列舉型別之下列成員的值使用：
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58d4d5665b1a098b84eaa95294e69220d6ea4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970114"
---
# <a name="d3dta"></a><span data-ttu-id="d5e1c-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="d5e1c-103">D3DTA</span></span>

<span data-ttu-id="d5e1c-104">材質引數常數會當做 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) 列舉型別之下列成員的值使用：</span><span class="sxs-lookup"><span data-stu-id="d5e1c-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="d5e1c-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="d5e1c-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="d5e1c-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="d5e1c-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="d5e1c-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="d5e1c-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="d5e1c-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="d5e1c-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="d5e1c-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="d5e1c-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="d5e1c-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="d5e1c-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="d5e1c-111">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="d5e1c-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="d5e1c-112">藉由呼叫 [**SetTextureStageState**](/windows/desktop/api) 和 [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) 方法來設定和取出材質引數。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="d5e1c-113">引數旗標</span><span class="sxs-lookup"><span data-stu-id="d5e1c-113">Argument flags</span></span>

<span data-ttu-id="d5e1c-114">您可以結合引數旗標與修飾詞，但無法結合兩個引數旗標。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e1c-115">\#定義</span><span class="sxs-lookup"><span data-stu-id="d5e1c-115">\#define</span></span>          | <span data-ttu-id="d5e1c-116">Description</span><span class="sxs-lookup"><span data-stu-id="d5e1c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d5e1c-117">D3DTA \_ 常數</span><span class="sxs-lookup"><span data-stu-id="d5e1c-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="d5e1c-118">從材質階段選取一個常數。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="d5e1c-119">預設值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d5e1c-120">D3DTA \_ 目前</span><span class="sxs-lookup"><span data-stu-id="d5e1c-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="d5e1c-121">材質引數是上一個混合階段的結果。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="d5e1c-122">在第一個材質階段 (階段 0) ，此引數相當於 D3DTA \_ 擴散。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="d5e1c-123">如果上一個混合階段使用 (的 D3DTOP \_) BUMPENVMAP 作業，則系統會在距離地圖材質之前選擇階段中的材質。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="d5e1c-124">如果 s 代表目前的材質階段，而 s-1 包含凹凸地圖材質，則這個引數會成為紋理階段 s-2 的結果輸出。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="d5e1c-125">許可權為讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="d5e1c-126">D3DTA \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="d5e1c-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="d5e1c-127">材質引數是在 Gouraud 網底期間，從頂點元件插入的擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="d5e1c-128">如果頂點未包含擴散色彩，預設色彩為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="d5e1c-129">許可權是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d5e1c-130">D3DTA \_ SELECTMASK</span><span class="sxs-lookup"><span data-stu-id="d5e1c-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="d5e1c-131">所有引數的遮罩值;設定材質引數時未使用。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d5e1c-132">D3DTA \_ 反光</span><span class="sxs-lookup"><span data-stu-id="d5e1c-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="d5e1c-133">材質引數是在 Gouraud 網底期間，從頂點元件插入的反射色彩。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="d5e1c-134">如果頂點未包含反射色彩，預設色彩為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="d5e1c-135">許可權是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d5e1c-136">D3DTA \_ TEMP</span><span class="sxs-lookup"><span data-stu-id="d5e1c-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="d5e1c-137">材質引數是用來讀取或寫入的臨時暫存器色彩。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="d5e1c-138">\_如果有[D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md)裝置功能，則支援 D3DTA TEMP。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="d5e1c-139">註冊的預設值是 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="d5e1c-140">許可權為讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="d5e1c-141">D3DTA \_ 材質</span><span class="sxs-lookup"><span data-stu-id="d5e1c-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="d5e1c-142">材質引數是此材質階段的材質色彩。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="d5e1c-143">許可權是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d5e1c-144">D3DTA \_ TFACTOR</span><span class="sxs-lookup"><span data-stu-id="d5e1c-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="d5e1c-145">材質引數是在上一次呼叫 [**graphicsdevice**](/windows/desktop/api) 時設定的材質因數，並具有 [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) 轉譯狀態值。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="d5e1c-146">許可權是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="d5e1c-147">修飾詞旗標</span><span class="sxs-lookup"><span data-stu-id="d5e1c-147">Modifier flags</span></span>

<span data-ttu-id="d5e1c-148">引數旗標可以與下列其中一個修飾詞旗標合併。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-148">An argument flag may be combined with one of the following modifier flags.</span></span>



|                       |                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e1c-149">\#定義</span><span class="sxs-lookup"><span data-stu-id="d5e1c-149">\#define</span></span>              | <span data-ttu-id="d5e1c-150">Description</span><span class="sxs-lookup"><span data-stu-id="d5e1c-150">Description</span></span>                                                                                                    |
| <span data-ttu-id="d5e1c-151">D3DTA \_ ALPHAREPLICATE</span><span class="sxs-lookup"><span data-stu-id="d5e1c-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="d5e1c-152">在作業完成之前，將 Alpha 資訊複寫至所有色彩通道。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="d5e1c-153">這是讀取修飾詞。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-153">This is a read modifier.</span></span> |
| <span data-ttu-id="d5e1c-154">D3DTA \_ 補數</span><span class="sxs-lookup"><span data-stu-id="d5e1c-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="d5e1c-155">取得引數 x 的補數， (1.0-x) 。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="d5e1c-156">這是讀取修飾詞。</span><span class="sxs-lookup"><span data-stu-id="d5e1c-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="d5e1c-157">常數資訊</span><span class="sxs-lookup"><span data-stu-id="d5e1c-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="d5e1c-158">標頭</span><span class="sxs-lookup"><span data-stu-id="d5e1c-158">Header</span></span>                   | <span data-ttu-id="d5e1c-159">d3d9types。h</span><span class="sxs-lookup"><span data-stu-id="d5e1c-159">d3d9types.h</span></span> |
| <span data-ttu-id="d5e1c-160">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="d5e1c-160">Minimum operating system</span></span> | <span data-ttu-id="d5e1c-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d5e1c-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="d5e1c-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5e1c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5e1c-163">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="d5e1c-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
