---
description: Direct3D 在單一階段中最多可以將八個紋理混合到原始物件上。
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: " (Direct3D 9) 的材質混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688487"
---
# <a name="texture-blending-direct3d-9"></a><span data-ttu-id="f2647-103"> (Direct3D 9) 的材質混合</span><span class="sxs-lookup"><span data-stu-id="f2647-103">Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="f2647-104">Direct3D 在單一階段中最多可以將八個紋理混合到原始物件上。</span><span class="sxs-lookup"><span data-stu-id="f2647-104">Direct3D can blend as many as eight textures onto primitives in a single pass.</span></span> <span data-ttu-id="f2647-105">使用多重紋理混合可大幅增加 Direct3D 應用程式的畫面播放速度。</span><span class="sxs-lookup"><span data-stu-id="f2647-105">The use of multiple texture blending can profoundly increase the frame rate of a Direct3D application.</span></span> <span data-ttu-id="f2647-106">應用程式藉由使用多重紋理混合，在單一階段中套用紋理、陰影、反射光源、擴散光源等其他特殊效果。</span><span class="sxs-lookup"><span data-stu-id="f2647-106">An application employs multiple texture blending to apply textures, shadows, specular lighting, diffuse lighting, and other special effects in a single pass.</span></span>

<span data-ttu-id="f2647-107">若要使用紋理混色，您的應用程式首先應該確認使用者的硬體是否支援該功能。</span><span class="sxs-lookup"><span data-stu-id="f2647-107">To use texture blending, your application should first check if the user's hardware supports it.</span></span> <span data-ttu-id="f2647-108">這項資訊可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 TextureCaps 成員中找到。</span><span class="sxs-lookup"><span data-stu-id="f2647-108">This information is found in the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="f2647-109">如需有關如何查詢使用者硬體以進行紋理混合功能的詳細資訊，請參閱 [**IDirect3DDevice9：： GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)。</span><span class="sxs-lookup"><span data-stu-id="f2647-109">For details about how to query the user's hardware for texture blending capabilities, see [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).</span></span>

## <a name="texture-stages-and-the-texture-blending-cascade"></a><span data-ttu-id="f2647-110">紋理階段和材質混合式</span><span class="sxs-lookup"><span data-stu-id="f2647-110">Texture Stages and the Texture Blending Cascade</span></span>

<span data-ttu-id="f2647-111">Direct3D 透過使用紋理階段來支援一階段的多重紋理混合。</span><span class="sxs-lookup"><span data-stu-id="f2647-111">Direct3D supports single-pass multiple texture blending through the use of texture stages.</span></span> <span data-ttu-id="f2647-112">紋理階段取得兩個引數之後，對其進行混合運算，並且將結果傳回以供進一步處理或點陣化使用。</span><span class="sxs-lookup"><span data-stu-id="f2647-112">A texture stage takes two arguments and performs a blending operation on them, passing on the result for further processing or for rasterization.</span></span> <span data-ttu-id="f2647-113">您可將紋理階段視覺化為以下圖例。</span><span class="sxs-lookup"><span data-stu-id="f2647-113">You can visualize a texture stage as shown in the following diagram.</span></span>

![紋理階段的簡圖](images/texstg.png)

