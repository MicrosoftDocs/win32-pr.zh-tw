---
title: 如何設計網域著色器
description: 本主題說明如何設計網域著色器。
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46733bc9147f67cf33a127d8254f16c5813d8ebc2f0cb96c2071ae15589e34bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566178"
---
# <a name="how-to-design-a-domain-shader"></a>如何：設計定義域著色器

網域著色器是三個階段中的第三個，可共同運作以實行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md)式。 網域著色器會從輪廓著色器和 UV 座標中的已轉換控制點產生表面幾何。 本主題說明如何設計網域著色器。

針對固定函式鑲嵌所產生的每個點，都會叫用一次網域著色器。 輸入是 \[ \] 修補程式點的 UV W 座標，以及來自輪廓著色器的所有輸出資料，包括控制點和修補常數。 輸出是以任何想要的方式定義的頂點。 如果輸出傳送至圖元著色器，輸出必須包含位置 (以 SV \_ 位置語義) 表示。

**設計網域著色器**

1.  定義網域屬性。

    ```
    [domain("quad")]
    ```

    

    此網域是針對四個修補程式所定義。

2.  宣告具有 [網域位置](/windows/desktop/direct3dhlsl/sv-domainlocation) 系統值的輪廓位置。

    -   若有四個修補程式，請使用 float2。
    -   針對三個修補程式，請使用 float3 (barycentric 座標) 
    -   若為等值線，請使用 float2。

    因此，四個修補程式的網域位置看起來像這樣：

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  定義其他輸入。

    其他輸入來自于輪廓著色器，並且是由使用者定義的。 這包括 patch 的輸入控制點，其中可以有1到32點，以及輸入 patch 常數資料。

    控制點是使用者定義的，通常是使用如下所示的結構 (定義在 [如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)) ：

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    修補程式常數資料也是使用者定義的，而且看起來像是 [如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)) 中定義的 (：

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  新增使用者定義的程式碼以計算輸出;這構成了網域著色器的主體。

    此結構包含使用者定義的網域著色器輸出。

    ```
    struct DS_OUTPUT
    {
        float3 vNormal    : NORMAL;
        float2 vUV        : TEXCOORD;
        float3 vTangent   : TANGENT;
        float3 vBiTangent : BITANGENT;
        
        float4 vPosition  : SV_POSITION;
    };
    ```

    

    此函式會從鑲嵌) 採用每個輸入 UV (，並在此位置評估貝塞爾修補程式。

    ```
    [domain("quad")]
    DS_OUTPUT BezierEvalDS( HS_CONSTANT_DATA_OUTPUT input, 
                            float2 UV : SV_DomainLocation,
                            const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch )
    {
        DS_OUTPUT Output;

        // Insert code to compute the output here.

        return Output;    
    }
    ```

    

    函數會針對 fixed 函數鑲嵌所產生的每個點叫用一次。 因為此範例使用四個修補程式，所以輸入網域位置 ([SV \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) 是 float2 (UV) ; 而三個修補程式會有 float3 輸入位置 (UVW barycentric 座標) ，而等值線會有 float2 輸入網域位置。

    函式的其他輸入會直接來自輪廓著色器。 在此範例中，每一個都是一個 **貝塞爾 \_ 控制點 \_**，以及修補常數資料 (**HS \_ 常數 \_ 資料 \_ 輸出**) ，都是16個控制點。 在此範例中，輸出是包含任何資料所需 **DS \_ 輸出** 的頂點。

設計網域著色器之後，請參閱 [如何：建立網域著色器](direct3d-11-advanced-stages-domain-shader-create.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 