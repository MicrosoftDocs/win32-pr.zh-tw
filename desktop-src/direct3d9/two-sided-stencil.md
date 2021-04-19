---
description: 利用樣板緩衝區繪製陰影時將會使用到陰影錐。
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: 'Two-Sided 範本 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970515"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="984a4-103">Two-Sided 範本 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="984a4-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="984a4-104">利用樣板緩衝區繪製陰影時將會使用到陰影錐。</span><span class="sxs-lookup"><span data-stu-id="984a4-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="984a4-105">應用程式透過計算剪影的邊緣，將其往光源的反方向突出並形成一組 3D 體積的集合，進而計算遮蔽幾何物的陰影錐。</span><span class="sxs-lookup"><span data-stu-id="984a4-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="984a4-106">這些物體接著會在經過兩次的轉譯之後寫入樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="984a4-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="984a4-107">第一次轉譯會繪製面向前端的多邊形，並遞增樣板緩衝區的值。</span><span class="sxs-lookup"><span data-stu-id="984a4-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="984a4-108">第二次轉譯會繪製陰影錐面向後端的多邊形，並遞減樣板緩衝區的值。</span><span class="sxs-lookup"><span data-stu-id="984a4-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="984a4-109">一般而言，所有遞增及遞減的值會互相抵銷。不過，當陰影錐被轉譯時，場景已經在一般幾何導致某些像素無法通過 z 衝突測試時轉譯完成。</span><span class="sxs-lookup"><span data-stu-id="984a4-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="984a4-110">留在樣板緩衝區的值將會對應到陰影中的像素。</span><span class="sxs-lookup"><span data-stu-id="984a4-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="984a4-111">這些剩餘的樣板緩衝區內容會作為遮罩使用，以將一個包括所有內容的巨大黑色四元組 Alpha 混合至場景中。</span><span class="sxs-lookup"><span data-stu-id="984a4-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="984a4-112">藉由將樣板緩衝區作為遮罩，陰影中的像素將會進一步加深。</span><span class="sxs-lookup"><span data-stu-id="984a4-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="984a4-113">這表示針對每個光源，陰影幾何都會繪製兩次，因此對 GPU 的頂點輸送量形成了壓力。</span><span class="sxs-lookup"><span data-stu-id="984a4-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="984a4-114">雙面樣板便是為了避免這種情況而設計出來的功能。</span><span class="sxs-lookup"><span data-stu-id="984a4-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="984a4-115">在這種方法之下，會有兩組樣板狀態 (命名如下)：其中一組為針對每個面向前端的三角形設定的樣板狀態，另外一組則是針對面向後端的三角形。</span><span class="sxs-lookup"><span data-stu-id="984a4-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="984a4-116">如此一來，針對每個光源及每個陰影錐都只會進行一階段的繪製。</span><span class="sxs-lookup"><span data-stu-id="984a4-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="984a4-117">API 變更會限制為一組新的呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="984a4-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="984a4-118">新的轉譯狀態 D3DRS \_ 雙 \_ 側 \_ StencilMODE 可以設定為 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="984a4-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="984a4-119">預設為 **FALSE** ，表示目前 (DirectX 8) 行為。</span><span class="sxs-lookup"><span data-stu-id="984a4-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="984a4-120">當這設定為 **TRUE** 時 (只有在將 D3DSTENCILCAPS TWOSIDED 設定為 [) ] 時，才會運作 \_ ，而下列轉譯狀態只會套用至正面 (順時針) 三角形。</span><span class="sxs-lookup"><span data-stu-id="984a4-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="984a4-121">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="984a4-121">Render state</span></span>        | <span data-ttu-id="984a4-122">Description</span><span class="sxs-lookup"><span data-stu-id="984a4-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="984a4-123">D3DRS \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="984a4-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="984a4-124">如果樣板測試失敗，則為 D3DSTENCILOP。</span><span class="sxs-lookup"><span data-stu-id="984a4-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="984a4-125">D3DRS \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="984a4-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="984a4-126">如果樣板測試通過和 z 測試失敗，則為 D3DSTENCILOP。</span><span class="sxs-lookup"><span data-stu-id="984a4-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="984a4-127">D3DRS \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="984a4-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="984a4-128">如果樣板和 z 測試都通過，則 D3DSTENCILOP。</span><span class="sxs-lookup"><span data-stu-id="984a4-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="984a4-129">D3DRS \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="984a4-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="984a4-130">D3DCMPFUNC fn。</span><span class="sxs-lookup"><span data-stu-id="984a4-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="984a4-131">如果 ( (ref & mask) stencilfn (樣板 & mask) ) 為 true，則樣板測試會通過。</span><span class="sxs-lookup"><span data-stu-id="984a4-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="984a4-132">一組新的轉譯狀態會套用至反向 () 三角形的回溯方向。</span><span class="sxs-lookup"><span data-stu-id="984a4-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="984a4-133">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="984a4-133">Render state</span></span>             | <span data-ttu-id="984a4-134">Description</span><span class="sxs-lookup"><span data-stu-id="984a4-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984a4-135">D3DRS \_ CCW \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="984a4-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="984a4-136">如果樣板測試失敗，則為 D3DSTENCILOP。</span><span class="sxs-lookup"><span data-stu-id="984a4-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="984a4-137">D3DRS \_ CCW \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="984a4-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="984a4-138">如果樣板測試通過和 z 測試失敗，則為 D3DSTENCILOP。</span><span class="sxs-lookup"><span data-stu-id="984a4-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="984a4-139">D3DRS \_ CCW \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="984a4-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="984a4-140">如果樣板和 z 測試都通過，則 D3DSTENCILOP。</span><span class="sxs-lookup"><span data-stu-id="984a4-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="984a4-141">D3DRS \_ CCW \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="984a4-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="984a4-142">D3DCMPFUNC 函式。</span><span class="sxs-lookup"><span data-stu-id="984a4-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="984a4-143">如果 ( (ref & mask) stencilfn (樣板 & mask) ) 為 true，則樣板測試會通過。</span><span class="sxs-lookup"><span data-stu-id="984a4-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="984a4-144">其餘的樣板呈現狀態一律會套用至順時針和逆時針三角形。</span><span class="sxs-lookup"><span data-stu-id="984a4-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="984a4-145">D3DRS \_ \_ \_ 會忽略行和點 sprite 的雙側 StencilMODE，這表示行為與 DirectX 8 不相同。</span><span class="sxs-lookup"><span data-stu-id="984a4-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="984a4-146">D3DRS \_ CCW 樣板 \_ 轉譯 \* 狀態會被忽略。</span><span class="sxs-lookup"><span data-stu-id="984a4-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="984a4-147">新的 cap 位表示裝置是否支援此功能。</span><span class="sxs-lookup"><span data-stu-id="984a4-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="984a4-148">不支援這項功能的驅動程式應該忽略這些新的呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="984a4-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="984a4-149">所有其他樣板的 cap 位都適用于兩種樣板緩衝模式。</span><span class="sxs-lookup"><span data-stu-id="984a4-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="984a4-150">因為兩個 \_ 側邊樣板 \_ 表示可以使用 D3DCULLMODE \_ NONE set 來繪製，所以如果它支援這個新的樣板模式，則必須由驅動程式設定對應的端點。</span><span class="sxs-lookup"><span data-stu-id="984a4-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="984a4-151">Microsoft Windows 硬體品質實驗室 (WHQL) 應該強制執行這種情況。</span><span class="sxs-lookup"><span data-stu-id="984a4-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="984a4-152">新的呈現狀態：</span><span class="sxs-lookup"><span data-stu-id="984a4-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="984a4-153">新 cap：</span><span class="sxs-lookup"><span data-stu-id="984a4-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="984a4-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="984a4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="984a4-155">樣板緩衝區技術</span><span class="sxs-lookup"><span data-stu-id="984a4-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="984a4-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="984a4-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