<span data-ttu-id="f2647-115">如上方簡圖所示，紋理階段會利用一個指定的運算子將兩個引數混合。</span><span class="sxs-lookup"><span data-stu-id="f2647-115">As the preceding diagram shows, texture stages blend two arguments by using a specified operator.</span></span> <span data-ttu-id="f2647-116">常見的運算包括了簡單的調節，或是增加引數的色彩或 Alpha 元件，但應用程式支援超過 24 種運算。</span><span class="sxs-lookup"><span data-stu-id="f2647-116">Common operations include simple modulation or addition of the color or alpha components of the arguments, but more than two dozen operations are supported.</span></span> <span data-ttu-id="f2647-117">階段的引數可以是關聯紋理、重複色彩及 Alpha (於 Gouraud Shading 中重複)、任意色彩及 Alpha，或是前一紋理階段的結果。</span><span class="sxs-lookup"><span data-stu-id="f2647-117">The arguments for a stage can be an associated texture, the iterated color or alpha (iterated during Gouraud shading), arbitrary color and alpha, or the result from the previous texture stage.</span></span> <span data-ttu-id="f2647-118">如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混合作業和引數 ](texture-blending-operations-and-arguments.md)。</span><span class="sxs-lookup"><span data-stu-id="f2647-118">For more information, see [Texture Blending Operations and Arguments (Direct3D 9)](texture-blending-operations-and-arguments.md).</span></span>

> [!Note]  
> <span data-ttu-id="f2647-119">Direct3D 會區分色彩與 Alpha 混色的混合。</span><span class="sxs-lookup"><span data-stu-id="f2647-119">Direct3D distinguishes color blending from alpha blending.</span></span> <span data-ttu-id="f2647-120">應用程式會為色彩及 Alpha 個別設定混合運算及引數，並且其結果均各自獨立。</span><span class="sxs-lookup"><span data-stu-id="f2647-120">Applications set blending operations and arguments for color and alpha individually, and the results of those settings are independent of one another.</span></span>

 

<span data-ttu-id="f2647-121">多重混合階段使用的引數及運算組合，定義了一個以流程為基礎的簡單混合語言。</span><span class="sxs-lookup"><span data-stu-id="f2647-121">The combination of arguments and operations used by multiple blending stages define a simple flow-based blending language.</span></span> <span data-ttu-id="f2647-122">一個階段的結果會流到另一個階段，並且再從該階段流至下一個階段，以此類推。</span><span class="sxs-lookup"><span data-stu-id="f2647-122">The results from one stage flow down to another stage, from that stage to the next, and so on.</span></span> <span data-ttu-id="f2647-123">運算結果從一個階段流至另一個階段，並且最終在一個多邊形上進行點陣化的這項概念，通常稱作紋理混色串聯。</span><span class="sxs-lookup"><span data-stu-id="f2647-123">The concept of results flowing from stage to stage to eventually be rasterized on a polygon is often called the texture blending cascade.</span></span> <span data-ttu-id="f2647-124">下列簡圖呈現了個別紋理階段組成紋理混色串聯的過程。</span><span class="sxs-lookup"><span data-stu-id="f2647-124">The following diagram shows how individual texture stages make up the texture blending cascade.</span></span>

![紋理混色串聯中紋理階段的簡圖](images/tcascade.png)

<span data-ttu-id="f2647-126">裝置中的每個階段都有一個以 0 為基礎的索引。</span><span class="sxs-lookup"><span data-stu-id="f2647-126">Each stage in a device has a zero-based index.</span></span> <span data-ttu-id="f2647-127">Direct3D 雖然允許最多八個混合階段，我們仍建議您事先檢查裝置功能，以決定現有硬體支援的最大階段數量。</span><span class="sxs-lookup"><span data-stu-id="f2647-127">Direct3D allows up to eight blending stages, although you should always check device capabilities to determine how many stages the current hardware supports.</span></span> <span data-ttu-id="f2647-128">第一個混合階段位於索引 0 上，第二個則位於 1，以此類推直到索引 7 為止。</span><span class="sxs-lookup"><span data-stu-id="f2647-128">The first blending stage is at index 0, the second is at 1, and so on, up to index 7.</span></span> <span data-ttu-id="f2647-129">系統以遞增索引順序混合各階段。</span><span class="sxs-lookup"><span data-stu-id="f2647-129">The system blends stages in increasing index order.</span></span>

