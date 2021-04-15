---
title: 如何設計輪廓著色器
description: 本主題說明如何設計輪廓著色器。
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990911"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="af3cd-103">如何：設計輪廓著色器</span><span class="sxs-lookup"><span data-stu-id="af3cd-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="af3cd-104">輪廓著色器是三個階段中的第一個，用來執行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md) 式 (另外兩個階段是鑲嵌和一個網域著色器) 。</span><span class="sxs-lookup"><span data-stu-id="af3cd-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="af3cd-105">本主題說明如何設計輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="af3cd-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="af3cd-106">輪廓著色器需要兩個函式，也就是主要的輪廓著色器和修補程式常數函數。</span><span class="sxs-lookup"><span data-stu-id="af3cd-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="af3cd-107">輪廓著色器會在每個控制點上實行計算;輪廓著色器也會呼叫會在每個修補程式上執行計算的 patch 常數函數。</span><span class="sxs-lookup"><span data-stu-id="af3cd-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="af3cd-108">在您設計了輪廓著色器之後，請參閱 [如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md) ，以瞭解如何建立輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="af3cd-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="af3cd-109">**設計輪廓著色器**</span><span class="sxs-lookup"><span data-stu-id="af3cd-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="af3cd-110">定義輪廓著色器輸入控制項和輸出控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="af3cd-111">定義輸出修補程式常數資料。</span><span class="sxs-lookup"><span data-stu-id="af3cd-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="af3cd-112">若為四個領域， [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) 會定義4個邊緣鑲嵌因數 (tessellate 邊緣) ，因為固定函式鑲嵌必須知道要 tessellate 多少。</span><span class="sxs-lookup"><span data-stu-id="af3cd-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="af3cd-113">三角形和等值線網域的必要輸出不同。</span><span class="sxs-lookup"><span data-stu-id="af3cd-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="af3cd-114">Fixed 函式鑲嵌不會查看任何其他的輪廓著色器輸出，例如其他 patch 常數資料或任何控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="af3cd-115">系統會為固定函式鑲嵌所產生的每個點叫用網域著色器--將會看到其輸入全部輪廓著色器的輸出控制點，以及所有輸出修補程式常數資料;著色器會在其位置評估修補程式。</span><span class="sxs-lookup"><span data-stu-id="af3cd-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="af3cd-116">定義 patch 常數函數。</span><span class="sxs-lookup"><span data-stu-id="af3cd-116">Define a patch constant function.</span></span> <span data-ttu-id="af3cd-117">Patch 常數函式會針對每個修補程式執行一次，以計算整個修補程式 (的任何資料，而不是每個控制點資料（在輪廓著色器) 中計算）。</span><span class="sxs-lookup"><span data-stu-id="af3cd-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="af3cd-118">Patch 常數函數的屬性包括：</span><span class="sxs-lookup"><span data-stu-id="af3cd-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="af3cd-119">其中一個輸入會指定包含修補程式識別碼的變數，並以 **SV \_ PrimitiveID** 系統值識別， (查看著色器模型 4) 中的 [語法](../direct3dhlsl/dx-graphics-hlsl-semantics.md) 。</span><span class="sxs-lookup"><span data-stu-id="af3cd-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="af3cd-120">其中一個輸入參數是輸入控制點，在此範例的 **VS \_ 控制 \_ 點 \_ 輸出** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="af3cd-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="af3cd-121">Patch 函式可以看到每個修補程式的所有輸入控制點，在此範例中，每個修補程式都有32個控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="af3cd-122">最小的情況下，此函式必須針對鑲嵌階段計算以 [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor)識別的每個修補程式鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="af3cd-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="af3cd-123">四個領域需要邊緣的四個鑲嵌因數，以及兩個額外的因素 (由 [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) 識別，以在修補程式內鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="af3cd-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="af3cd-124">Fixed 函式鑲嵌不會查看任何其他的輪廓著色器輸出 (例如修補程式常數資料或) 的任何控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="af3cd-125">輸出通常是由結構所定義，而且是由這個範例中的 **HS \_ 常數 \_ 資料 \_ 輸出** 所識別; 此結構相依于網欄位型別，而且為三角形或等值線網域的不同。</span><span class="sxs-lookup"><span data-stu-id="af3cd-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="af3cd-126">相反地，會針對固定函式鑲嵌所產生的每個點叫用網域著色器，並需要查看輸出控制點和輸出修補常數資料 (從輪廓著色器) ，以在其位置評估修補程式。</span><span class="sxs-lookup"><span data-stu-id="af3cd-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="af3cd-127">定義輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="af3cd-127">Define a hull shader.</span></span> <span data-ttu-id="af3cd-128">輪廓著色器會識別修補程式的屬性，包括修補程式常數函數。</span><span class="sxs-lookup"><span data-stu-id="af3cd-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="af3cd-129">每個輸出控制點都會叫用一次輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="af3cd-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="af3cd-130">輪廓著色器會使用下列屬性：</span><span class="sxs-lookup"><span data-stu-id="af3cd-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="af3cd-131">[網域](/windows/desktop/direct3dhlsl/sm5-attributes-domain)屬性。</span><span class="sxs-lookup"><span data-stu-id="af3cd-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="af3cd-132">[分割](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning)屬性。</span><span class="sxs-lookup"><span data-stu-id="af3cd-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="af3cd-133">[Outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology)屬性。</span><span class="sxs-lookup"><span data-stu-id="af3cd-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="af3cd-134">[Outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints)屬性。</span><span class="sxs-lookup"><span data-stu-id="af3cd-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="af3cd-135">[Patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc)屬性。</span><span class="sxs-lookup"><span data-stu-id="af3cd-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="af3cd-136">輪廓著色器會計算輸出控制點，此範例中有16個輸出貝茲曲線控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="af3cd-137">所有的輸入控制點 (由 **VS \_ 控制 \_ 點 \_ 輸出** 所識別，) 每個輪廓著色器調用都可以看到。</span><span class="sxs-lookup"><span data-stu-id="af3cd-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="af3cd-138">在此範例中，有32的輸入控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="af3cd-139">每個輸出控制點都會叫用一次輪廓著色器 (識別為每個修補程式的 [sv \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) ， (以 sv \_ PrimitiveID) 識別。</span><span class="sxs-lookup"><span data-stu-id="af3cd-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="af3cd-140">此特定著色器的目的是要計算輸出 *i*（定義為貝塞爾控制點）， (這個範例有16個 outputcontrolpoints) 所定義的輸出控制點。</span><span class="sxs-lookup"><span data-stu-id="af3cd-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="af3cd-141">輪廓著色器會針對每個修補程式執行一次常式 (修補程式常數函式) 計算修補程式常數資料 (鑲嵌因數作為最小) 。</span><span class="sxs-lookup"><span data-stu-id="af3cd-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="af3cd-142">輪廓著色器會分別在每個修補程式上執行 patch 常數函式 (稱為 SubDToBezierConstantsHS) ，以計算修補程式常數資料，例如鑲嵌階段的鑲嵌式因素。</span><span class="sxs-lookup"><span data-stu-id="af3cd-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af3cd-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="af3cd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af3cd-144">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="af3cd-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="af3cd-145">鑲嵌式總覽</span><span class="sxs-lookup"><span data-stu-id="af3cd-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 