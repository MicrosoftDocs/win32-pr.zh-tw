---
description: Direct3D 可讓應用程式藉由轉譯分割的多邊形物件（特別是字元）來提高其幕後的本質，而這些物件具有順暢的混合接點。
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: " (Direct3D 9) 的幾何混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687368"
---
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="c80b0-103"> (Direct3D 9) 的幾何混合</span><span class="sxs-lookup"><span data-stu-id="c80b0-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="c80b0-104">Direct3D 可讓應用程式藉由轉譯分割的多邊形物件（特別是字元）來提高其幕後的本質，而這些物件具有順暢的混合接點。</span><span class="sxs-lookup"><span data-stu-id="c80b0-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="c80b0-105">這些效果通常稱為「外觀」。</span><span class="sxs-lookup"><span data-stu-id="c80b0-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="c80b0-106">系統會藉由將額外的世界轉換矩陣套用至一組頂點來建立多個結果，然後在結果頂點之間執行線性 blend 來建立單一幾何集合，以達成此效果。</span><span class="sxs-lookup"><span data-stu-id="c80b0-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="c80b0-107">Banana 的下圖顯示此程式。</span><span class="sxs-lookup"><span data-stu-id="c80b0-107">The following illustration of a banana shows this process.</span></span>

![將兩個物件與 banana 材質混合的流程圖例](images/geometry-blend.png)

<span data-ttu-id="c80b0-109">上圖顯示您可能想像幾何混合進程的方式。</span><span class="sxs-lookup"><span data-stu-id="c80b0-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="c80b0-110">在單一轉譯呼叫中，系統會取得 banana 的頂點、將它們轉換兩次（不需要修改），並使用簡單的旋轉並混合結果來建立彎曲的 banana。</span><span class="sxs-lookup"><span data-stu-id="c80b0-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="c80b0-111">系統會混合頂點位置，以及啟用光源時的頂點法線。</span><span class="sxs-lookup"><span data-stu-id="c80b0-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="c80b0-112">應用程式不限於兩個混合路徑;Direct3D 可以 blend 多達四個世界矩陣，包括標準世界矩陣 [**D3DTS \_ 世界**](d3dts-world.md)。</span><span class="sxs-lookup"><span data-stu-id="c80b0-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="c80b0-113">啟用光源時，會以對應的反向世界視圖矩陣（以與頂點位置計算相同的方式加權）來轉換頂點法線。</span><span class="sxs-lookup"><span data-stu-id="c80b0-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="c80b0-114">如果 D3DRS \_ NORMALIZENORMALS 轉譯狀態設為 **TRUE**，系統就會將產生的一般向量標準化。</span><span class="sxs-lookup"><span data-stu-id="c80b0-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="c80b0-115">如果沒有幾何混合，動態具現化的模型通常會在區段中呈現。</span><span class="sxs-lookup"><span data-stu-id="c80b0-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="c80b0-116">例如，請考慮使用人體 arm 的3D 模型。</span><span class="sxs-lookup"><span data-stu-id="c80b0-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="c80b0-117">在最簡單的觀點中，arm 有兩個部分：連線至內文的上層 arm，以及連線至手的較低 arm。</span><span class="sxs-lookup"><span data-stu-id="c80b0-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="c80b0-118">這兩個連接在肘線，而較低的 arm 會在該點旋轉。</span><span class="sxs-lookup"><span data-stu-id="c80b0-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="c80b0-119">轉譯 arm 的應用程式可能會保留上層和較低 arm 的頂點資料，每個都有不同的世界轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="c80b0-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="c80b0-120">下列程式碼範例會說明這點。</span><span class="sxs-lookup"><span data-stu-id="c80b0-120">The following code example illustrates this.</span></span>


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



<span data-ttu-id="c80b0-121">為了轉譯 arm，會進行兩個轉譯呼叫，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="c80b0-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



<span data-ttu-id="c80b0-122">下圖是 banana，修改為使用這項技術。</span><span class="sxs-lookup"><span data-stu-id="c80b0-122">The following illustration is a banana, modified to use this technique.</span></span>

![混合 banana 沒有幾何混合的圖例](images/noblend.png)

<span data-ttu-id="c80b0-124">混合幾何和 nonblended 幾何之間的差異很明顯。</span><span class="sxs-lookup"><span data-stu-id="c80b0-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="c80b0-125">這個範例有點極端。</span><span class="sxs-lookup"><span data-stu-id="c80b0-125">This example is somewhat extreme.</span></span> <span data-ttu-id="c80b0-126">在真實世界的應用程式中，分割模型的接點是設計成讓接縫不太明顯。</span><span class="sxs-lookup"><span data-stu-id="c80b0-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="c80b0-127">不過，在某些情況下會顯示接縫，以呈現模型設計師的常數挑戰。</span><span class="sxs-lookup"><span data-stu-id="c80b0-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="c80b0-128">Direct3D 中的幾何混合提供傳統分段模型案例的替代方案。</span><span class="sxs-lookup"><span data-stu-id="c80b0-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="c80b0-129">不過，已改善的分段物件視覺品質會產生轉譯期間的混合計算成本。</span><span class="sxs-lookup"><span data-stu-id="c80b0-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="c80b0-130">為了將這些額外作業的影響降到最低，Direct3D 幾何管線已針對混合幾何進行優化，而且可能會產生最少的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="c80b0-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="c80b0-131">使用 Direct3D 所提供之幾何混合服務的應用程式，可以改善其字元的真實性，同時避免嚴重的效能影響。</span><span class="sxs-lookup"><span data-stu-id="c80b0-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="c80b0-132">混合轉換和呈現狀態</span><span class="sxs-lookup"><span data-stu-id="c80b0-132">Blending Transform and Render States</span></span>

