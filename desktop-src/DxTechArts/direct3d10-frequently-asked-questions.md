---
title: Direct3D 10 常見問題集
description: 本文包含有關 Direct3D 10 的一些常見問題，從 Direct3D 9 (D3D9) 移植現有的應用程式，到 Direct3D 10 (D3D10) 。
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092860"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="54eef-103">Direct3D 10 常見問題集</span><span class="sxs-lookup"><span data-stu-id="54eef-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="54eef-104">本文包含有關 Direct3D 10 的一些常見問題，從 Direct3D 9 (D3D9) 移植現有的應用程式，到 Direct3D 10 (D3D10) 。</span><span class="sxs-lookup"><span data-stu-id="54eef-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="54eef-105">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="54eef-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="54eef-106">State</span><span class="sxs-lookup"><span data-stu-id="54eef-106">State</span></span>](#state)
-   [<span data-ttu-id="54eef-107">格式</span><span class="sxs-lookup"><span data-stu-id="54eef-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="54eef-108">著色器連結</span><span class="sxs-lookup"><span data-stu-id="54eef-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="54eef-109">繪製呼叫</span><span class="sxs-lookup"><span data-stu-id="54eef-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="54eef-110">資源</span><span class="sxs-lookup"><span data-stu-id="54eef-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="54eef-111">深度為材質</span><span class="sxs-lookup"><span data-stu-id="54eef-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="54eef-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="54eef-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="54eef-113">損毀</span><span class="sxs-lookup"><span data-stu-id="54eef-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="54eef-114">前提轉譯</span><span class="sxs-lookup"><span data-stu-id="54eef-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="54eef-115">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="54eef-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="54eef-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="54eef-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="54eef-117">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="54eef-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="54eef-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>更新常數緩衝區的最佳方式是什麼？</span><span class="sxs-lookup"><span data-stu-id="54eef-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="54eef-119">使用捨棄的 UpdateSubresource 和 Map 應該會有相同的速度。</span><span class="sxs-lookup"><span data-stu-id="54eef-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="54eef-120">根據哪一個複製最少的記憶體量，在兩者之間進行選擇。</span><span class="sxs-lookup"><span data-stu-id="54eef-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="54eef-121">如果您已將資料儲存在記憶體中的一個連續區塊中，請使用 UpdateSubresource。</span><span class="sxs-lookup"><span data-stu-id="54eef-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="54eef-122">如果您需要從其他位置累積資料，請使用 Map 來捨棄。</span><span class="sxs-lookup"><span data-stu-id="54eef-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>組織常數緩衝區最差的方式為何？</span><span class="sxs-lookup"><span data-stu-id="54eef-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="54eef-124">將特定著色器的所有常數放入一個常數緩衝區，可實現最差的效能。</span><span class="sxs-lookup"><span data-stu-id="54eef-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="54eef-125">雖然這通常是從 D3D9 移植至 D3D10 最簡單的方式，但它可能會使效能癱瘓。</span><span class="sxs-lookup"><span data-stu-id="54eef-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="54eef-126">例如，假設有一個使用下列常數緩衝區的案例：</span><span class="sxs-lookup"><span data-stu-id="54eef-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="54eef-127">緩衝區為6560個位元組。</span><span class="sxs-lookup"><span data-stu-id="54eef-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="54eef-128">假設有一個應用程式具有要轉譯的1000物件，100個是 skinned 網格，而900則為靜態網格。</span><span class="sxs-lookup"><span data-stu-id="54eef-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="54eef-129">此外，假設此應用程式使用陰影對應搭配一個光源。</span><span class="sxs-lookup"><span data-stu-id="54eef-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="54eef-130">這表示有兩個行程，一個用於從光源所呈現的深度地圖，另一個用於向前轉譯行程。</span><span class="sxs-lookup"><span data-stu-id="54eef-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="54eef-131">這會導致2000繪製呼叫。</span><span class="sxs-lookup"><span data-stu-id="54eef-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="54eef-132">雖然每個繪製呼叫不需要更新常數緩衝區的每個部分，但是整個常數緩衝區仍會更新並傳送到卡片。</span><span class="sxs-lookup"><span data-stu-id="54eef-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="54eef-133">這會導致每個畫面格更新 13 MB 的資料， (2000 繪製呼叫乘以 6560 KB) 。</span><span class="sxs-lookup"><span data-stu-id="54eef-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="54eef-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>組織常數緩衝區的最佳方式是什麼？</span><span class="sxs-lookup"><span data-stu-id="54eef-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="54eef-135">最佳方式是依更新頻率來組織常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="54eef-136">以類似頻率更新的常數應該在相同的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="54eef-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="54eef-137">例如，請考慮以下的案例：「組織常數緩衝區有何最差的方法？」，但有更好的配置：</span><span class="sxs-lookup"><span data-stu-id="54eef-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="54eef-138">常數緩衝區依其更新頻率分割，但這只是解決方案的一半。</span><span class="sxs-lookup"><span data-stu-id="54eef-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="54eef-139">應用程式需要正確更新常數緩衝區，才能充分利用分割。</span><span class="sxs-lookup"><span data-stu-id="54eef-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="54eef-140">我們會假設與上面相同的場景：900靜態網格、100 skinned 網格、一次輕量，以及一次向前傳遞。</span><span class="sxs-lookup"><span data-stu-id="54eef-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="54eef-141">我們也會假設會儲存每個物件的一些常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="54eef-142">這表示，每個物件都會包含 VSPerSkinnedCB 或 VSPerStaticCB，視其為 skinned 或靜態而定。</span><span class="sxs-lookup"><span data-stu-id="54eef-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="54eef-143">這麼做是為了避免透過管線傳送的矩陣數量加倍。</span><span class="sxs-lookup"><span data-stu-id="54eef-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="54eef-144">我們將框架分成三個階段。</span><span class="sxs-lookup"><span data-stu-id="54eef-144">We split the frame into three phases.</span></span> <span data-ttu-id="54eef-145">第一個階段是框架的開頭，且不包含任何轉譯，而只是持續更新。</span><span class="sxs-lookup"><span data-stu-id="54eef-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="54eef-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**開始畫面格**</span><span class="sxs-lookup"><span data-stu-id="54eef-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="54eef-147"> (4 個位元組的應用程式時間更新 VSGlobalPerFrameCB) </span><span class="sxs-lookup"><span data-stu-id="54eef-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="54eef-148">100 skinned 物件的更新 100 VSPerSkinnedCB (640000 個位元組) </span><span class="sxs-lookup"><span data-stu-id="54eef-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="54eef-149">900靜態物件的更新 VSPerStaticCB (57600 位元組) </span><span class="sxs-lookup"><span data-stu-id="54eef-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="54eef-150">接下來是陰影地圖傳遞。</span><span class="sxs-lookup"><span data-stu-id="54eef-150">Next is the shadow map pass.</span></span> <span data-ttu-id="54eef-151">請注意，實際更新的唯一常數緩衝區是 VSPerPassCB。</span><span class="sxs-lookup"><span data-stu-id="54eef-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="54eef-152">所有其他常數緩衝區都已在開始框架傳遞期間更新。</span><span class="sxs-lookup"><span data-stu-id="54eef-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="54eef-153">雖然我們仍然需要系結這些常數緩衝區，但傳遞至視訊卡的資訊量很少，因為已更新緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**陰影傳遞**</span><span class="sxs-lookup"><span data-stu-id="54eef-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="54eef-155">更新 VSPerPassCB (72 個位元組) </span><span class="sxs-lookup"><span data-stu-id="54eef-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="54eef-156">繪製 100 skinned 網格 (100 系結，沒有更新) </span><span class="sxs-lookup"><span data-stu-id="54eef-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="54eef-157">繪製900靜態網格 (100 系結，沒有更新) </span><span class="sxs-lookup"><span data-stu-id="54eef-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="54eef-158">同樣地，向前轉譯傳遞只需要更新每個材質的資料，因為它不會儲存在每個網格中。</span><span class="sxs-lookup"><span data-stu-id="54eef-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="54eef-159">假設在場景中使用500材質：</span><span class="sxs-lookup"><span data-stu-id="54eef-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="54eef-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**向前傳遞**</span><span class="sxs-lookup"><span data-stu-id="54eef-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="54eef-161">更新 VSPerPassCB (72 個位元組) </span><span class="sxs-lookup"><span data-stu-id="54eef-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="54eef-162">更新 500 VSPerMaterialCBs (10000 位元組) </span><span class="sxs-lookup"><span data-stu-id="54eef-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="54eef-163">這會導致總共只有 707 KB。</span><span class="sxs-lookup"><span data-stu-id="54eef-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="54eef-164">雖然這是非常假設的案例，但它會透過依更新頻率排序常數，來說明可減少多少常數的更新負擔。</span><span class="sxs-lookup"><span data-stu-id="54eef-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="54eef-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>如果我沒有足夠的空間來儲存網格、材質等的個別常數緩衝區，該怎麼辦？</span><span class="sxs-lookup"><span data-stu-id="54eef-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-166">您一律可以使用常數緩衝區的分層式系統。</span><span class="sxs-lookup"><span data-stu-id="54eef-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="54eef-167">建立變動大小的常數緩衝區 (16 個位元組、32個位元組、64個位元組，依此類推，) 最多需要最大的常數緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="54eef-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="54eef-168">當您將常數緩衝區系結至著色器時，請選取可保存著色器所需資料的最小常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="54eef-169">雖然這種方法的效率稍微低，但這是不錯的中間步驟。</span><span class="sxs-lookup"><span data-stu-id="54eef-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>我在不同的著色器之間共用了常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="54eef-171">一個著色器可能會使用所有常數，但另一個著色器可能會使用某些常數。</span><span class="sxs-lookup"><span data-stu-id="54eef-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="54eef-172">更新這些專案的最佳方式是什麼？</span><span class="sxs-lookup"><span data-stu-id="54eef-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-173">其中一個方法是更進一步分割常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="54eef-174">不過，有太多常數緩衝區系結的點。</span><span class="sxs-lookup"><span data-stu-id="54eef-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="54eef-175">在此情況下，請將很多著色器未使用的常數，移至常數緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="54eef-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="54eef-176">從著色器取得變數資料時，請使用 \_ \_ D3D10 著色器變數 DESC 中的 D3D10 SVF 使用旗標 \_ \_ \_ 來判斷變數是否已使用。</span><span class="sxs-lookup"><span data-stu-id="54eef-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="54eef-177">藉由在常數緩衝區的結尾放置未使用的變數，您可以將較小的緩衝區系結至不使用這些變數的著色器，藉此節省更新成本。</span><span class="sxs-lookup"><span data-stu-id="54eef-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>如果每個畫面上只上傳一次字元的骨骼，而不是每次通過/繪製一次，則可以改善畫面播放速率的大小？</span><span class="sxs-lookup"><span data-stu-id="54eef-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-179">您可以根據多餘的資料量，改善介於8% 到50% 之間的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="54eef-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="54eef-180">在最糟的情況下，效能不會降低。</span><span class="sxs-lookup"><span data-stu-id="54eef-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>我應該同時系結多少常數緩衝區？</span><span class="sxs-lookup"><span data-stu-id="54eef-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-182">系結取得所有資料到著色器所花費的常數緩衝區數目下限。</span><span class="sxs-lookup"><span data-stu-id="54eef-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="54eef-183">在實際案例中，建議使用五個常數緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="54eef-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="54eef-184">在著色器之間共用常數緩衝區 (將相同的 CB 系結至 VS 和 PS) 也可以改善效能。</span><span class="sxs-lookup"><span data-stu-id="54eef-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>系結常數緩衝區是否有成本，而不使用它們？</span><span class="sxs-lookup"><span data-stu-id="54eef-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-186">是的，如果您不想要使用緩衝區，請不要呼叫 VSSetConsantBuffer 或 PSSetConstantBuffer。</span><span class="sxs-lookup"><span data-stu-id="54eef-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="54eef-187">這項額外的 API 額外負荷可能會在多個繪製呼叫的過程中增加。</span><span class="sxs-lookup"><span data-stu-id="54eef-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="54eef-188">狀態</span><span class="sxs-lookup"><span data-stu-id="54eef-188">State</span></span>

<dl> <dt>

<span data-ttu-id="54eef-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>在 D3D10 中管理狀態的最佳方式為何？</span><span class="sxs-lookup"><span data-stu-id="54eef-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-190">最好的解決方法是事先瞭解所有的狀態，然後事先建立狀態物件。</span><span class="sxs-lookup"><span data-stu-id="54eef-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="54eef-191">這表示在轉譯時期，狀態系結是唯一需要發生的作業。</span><span class="sxs-lookup"><span data-stu-id="54eef-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="54eef-192">D3D10 也會篩選出重複的專案。</span><span class="sxs-lookup"><span data-stu-id="54eef-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>我的遊戲動態載入或具有使用者產生的內容。</span><span class="sxs-lookup"><span data-stu-id="54eef-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="54eef-194">我無法提前載入所有的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="54eef-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="54eef-195">我該怎麼辦？</span><span class="sxs-lookup"><span data-stu-id="54eef-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-196">這裡有兩個解決方案。</span><span class="sxs-lookup"><span data-stu-id="54eef-196">There are two solutions here.</span></span> <span data-ttu-id="54eef-197">第一種方式是立即建立狀態物件，並讓 D3D10 篩選出重複的專案。</span><span class="sxs-lookup"><span data-stu-id="54eef-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="54eef-198">但是，不建議在每個畫面上有許多狀態物件變更的案例中使用。</span><span class="sxs-lookup"><span data-stu-id="54eef-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="54eef-199">更好的解決方法是在雜湊表中找不到符合需求的狀態物件時自行進行雜湊處理，並建立狀態物件。</span><span class="sxs-lookup"><span data-stu-id="54eef-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="54eef-200">使用自訂雜湊表的原因是，應用程式可以根據特定應用程式的使用案例來選取快速雜湊。</span><span class="sxs-lookup"><span data-stu-id="54eef-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="54eef-201">例如，如果應用程式只變更 BlendState 中的 rendertargetwritemask，並保留所有其他值，則應用程式可以從 rendertargetwritemask 產生雜湊，而不是整個結構。</span><span class="sxs-lookup"><span data-stu-id="54eef-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest 狀態已消失。</span><span class="sxs-lookup"><span data-stu-id="54eef-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="54eef-203">它在哪裡？</span><span class="sxs-lookup"><span data-stu-id="54eef-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-204">AlphaTest 現在應該是著色器中的效能。</span><span class="sxs-lookup"><span data-stu-id="54eef-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="54eef-205">請參閱 FixedFuncEMU 範例。</span><span class="sxs-lookup"><span data-stu-id="54eef-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>使用者裁剪平面發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="54eef-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-207">使用者裁剪平面已移至著色器。</span><span class="sxs-lookup"><span data-stu-id="54eef-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="54eef-208">有兩種方式可以處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="54eef-208">There are two ways to handle this.</span></span> <span data-ttu-id="54eef-209">第一個是 \_ 從頂點著色器或幾何著色器輸出 SV ClipDistance。</span><span class="sxs-lookup"><span data-stu-id="54eef-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="54eef-210">另一個選項是在圖元著色器中使用 [捨棄]，並根據頂點著色器或幾何著色器所傳遞的某個值。</span><span class="sxs-lookup"><span data-stu-id="54eef-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="54eef-211">進行這兩者的實驗，以查看您的特定案例更快。</span><span class="sxs-lookup"><span data-stu-id="54eef-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="54eef-212">使用 SV \_ ClipDistance 可能會導致硬體使用以幾何為基礎的裁剪常式，而這可能會造成幾何系結繪製呼叫的執行速度變慢。</span><span class="sxs-lookup"><span data-stu-id="54eef-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="54eef-213">同樣地，使用「捨棄」會將工作移至圖元著色器，這可能會造成圖元系結的繪製呼叫執行速度較慢。</span><span class="sxs-lookup"><span data-stu-id="54eef-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>清除不遵守任何狀態設定，例如我的轉譯器狀態中的剪式矩形設定。</span><span class="sxs-lookup"><span data-stu-id="54eef-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-215">清除已與管線狀態分開。</span><span class="sxs-lookup"><span data-stu-id="54eef-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="54eef-216">為了取得 D3D9 樣式的行為，請藉由繪製全螢幕的四種方式來清除。</span><span class="sxs-lookup"><span data-stu-id="54eef-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>我將狀態設回預設值，以嘗試診斷轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="54eef-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="54eef-218">現在我的畫面只會顯示黑色，雖然我知道要在螢幕上繪製物件。</span><span class="sxs-lookup"><span data-stu-id="54eef-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-219">將狀態設回預設值 (Null) 時，請確定 OMSetBlendState 呼叫中的 SampleMask 永遠不會是零。</span><span class="sxs-lookup"><span data-stu-id="54eef-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="54eef-220">如果 SampleMask 設定為零，則所有範例都會以邏輯方式與零。</span><span class="sxs-lookup"><span data-stu-id="54eef-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="54eef-221">在此案例中，沒有任何範例會通過 blend 測試。</span><span class="sxs-lookup"><span data-stu-id="54eef-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>D3DSAMP \_ SRGBTEXTURE 狀態在哪裡？</span><span class="sxs-lookup"><span data-stu-id="54eef-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-223">已移除 SRGB 作為取樣器狀態的一部分，現在會系結至材質格式。</span><span class="sxs-lookup"><span data-stu-id="54eef-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="54eef-224">如果您 \_ 在 Direct3D 9 中指定了 D3DSAMP SRGBTEXTURE，系結 SRGB 材質將會產生相同的取樣。</span><span class="sxs-lookup"><span data-stu-id="54eef-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="54eef-225">格式</span><span class="sxs-lookup"><span data-stu-id="54eef-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="54eef-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>哪一種 D3D9 格式對應至哪個 D3D10 格式？</span><span class="sxs-lookup"><span data-stu-id="54eef-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-227">如需詳細資訊，請參閱 [direct3d 9 至 direct3d 10 考慮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations)。</span><span class="sxs-lookup"><span data-stu-id="54eef-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="54eef-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>A8R8G8B8 紋理格式有何變化？</span><span class="sxs-lookup"><span data-stu-id="54eef-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-229">它們在 D3D10 中已被取代。</span><span class="sxs-lookup"><span data-stu-id="54eef-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="54eef-230">您可以將紋理以 R8G8B8A8 的形式重新來源，或者可以在載入時 swizzle，也可以在著色器中 swizzle。</span><span class="sxs-lookup"><span data-stu-id="54eef-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>如何? 使用調色盤材質？</span><span class="sxs-lookup"><span data-stu-id="54eef-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-232">將您的色板置於材質或常數緩衝區，並將其系結至管線。</span><span class="sxs-lookup"><span data-stu-id="54eef-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="54eef-233">在圖元著色器中，使用調色盤材質中的索引進行間接查閱。</span><span class="sxs-lookup"><span data-stu-id="54eef-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>這些新的 SRGB 格式有哪些？</span><span class="sxs-lookup"><span data-stu-id="54eef-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-235">已將 SRGB 移除為取樣器狀態的一部分，而且現在已系結至材質格式。</span><span class="sxs-lookup"><span data-stu-id="54eef-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="54eef-236">如果您 \_ 在 Direct3D 9 中指定了 D3DSAMP SRGBTEXTURE，系結 SRGB 材質將會產生相同的取樣。</span><span class="sxs-lookup"><span data-stu-id="54eef-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>三角形風扇在哪裡去了？</span><span class="sxs-lookup"><span data-stu-id="54eef-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-238">三角形在 D3D10 中已被取代。</span><span class="sxs-lookup"><span data-stu-id="54eef-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="54eef-239">三角形的風扇必須在內容管線或載入時進行轉換。</span><span class="sxs-lookup"><span data-stu-id="54eef-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="54eef-240">著色器連結</span><span class="sxs-lookup"><span data-stu-id="54eef-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="54eef-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>我的 Direct3D 9 著色器可以編譯為著色器模型4.0，但是當我將它們系結至管線時，會出現在偵錯工具中使用偵錯工具執行時間顯示的連結錯誤。</span><span class="sxs-lookup"><span data-stu-id="54eef-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-242">著色器連結在 D3D10 中更嚴格。</span><span class="sxs-lookup"><span data-stu-id="54eef-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="54eef-243">後續階段中的元素必須以其從上一個階段輸出的順序來讀取。</span><span class="sxs-lookup"><span data-stu-id="54eef-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="54eef-244">例如：</span><span class="sxs-lookup"><span data-stu-id="54eef-244">For example:</span></span>

<span data-ttu-id="54eef-245">頂點著色器輸出：</span><span class="sxs-lookup"><span data-stu-id="54eef-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="54eef-246">圖元著色器會讀取：</span><span class="sxs-lookup"><span data-stu-id="54eef-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="54eef-247">雖然圖元著色器中不需要位置，但這會導致連結錯誤，因為位置是從頂點著色器輸出，而不是由圖元著色器讀取。</span><span class="sxs-lookup"><span data-stu-id="54eef-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="54eef-248">更正確的版本看起來會像這樣：</span><span class="sxs-lookup"><span data-stu-id="54eef-248">The more correct version would look like this:</span></span>

<span data-ttu-id="54eef-249">頂點著色器輸出：</span><span class="sxs-lookup"><span data-stu-id="54eef-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="54eef-250">圖元著色器會讀取：</span><span class="sxs-lookup"><span data-stu-id="54eef-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="54eef-251">在此情況下，頂點著色器會輸出相同的資訊，但現在圖元著色器會在訂單輸出中讀取專案。</span><span class="sxs-lookup"><span data-stu-id="54eef-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="54eef-252">由於圖元著色器在 Tex 之後不會讀取任何內容，因此我們不需要擔心 VS 所輸出的資訊會比 PS 正在讀取的還多。</span><span class="sxs-lookup"><span data-stu-id="54eef-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>我需要著色器簽章才能建立輸入版面配置，但我會在建立著色器之前載入網格，並建立版面配置。</span><span class="sxs-lookup"><span data-stu-id="54eef-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="54eef-254">該怎麼辦？</span><span class="sxs-lookup"><span data-stu-id="54eef-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-255">其中一個解決方法是在載入網格之前切換訂單和載入著色器。</span><span class="sxs-lookup"><span data-stu-id="54eef-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="54eef-256">不過，這種方式比完成的簡單得多。</span><span class="sxs-lookup"><span data-stu-id="54eef-256">However, this is much easier said than done.</span></span> <span data-ttu-id="54eef-257">您隨時都可以視需要建立應用程式所需的輸入版面配置。</span><span class="sxs-lookup"><span data-stu-id="54eef-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="54eef-258">您必須保留一個版本的著色器簽章。</span><span class="sxs-lookup"><span data-stu-id="54eef-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="54eef-259">您應該根據著色器和緩衝區配置建立雜湊，而且只有當相符專案尚未存在時，才會建立輸入版面配置。</span><span class="sxs-lookup"><span data-stu-id="54eef-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="54eef-260">繪製呼叫</span><span class="sxs-lookup"><span data-stu-id="54eef-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="54eef-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>D3D10 到達 60 Hz 的繪製通話限制為何？</span><span class="sxs-lookup"><span data-stu-id="54eef-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="54eef-262">30 Hz？</span><span class="sxs-lookup"><span data-stu-id="54eef-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-263">由於每個繪製呼叫的 CPU 成本，Direct3D 9 對繪製呼叫的數目有限制。</span><span class="sxs-lookup"><span data-stu-id="54eef-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="54eef-264">在 Direct3D 10 上，每個繪製呼叫的成本都已減少。</span><span class="sxs-lookup"><span data-stu-id="54eef-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="54eef-265">不過，繪製呼叫和畫面播放速率之間不再有明確的關聯性。</span><span class="sxs-lookup"><span data-stu-id="54eef-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="54eef-266">由於繪製呼叫通常需要許多支援呼叫 ( 常數緩衝區更新、材質系結、狀態設定等等) 因此，API 的畫面播放速率影響現在更相依于整體的 API 使用方式，而不只是繪製呼叫計數。</span><span class="sxs-lookup"><span data-stu-id="54eef-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="54eef-267">資源</span><span class="sxs-lookup"><span data-stu-id="54eef-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="54eef-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>我應該使用何種資源使用類型來執行哪些作業？</span><span class="sxs-lookup"><span data-stu-id="54eef-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-269">使用下列內容頁：</span><span class="sxs-lookup"><span data-stu-id="54eef-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="54eef-270">CPU 會每個畫面更新一次以上的資源： D3D10 \_ 使用量 \_ 動態</span><span class="sxs-lookup"><span data-stu-id="54eef-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="54eef-271">CPU 會將每個畫面格的資源更新為小於一次： D3D10 \_ 使用量 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="54eef-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="54eef-272">CPU 不會更新資源： D3D10 使用方式 \_ \_ 不可變</span><span class="sxs-lookup"><span data-stu-id="54eef-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="54eef-273">CPU 需要讀取資源： D3D10 \_ 使用量 \_ 暫存</span><span class="sxs-lookup"><span data-stu-id="54eef-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="54eef-274">因為常數緩衝區一律會經常更新，所以它們不符合「操作簡介」。</span><span class="sxs-lookup"><span data-stu-id="54eef-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="54eef-275">針對要用於常數緩衝區的資源類型，請參閱 [常數緩衝區](#constant-buffers) 區段。</span><span class="sxs-lookup"><span data-stu-id="54eef-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>DrawPrimitiveUP 和 DrawIndexedPrimitiveUP 會發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="54eef-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-277">它們 D3D10。</span><span class="sxs-lookup"><span data-stu-id="54eef-277">They are gone in D3D10.</span></span> <span data-ttu-id="54eef-278">若為動態幾何，請使用大型 D3D10 \_ 使用 \_ 動態緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="54eef-279">在框架的開頭，將它與 D3D10 \_ map \_ WRITE 捨棄進行對應 \_ 。</span><span class="sxs-lookup"><span data-stu-id="54eef-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="54eef-280">針對每個後續的繪製呼叫，將寫入指標提前超過先前繪製頂點的位置，並將緩衝區與 D3D10 \_ 對應 \_ 寫入 [ \_ 不覆寫] \_ 。</span><span class="sxs-lookup"><span data-stu-id="54eef-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="54eef-281">如果您接近框架結尾之前的緩衝區結尾，請將寫入指標包裝到開頭和 map，並 D3D10 \_ 對應 \_ 寫入 \_ 捨棄。</span><span class="sxs-lookup"><span data-stu-id="54eef-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>我可以將16位的索引和32位索引寫入相同的動態幾何緩衝區嗎？</span><span class="sxs-lookup"><span data-stu-id="54eef-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-283">是的，您可以，但這可能會對特定硬體造成效能上的影響。</span><span class="sxs-lookup"><span data-stu-id="54eef-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="54eef-284">針對動態16位索引資料和32位索引資料建立不同的緩衝區是比較安全的做法。</span><span class="sxs-lookup"><span data-stu-id="54eef-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>如何? 從 GPU 將資料讀取回 CPU？</span><span class="sxs-lookup"><span data-stu-id="54eef-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-286">您必須使用暫存資源。</span><span class="sxs-lookup"><span data-stu-id="54eef-286">You must use a staging resource.</span></span> <span data-ttu-id="54eef-287">使用 CopyResource 將資料從 GPU 資源複製到預備資源。</span><span class="sxs-lookup"><span data-stu-id="54eef-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="54eef-288">對應暫存資源以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="54eef-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>我的應用程式相依于 StretchRect 功能。</span><span class="sxs-lookup"><span data-stu-id="54eef-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-290">因為這本質上是基本 Direct3D 功能的包裝函式，所以已從 API 中移除。</span><span class="sxs-lookup"><span data-stu-id="54eef-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="54eef-291">部分 StretchRect 功能已移至 D3DX10LoadTextureFromTexture。</span><span class="sxs-lookup"><span data-stu-id="54eef-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="54eef-292">針對格式轉換和複製材質，D3DX10LoadTextureFromTexture 可能會進行工作。</span><span class="sxs-lookup"><span data-stu-id="54eef-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="54eef-293">不過，從某個大小轉換成另一種大小的作業，可能需要在應用程式中轉譯成材質。</span><span class="sxs-lookup"><span data-stu-id="54eef-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>資源的地圖呼叫沒有位移或大小。</span><span class="sxs-lookup"><span data-stu-id="54eef-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="54eef-295">這些都是在 Direct3D 9 上的鎖定呼叫;為何會變更？</span><span class="sxs-lookup"><span data-stu-id="54eef-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-296">在 Direct3D 9 上鎖定呼叫的位移和大小基本上是 API 雜亂的，且驅動程式通常會忽略此情形。</span><span class="sxs-lookup"><span data-stu-id="54eef-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="54eef-297">您應改為從 Map 呼叫中傳回的指標來計算位移。</span><span class="sxs-lookup"><span data-stu-id="54eef-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="54eef-298">深度為材質</span><span class="sxs-lookup"><span data-stu-id="54eef-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="54eef-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>速度更快？</span><span class="sxs-lookup"><span data-stu-id="54eef-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="54eef-300">使用深度作為材質或將深度寫到 Alpha 並閱讀</span><span class="sxs-lookup"><span data-stu-id="54eef-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-301">這是應用程式和硬體特有的。</span><span class="sxs-lookup"><span data-stu-id="54eef-301">This is application and hardware specific.</span></span> <span data-ttu-id="54eef-302">使用哪一個可節省最多頻寬。</span><span class="sxs-lookup"><span data-stu-id="54eef-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="54eef-303">如果您已經使用多個轉譯目標並有額外的通道，則從著色器寫入深度可能是較佳的解決方案。</span><span class="sxs-lookup"><span data-stu-id="54eef-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="54eef-304">此外，將深度寫到 Alpha 或其他轉譯目標，可讓您撰寫線性深度值，以加速需要存取深度緩衝區的計算。</span><span class="sxs-lookup"><span data-stu-id="54eef-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>是否可以將材質系結為輸入，並將其系結為深度樣板材質（只要我停用深度寫入）？</span><span class="sxs-lookup"><span data-stu-id="54eef-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-306">不在 D3D10 中。</span><span class="sxs-lookup"><span data-stu-id="54eef-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="54eef-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="54eef-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="54eef-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>我可以解析 MSAA 深度樣板材質嗎？</span><span class="sxs-lookup"><span data-stu-id="54eef-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-309">不在 D3D10 中。</span><span class="sxs-lookup"><span data-stu-id="54eef-309">Not in D3D10.</span></span> <span data-ttu-id="54eef-310">不過，您可以從 MSAA 材質取樣個別樣本。</span><span class="sxs-lookup"><span data-stu-id="54eef-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="54eef-311">如需詳細資訊，請參閱 [HLSL](#hlsl) 一節。</span><span class="sxs-lookup"><span data-stu-id="54eef-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>為什麼我的應用程式在啟用 MSAA 時立即損毀？</span><span class="sxs-lookup"><span data-stu-id="54eef-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-313">確定您要啟用由驅動程式所列舉的 MSAA 樣本計數和品質數位。</span><span class="sxs-lookup"><span data-stu-id="54eef-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="54eef-314">損毀</span><span class="sxs-lookup"><span data-stu-id="54eef-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="54eef-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>我的應用程式在 D3D10 或驅動程式中損毀，但我不知道原因。</span><span class="sxs-lookup"><span data-stu-id="54eef-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-316">第一個步驟是啟用將偵錯工具執行時間 ([**D3D10 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) 程式旗標傳入 [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)) 。</span><span class="sxs-lookup"><span data-stu-id="54eef-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="54eef-317">這會將最常見的錯誤公開為 debug 輸出。</span><span class="sxs-lookup"><span data-stu-id="54eef-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>當我嘗試搭配使用我的應用程式與應用程式時，PIX 會當機。</span><span class="sxs-lookup"><span data-stu-id="54eef-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-319">第一個步驟是啟用將偵錯工具執行時間 ([**D3D10 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) 程式旗標傳入 [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)) 。</span><span class="sxs-lookup"><span data-stu-id="54eef-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="54eef-320">如果偵錯工具輸出不幹淨，PIX 有更高的損毀可能性。</span><span class="sxs-lookup"><span data-stu-id="54eef-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>我的遊戲在 D3D10 的32位 Vista 上的虛擬位址空間不足。</span><span class="sxs-lookup"><span data-stu-id="54eef-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="54eef-322">在 D3D9 上沒有任何問題。</span><span class="sxs-lookup"><span data-stu-id="54eef-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-323">D3D10 和虛擬位址空間有一些問題。</span><span class="sxs-lookup"><span data-stu-id="54eef-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="54eef-324">這已在 [KB940105](https://support.microsoft.com/kb/940105)中修正。</span><span class="sxs-lookup"><span data-stu-id="54eef-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="54eef-325">如果這無法修正您的問題，請確定您未在 D3D10 中建立更多可對應 (鎖定) 的資源，而不是在 D3D9 中建立。</span><span class="sxs-lookup"><span data-stu-id="54eef-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="54eef-326">也請考慮移植到64位，因為這會在未來更普遍。</span><span class="sxs-lookup"><span data-stu-id="54eef-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="54eef-327">前提轉譯</span><span class="sxs-lookup"><span data-stu-id="54eef-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="54eef-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>我使用前提轉譯 (根據遮蔽查詢結果) 。</span><span class="sxs-lookup"><span data-stu-id="54eef-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="54eef-329">為什麼我的應用程式仍然是一樣的速度？</span><span class="sxs-lookup"><span data-stu-id="54eef-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-330">首先，請確定您想要跳過的呈現實際上是應用程式瓶頸。</span><span class="sxs-lookup"><span data-stu-id="54eef-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="54eef-331">如果不是瓶頸，則略過轉譯將無法協助畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="54eef-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="54eef-332">其次，請確定在您想要述詞的查詢和轉譯的問題之間，已經過足夠的時間。</span><span class="sxs-lookup"><span data-stu-id="54eef-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="54eef-333">如果查詢在轉譯呼叫到達 GPU 時未完成，則仍會進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="54eef-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="54eef-334">第三，predication 只會略過特定的呼叫。</span><span class="sxs-lookup"><span data-stu-id="54eef-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="54eef-335">略過的呼叫為 Draw、Clear、Copy、Update、ResolveSubresource 和 GenerateMips。</span><span class="sxs-lookup"><span data-stu-id="54eef-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="54eef-336">狀態設定、IA 安裝、對應和建立呼叫不遵守 predication。</span><span class="sxs-lookup"><span data-stu-id="54eef-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="54eef-337">如果要前提繪製呼叫周圍有許多狀態設定呼叫，仍會設定這些狀態。</span><span class="sxs-lookup"><span data-stu-id="54eef-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="54eef-338">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="54eef-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="54eef-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>我應該使用幾何著色器來 tessellate 我的 (在此處插入任何內容) ？</span><span class="sxs-lookup"><span data-stu-id="54eef-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-340">不會。</span><span class="sxs-lookup"><span data-stu-id="54eef-340">No.</span></span> <span data-ttu-id="54eef-341">幾何著色器不應該用於鑲嵌式。</span><span class="sxs-lookup"><span data-stu-id="54eef-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>我可以使用幾何著色器來建立幾何嗎？</span><span class="sxs-lookup"><span data-stu-id="54eef-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-343">是，在極少數的案例中。</span><span class="sxs-lookup"><span data-stu-id="54eef-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="54eef-344">目前 D3D10 中的幾何著色器 (2008) 元件並沒有處理許多擴充的能力。</span><span class="sxs-lookup"><span data-stu-id="54eef-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="54eef-345">未來可能會變更。</span><span class="sxs-lookup"><span data-stu-id="54eef-345">This may change in the future.</span></span> <span data-ttu-id="54eef-346">由於現有的點 sprite 硬體，視訊卡廠商可能會有一到四個擴充的特殊路徑。</span><span class="sxs-lookup"><span data-stu-id="54eef-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="54eef-347">任何其他擴充都必須非常有限。</span><span class="sxs-lookup"><span data-stu-id="54eef-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="54eef-348">ParticlesGS 和 PipesGS 範例只會執行有限的擴充，以達到高框架速率。</span><span class="sxs-lookup"><span data-stu-id="54eef-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="54eef-349">每個畫面格只會展開一些點。</span><span class="sxs-lookup"><span data-stu-id="54eef-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>如何使用幾何著色器？</span><span class="sxs-lookup"><span data-stu-id="54eef-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-351">需要對整個基本類型進行作業的任何作業，例如側面程式偵測、barycentric 座標等等。</span><span class="sxs-lookup"><span data-stu-id="54eef-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="54eef-352">也可以用來選取要將基本類型傳送至其中的轉譯目標陣列配量。</span><span class="sxs-lookup"><span data-stu-id="54eef-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>我可以從幾何著色器輸出可變數量的幾何嗎？</span><span class="sxs-lookup"><span data-stu-id="54eef-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-354">是的，但這可能會導致效能問題。</span><span class="sxs-lookup"><span data-stu-id="54eef-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="54eef-355">針對一個叫用輸出1點，並為另一個叫用4點。</span><span class="sxs-lookup"><span data-stu-id="54eef-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="54eef-356">在擴充方針內進行調整時，這可能會導致幾何著色器執行緒循序執行。</span><span class="sxs-lookup"><span data-stu-id="54eef-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>D3D10 如何知道如何為我的網格產生連續的索引？</span><span class="sxs-lookup"><span data-stu-id="54eef-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="54eef-358">或者，當我指定幾何著色器需要相鄰資訊時，為什麼 D3D10 無法正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="54eef-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-359">相鄰資訊不是由 D3D10 所建立，而是由應用程式所建立。</span><span class="sxs-lookup"><span data-stu-id="54eef-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="54eef-360">鄰接索引是由應用程式產生的，而且每個基本必須包含六個索引;在六個中，奇數編號的索引是邊緣相鄰頂點。</span><span class="sxs-lookup"><span data-stu-id="54eef-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="54eef-361">ID3DX10Mesh：： GenerateAdjacencyAndPointsReps 可以用來產生此資料。</span><span class="sxs-lookup"><span data-stu-id="54eef-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="54eef-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="54eef-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="54eef-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>整數和位指令是否慢？</span><span class="sxs-lookup"><span data-stu-id="54eef-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-364">它們可以是。</span><span class="sxs-lookup"><span data-stu-id="54eef-364">They can be.</span></span> <span data-ttu-id="54eef-365">不同的 D3D10 卡可能只能針對可用的 ALU 單位子集發出整數運算。</span><span class="sxs-lookup"><span data-stu-id="54eef-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="54eef-366">這會高度依賴硬體。</span><span class="sxs-lookup"><span data-stu-id="54eef-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="54eef-367">請參閱您的個人硬體廠商，以取得如何處理該特定硬體上的整數作業的建議。</span><span class="sxs-lookup"><span data-stu-id="54eef-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="54eef-368">此外，請務必小心轉換類型。</span><span class="sxs-lookup"><span data-stu-id="54eef-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>VPOS 發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="54eef-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-370">如果您將圖元著色器的輸入宣告為 SV \_ 位置，則會得到與將它宣告為 VPOS 相同的行為。</span><span class="sxs-lookup"><span data-stu-id="54eef-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>如何? MSAA 材質範例？</span><span class="sxs-lookup"><span data-stu-id="54eef-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-372">在您的著色器中，將材質宣告為 Texture2DMS。</span><span class="sxs-lookup"><span data-stu-id="54eef-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="54eef-373">然後，您可以使用 Texture2DMS 物件以外的範例方法來提取個別的範例。</span><span class="sxs-lookup"><span data-stu-id="54eef-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>如何? 告訴您是否真的使用常數緩衝區中的著色器變數？</span><span class="sxs-lookup"><span data-stu-id="54eef-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-375">查看 \_ 針對該變數反映的 D3D10 著色器 \_ 變數 \_ DESC 結構。</span><span class="sxs-lookup"><span data-stu-id="54eef-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="54eef-376">uFlags 應 \_ 設定 D3D10 SVF \_ 使用旗標。</span><span class="sxs-lookup"><span data-stu-id="54eef-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>如何? 知道常數緩衝區中的著色器變數是否真的使用 FX10？</span><span class="sxs-lookup"><span data-stu-id="54eef-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-378">目前無法使用 FX10。</span><span class="sxs-lookup"><span data-stu-id="54eef-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>我無法控制 FX10 所建立的常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54eef-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="54eef-380">他們如何建立和更新？</span><span class="sxs-lookup"><span data-stu-id="54eef-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-381">所有 FX10 管理的常數緩衝區都會建立為 D3D10 \_ 使用量 \_ 預設資源，並使用 UpdateSubresource 進行更新。</span><span class="sxs-lookup"><span data-stu-id="54eef-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="54eef-382">因為 FX10 會保留所有常數資料的備份存放區，所以 UpdateSubresource 是更新這些資料的最佳方法。</span><span class="sxs-lookup"><span data-stu-id="54eef-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>如何? 使用著色器模擬 fixed 函數管線？</span><span class="sxs-lookup"><span data-stu-id="54eef-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-384">請參閱 FixedFuncEMU 範例。</span><span class="sxs-lookup"><span data-stu-id="54eef-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>我應該使用新的 \[ 展開 \] 、 \[ 迴圈 \] 、 \[ 分支等 \] 編譯器提示嗎？</span><span class="sxs-lookup"><span data-stu-id="54eef-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-386">一般而言不行。</span><span class="sxs-lookup"><span data-stu-id="54eef-386">In general, no.</span></span> <span data-ttu-id="54eef-387">編譯器通常會嘗試這兩種方式，並選擇最快的方法。</span><span class="sxs-lookup"><span data-stu-id="54eef-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="54eef-388">在某些情況下，可能需要使用 \[ 展開 \] ，例如，當迴圈內的材質提取需要存取漸層時。</span><span class="sxs-lookup"><span data-stu-id="54eef-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>部分有效位數會對 D3D10 有任何差異嗎？</span><span class="sxs-lookup"><span data-stu-id="54eef-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="54eef-390">我可以在我的 D3D9 HLSL 中指定部分有效位數，但不能在我的 D3D10 HLSL 中指定。</span><span class="sxs-lookup"><span data-stu-id="54eef-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-391">所有 D3D10 作業都指定為以32位浮點精確度執行。</span><span class="sxs-lookup"><span data-stu-id="54eef-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="54eef-392">因此，部分有效位數不應該在 D3D10 中產生任何差異。</span><span class="sxs-lookup"><span data-stu-id="54eef-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>在 D3D9 中，我可以藉由將深度緩衝區系結為材質並使用一般 tex2d hlsl 指示，來進行 HW PCF 影子篩選。</span><span class="sxs-lookup"><span data-stu-id="54eef-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="54eef-394">如何? 在 D3D10 上這樣做呢？</span><span class="sxs-lookup"><span data-stu-id="54eef-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-395">您必須使用比較取樣器狀態，並使用 SampleCmp 指令。</span><span class="sxs-lookup"><span data-stu-id="54eef-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="54eef-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>此 register 關鍵字在 D3D10 中的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="54eef-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-397">D3D10 中的 register 關鍵字現在適用于特定資源系結至的位置。</span><span class="sxs-lookup"><span data-stu-id="54eef-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="54eef-398">在此情況下，資源可以是緩衝區 (常數或) 、材質或取樣器。</span><span class="sxs-lookup"><span data-stu-id="54eef-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="54eef-399">針對常數緩衝區，請使用語法： register (bN) ，其中 N 是輸入位置 (0-15) </span><span class="sxs-lookup"><span data-stu-id="54eef-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="54eef-400">針對材質，請使用語法： register (tN) ，其中 N 是輸入位置 (0-127) </span><span class="sxs-lookup"><span data-stu-id="54eef-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="54eef-401">針對取樣器，請使用語法： register (sN) ，其中 N 是輸入位置 (0-127) </span><span class="sxs-lookup"><span data-stu-id="54eef-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="54eef-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>如果 register 只是用來指定要系結整個緩衝區的位置，如何? 在常數緩衝區內放置變數呢？</span><span class="sxs-lookup"><span data-stu-id="54eef-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="54eef-403">使用 packoffset 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="54eef-403">Use the packoffset keyword.</span></span> <span data-ttu-id="54eef-404">Packoffset 的引數是 c 0-4095 的形式 \[ \] 。 \[x、y、z、w \] 。</span><span class="sxs-lookup"><span data-stu-id="54eef-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="54eef-405">例如：</span><span class="sxs-lookup"><span data-stu-id="54eef-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="54eef-406">在這個常數緩衝區中，IWaste2Floats 會放在常數緩衝區中的第三個 float (第12個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="54eef-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="54eef-407">IWasteMore 會放在常數緩衝區中的第13個 float4 或52nd 浮點數。</span><span class="sxs-lookup"><span data-stu-id="54eef-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 