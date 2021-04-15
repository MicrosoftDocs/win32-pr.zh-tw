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
# <a name="how-to-design-a-hull-shader"></a>如何：設計輪廓著色器

輪廓著色器是三個階段中的第一個，用來執行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md) 式 (另外兩個階段是鑲嵌和一個網域著色器) 。 本主題說明如何設計輪廓著色器。

輪廓著色器需要兩個函式，也就是主要的輪廓著色器和修補程式常數函數。 輪廓著色器會在每個控制點上實行計算;輪廓著色器也會呼叫會在每個修補程式上執行計算的 patch 常數函數。

在您設計了輪廓著色器之後，請參閱 [如何：建立輪廓著色器](direct3d-11-advanced-stages-hull-shader-create.md) ，以瞭解如何建立輪廓著色器。

**設計輪廓著色器**

1.  定義輪廓著色器輸入控制項和輸出控制點。

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

    

2.  定義輸出修補程式常數資料。

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

    

    若為四個領域， [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) 會定義4個邊緣鑲嵌因數 (tessellate 邊緣) ，因為固定函式鑲嵌必須知道要 tessellate 多少。 三角形和等值線網域的必要輸出不同。

    Fixed 函式鑲嵌不會查看任何其他的輪廓著色器輸出，例如其他 patch 常數資料或任何控制點。 系統會為固定函式鑲嵌所產生的每個點叫用網域著色器--將會看到其輸入全部輪廓著色器的輸出控制點，以及所有輸出修補程式常數資料;著色器會在其位置評估修補程式。

3.  定義 patch 常數函數。 Patch 常數函式會針對每個修補程式執行一次，以計算整個修補程式 (的任何資料，而不是每個控制點資料（在輪廓著色器) 中計算）。

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

    

    Patch 常數函數的屬性包括：

    -   其中一個輸入會指定包含修補程式識別碼的變數，並以 **SV \_ PrimitiveID** 系統值識別， (查看著色器模型 4) 中的 [語法](../direct3dhlsl/dx-graphics-hlsl-semantics.md) 。
    -   其中一個輸入參數是輸入控制點，在此範例的 **VS \_ 控制 \_ 點 \_ 輸出** 中宣告。 Patch 函式可以看到每個修補程式的所有輸入控制點，在此範例中，每個修補程式都有32個控制點。
    -   最小的情況下，此函式必須針對鑲嵌階段計算以 [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor)識別的每個修補程式鑲嵌因數。 四個領域需要邊緣的四個鑲嵌因數，以及兩個額外的因素 (由 [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) 識別，以在修補程式內鑲嵌。 Fixed 函式鑲嵌不會查看任何其他的輪廓著色器輸出 (例如修補程式常數資料或) 的任何控制點。
    -   輸出通常是由結構所定義，而且是由這個範例中的 **HS \_ 常數 \_ 資料 \_ 輸出** 所識別; 此結構相依于網欄位型別，而且為三角形或等值線網域的不同。

    相反地，會針對固定函式鑲嵌所產生的每個點叫用網域著色器，並需要查看輸出控制點和輸出修補常數資料 (從輪廓著色器) ，以在其位置評估修補程式。

4.  定義輪廓著色器。 輪廓著色器會識別修補程式的屬性，包括修補程式常數函數。 每個輸出控制點都會叫用一次輪廓著色器。

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

    

    輪廓著色器會使用下列屬性：

    -   [網域](/windows/desktop/direct3dhlsl/sm5-attributes-domain)屬性。
    -   [分割](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning)屬性。
    -   [Outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology)屬性。
    -   [Outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints)屬性。
    -   [Patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc)屬性。 輪廓著色器會計算輸出控制點，此範例中有16個輸出貝茲曲線控制點。

所有的輸入控制點 (由 **VS \_ 控制 \_ 點 \_ 輸出** 所識別，) 每個輪廓著色器調用都可以看到。 在此範例中，有32的輸入控制點。

每個輸出控制點都會叫用一次輪廓著色器 (識別為每個修補程式的 [sv \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) ， (以 sv \_ PrimitiveID) 識別。 此特定著色器的目的是要計算輸出 *i*（定義為貝塞爾控制點）， (這個範例有16個 outputcontrolpoints) 所定義的輸出控制點。

輪廓著色器會針對每個修補程式執行一次常式 (修補程式常數函式) 計算修補程式常數資料 (鑲嵌因數作為最小) 。 輪廓著色器會分別在每個修補程式上執行 patch 常數函式 (稱為 SubDToBezierConstantsHS) ，以計算修補程式常數資料，例如鑲嵌階段的鑲嵌式因素。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 