<span data-ttu-id="c80b0-133">[**IDirect3DDevice9：： SetTransform**](/windows/desktop/api)方法可辨識 [**D3DTS \_ WORLD**](d3dts-world.md)和 [**D3DTS \_ WORLDn**](d3dts-worldn.md)宏，這些宏對應到可由 [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)巨集定義的值。</span><span class="sxs-lookup"><span data-stu-id="c80b0-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="c80b0-134">這些宏會用來識別將混合幾何的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c80b0-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="c80b0-135">[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)列舉型別包含 D3DRS \_ VERTEXBLEND 轉譯狀態，以啟用並控制幾何混合。</span><span class="sxs-lookup"><span data-stu-id="c80b0-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="c80b0-136">此呈現狀態的有效值是由 [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) 列舉型別所定義。</span><span class="sxs-lookup"><span data-stu-id="c80b0-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="c80b0-137">如果已啟用幾何混色，頂點格式必須包含適當的混色加權數目。</span><span class="sxs-lookup"><span data-stu-id="c80b0-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="c80b0-138">混合加權</span><span class="sxs-lookup"><span data-stu-id="c80b0-138">Blending Weights</span></span>

<span data-ttu-id="c80b0-139">混合權數（有時稱為測試加權）會控制指定的世界矩陣影響頂點的範圍。</span><span class="sxs-lookup"><span data-stu-id="c80b0-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="c80b0-140">混合權數是從0.0 到1.0 的浮點數，以頂點格式編碼，其中的值為0.0 表示頂點不會與該矩陣混合，而1.0 表示頂點會受到矩陣的完整影響。</span><span class="sxs-lookup"><span data-stu-id="c80b0-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="c80b0-141">幾何混合權數會以頂點格式編碼，並緊接在每個頂點的位置之後，如 [Fixed FUNCTION FVF 程式碼 (Direct3D 9) ](fixed-function-fvf-codes.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="c80b0-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="c80b0-142">您可以藉由在您提供給轉譯方法的頂點描述中包含其中一個 [FVF 常數](d3dfvf.md) ，來傳達頂點格式的混色加權數目。</span><span class="sxs-lookup"><span data-stu-id="c80b0-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="c80b0-143">系統會在 blend 矩陣的加權結果之間執行線性 blend。</span><span class="sxs-lookup"><span data-stu-id="c80b0-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="c80b0-144">下列方程式是完整的混合公式。</span><span class="sxs-lookup"><span data-stu-id="c80b0-144">The following equation is the complete blending formula.</span></span>

![線性混合的方程式，使用世界轉換矩陣](images/vert-blend-formula.png)

<span data-ttu-id="c80b0-146">在上述的方程式中，vBlend 是輸出頂點，v 元素是套用的世界矩陣所產生的頂點 ([**D3DTS \_ WORLDn**](d3dts-worldn.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c80b0-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="c80b0-147">W 元素是頂點格式內對應的加權值。</span><span class="sxs-lookup"><span data-stu-id="c80b0-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="c80b0-148">在 n 個矩陣之間混合的頂點可以有-1 個混合加權值，每個混色矩陣各有一個，但最後一個除外。</span><span class="sxs-lookup"><span data-stu-id="c80b0-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="c80b0-149">系統會自動產生最後一個世界矩陣的權數，讓所有加權的總和都是1.0，以 sigma 標記法表示。</span><span class="sxs-lookup"><span data-stu-id="c80b0-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="c80b0-150">您可以針對 Direct3D 所支援的每個案例簡化此公式，如下列方程式所示。</span><span class="sxs-lookup"><span data-stu-id="c80b0-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![三種混色案例的線性混合方程式](images/vert-blend-formulas-simple.png)

<span data-ttu-id="c80b0-152">這些是兩個、三個和四個 blend 矩陣案例的完整混合公式的簡化形式。</span><span class="sxs-lookup"><span data-stu-id="c80b0-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="c80b0-153">雖然 Direct3D 包含 FVF 描述項來定義最多有五個混色加權的頂點，但這一版的 DirectX 只能使用三個。</span><span class="sxs-lookup"><span data-stu-id="c80b0-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="c80b0-154">下列主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="c80b0-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="c80b0-155">使用 (Direct3D 9) 的幾何混合 </span><span class="sxs-lookup"><span data-stu-id="c80b0-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="c80b0-156"> (Direct3D 9) 的索引頂點混合 </span><span class="sxs-lookup"><span data-stu-id="c80b0-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="c80b0-157"> (Direct3D 9) 的頂點補間 </span><span class="sxs-lookup"><span data-stu-id="c80b0-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="c80b0-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="c80b0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c80b0-159">頂點管線</span><span class="sxs-lookup"><span data-stu-id="c80b0-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