<span data-ttu-id="f2647-130">建議您只使用您需要的階段數量。任何未使用的混合階段預設都會停用。</span><span class="sxs-lookup"><span data-stu-id="f2647-130">Use only the number of stages you need; the unused blending stages are disabled by default.</span></span> <span data-ttu-id="f2647-131">因此，若您的應用程式只會使用到前兩個階段，您只需要為階段 0 及階段 1 設定運算及引數。</span><span class="sxs-lookup"><span data-stu-id="f2647-131">So, if your application only uses the first two stages, it need only set operations and arguments for stage 0 and 1.</span></span> <span data-ttu-id="f2647-132">系統會混合兩個階段，並且忽略所有停用的階段。</span><span class="sxs-lookup"><span data-stu-id="f2647-132">The system blends the two stages, and ignores the disabled stages.</span></span>

> [!Note]  
> <span data-ttu-id="f2647-133">若您的應用程式根據不同的狀況，可能會使用不同數量的階段 (例如：針對一些物件設定四個階段，其他的則為兩個階段)，您不需要明確停用所有之前使用過的階段。</span><span class="sxs-lookup"><span data-stu-id="f2647-133">If your application varies the number of stages it uses for different situations - such as four stages for some objects, and only two for others - you don't need to explicitly disable all previously used stages.</span></span> <span data-ttu-id="f2647-134">其中一個選項是停用第一個未使用階段的色彩運算，則所有具有更高索引值的階段皆不會啟用。</span><span class="sxs-lookup"><span data-stu-id="f2647-134">One option is to disable the color operation for the first unused stage, then all stages with a higher index will not be applied.</span></span> <span data-ttu-id="f2647-135">另一個選項是設定第一個材質階段的色彩作業， (階段 0) D3DTOP 停用，以停用材質對應 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f2647-135">Another option is to disable texture mapping altogether by setting the color operation for the first texture stage (stage 0) to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="f2647-136">第三個選項是當材質階段具有 \_ 等於 D3DTA 材質的 D3DTSS COLORARG1， \_ 且階段的材質指標為 **Null** 時，這個階段和所有階段都不會處理。</span><span class="sxs-lookup"><span data-stu-id="f2647-136">A third option is when a texture stage has D3DTSS\_COLORARG1 equal to D3DTA\_TEXTURE and the texture pointer for the stage is **NULL**, this stage and all stages after it are not processed.</span></span>

 

<span data-ttu-id="f2647-137">下列主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="f2647-137">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="f2647-138"> (Direct3D 9) 的材質混合作業和引數 </span><span class="sxs-lookup"><span data-stu-id="f2647-138">Texture Blending Operations and Arguments (Direct3D 9)</span></span>](texture-blending-operations-and-arguments.md)
-   [<span data-ttu-id="f2647-139">將目前的材質指派 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="f2647-139">Assigning the Current Textures (Direct3D 9)</span></span>](assigning-the-current-textures.md)
-   [<span data-ttu-id="f2647-140"> (Direct3D 9) 建立混合階段 </span><span class="sxs-lookup"><span data-stu-id="f2647-140">Creating Blending Stages (Direct3D 9)</span></span>](creating-blending-stages.md)
-   [<span data-ttu-id="f2647-141"> (Direct3D 9) 的 Alpha 材質混合 </span><span class="sxs-lookup"><span data-stu-id="f2647-141">Alpha Texture Blending (Direct3D 9)</span></span>](alpha-texture-blending.md)
-   [<span data-ttu-id="f2647-142">Multipass (Direct3D 9) 的材質混合 </span><span class="sxs-lookup"><span data-stu-id="f2647-142">Multipass Texture Blending (Direct3D 9)</span></span>](multipass-texture-blending.md)
-   [<span data-ttu-id="f2647-143">使用 (Direct3D 9) 的材質進行淺色對應 </span><span class="sxs-lookup"><span data-stu-id="f2647-143">Light Mapping with Textures (Direct3D 9)</span></span>](light-mapping-with-textures.md)

## <a name="related-topics"></a><span data-ttu-id="f2647-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2647-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2647-145">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="f2647-145">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
