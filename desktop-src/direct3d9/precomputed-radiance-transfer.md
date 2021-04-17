---
description: '預先計算 Radiance Transfer (Direct3D 9) '
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: '預先計算 Radiance Transfer (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568203"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>預先計算 Radiance Transfer (Direct3D 9) 

## <a name="using-precomputed-radiance-transfer"></a>使用預先計算 Radiance 傳輸

有趣的場景中有數種形式的複雜度，包括光源環境的模型 (也就是，區域光源模型與點/方向一) ，以及模型化何種全域效果 (例如，遮蔽、interreflections、地下散佈。 ) 傳統的互動式轉譯技術模型，這是有限的複雜度。 PRT 可讓這些結果有一些重大限制：

-   物件會假設為固定 (也就是沒有 deformations) 。
-   它是以物件為中心的方法 (除非物件會一起移動，否則這些全域效果將不會在) 之間進行維護。
-   只有低頻率的光源會模型化 (產生軟陰影。 ) 高頻率的燈光 (清晰的陰影) ，則必須採用傳統的技巧。

PRT 需要下列其中一項，但不需要兩者：

-   高鑲嵌模型和 vs \_ 1 \_ 1
-   ps \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>標準漫射光源與 PRT

下圖是使用傳統 (n ·l) 光源模型。 您可以使用另一個 pass 和某種形式的遮蔽技術來啟用明確陰影， (陰影深度對應或陰影磁片區) 。 如果要使用 () 或更複雜的著色器，以使用傳統的技術，新增多個燈光會需要多個走。

![使用傳統光源模型所呈現之圖例的螢幕擷取畫面](images/prt-diffuse-cropped.png)

下圖是使用 PRT 來呈現，並使用可解決的單一方向光源的最佳近似值。 這會導致不容易以傳統技術產生的軟陰影。 由於 PRT 一律會將已完成的照明環境模型加入多個燈光或使用環境對應，因此您只會變更 (的值，但不會變更著色器所使用的常數) 數目。

![使用 prt 所呈現圖例的螢幕擷取畫面](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>使用 Interreflections 的 PRT

直接光源會直接從燈光到達表面。 Interreflections 會在將某些其他介面彈到某些次數之後，觸及表面。 PRT 可以建立此行為的模型，而不需要在執行時間變更效能，只要使用不同的參數執行模擬器即可。

下圖僅使用 direct PRT 來建立， (0 彈跳而沒有 interreflections) 。

![僅使用直接 prt 所呈現之圖例的螢幕擷取畫面](images/prt-nointerreflections.png)

下圖是使用 PRT 與 interreflections 建立的， (2 使用 interreflections) 彈跳。

![使用 prt 搭配 interreflections 所呈現圖例的螢幕擷取畫面](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>使用地下散佈的 PRT

地下散佈是一種技術，可建立光線如何通過特定材質的模型。 例如，對您手的手掌按下亮燈。 這種光線的光線通過您的手， (變更程式) 中的色彩，然後離開您手的另一端。 這也可以使用模擬器的簡單變更來建立模型，而且不會變更執行時間。

下圖示范 PRT 與地下散佈。

![使用 prt 搭配地下散佈所呈現圖例的螢幕擷取畫面](images/prt-subsurface.png)

## <a name="how-prt-works"></a>PRT 的運作方式

下列詞彙有助於瞭解 PRT 的運作方式，如下圖所示。

來源 Radiance：來源 Radiance 表示整個光源的環境。 在 PRT 中，使用球形調和來估算任意的環境，此光源會假設為相對於物件 (與使用環境對應所做的相同假設 ) 。

Exit Radiance： Exit Radiance 是離開介面上某個點的燈光，從任何可能的來源 (反映 Radiance、地下散佈、發射) 。

傳輸向量：將向量地圖來源 Radiance 轉換成 exit Radiance，並使用複雜的燈光傳輸模擬來預先計算離線。

![prt 運作方式的圖表](images/prt-lightingpicture.png)

PRT 會將轉譯程式分為兩個階段，如下圖所示：

1.  昂貴的輕量傳輸模擬 precomputes 可在執行時間使用的傳輸係數。
2.  相對較輕量的執行時間階段會先接近使用球形調和的照明環境，然後使用這些光源係數和預先計算傳輸係數 (從第1階段) ，再加上一個簡單的著色器，因此會導致結束 radiance (光離開物件) 。

![prt 資料流程的圖表](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>如何使用 PRT API

1.  使用其中一個計算來計算傳輸向量 .。。 [**ID3DXPRTEngine**](id3dxprtengine.md)的方法。

    直接處理這些傳輸媒介需要大量的記憶體和著色器計算。 壓縮可大幅減少所需的記憶體和著色器計算量。

    最後的光源值會在端點著色器中計算，以執行下列壓縮的轉譯方程式。

    ![prt 轉譯的方程式](images/prt-shaderequation.png)

    其中：

    

    | 參數      | Description                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | Rp             | 在頂點 p 的結束 radiance 單一通道，會在網格上的每個頂點進行評估。                     |
    | Mk             | 群集 k 的平均值。 這是係數的 Order ²向量。                                               |
    | k              | 頂點 p 的叢集識別碼。                                                                                    |
    | L<sup>'</sup>  | 來源 radiance 至 SH 基礎函數的近似值。 這是係數的 Order ²向量。 |
    | j              | 加總 PCA 向量數目的整數。                                                            |
    | w<sub>pj</sub> | 點 p 的第 j 個 PCA 加權。 這是單一係數。                                                   |
    | B<sub>kj</sub> | 適用于群集 k 的第 j 個 PCA 基礎向量。 這是係數的 Order ²向量。                               |

    

     

    解壓縮 .。。 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 方法可讓您從模擬存取壓縮的資料。

2.  計算來源 radiance。

    API 中有數個 helper 函式，可處理各種常見的光源案例。

    

    | 函式                                                         | 用途                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | 近似于傳統的方向淺色。                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | 近似于本機球形燈光來源。  (請注意，PRT 僅適用于距離光源環境。 )  |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | 近似于遠處區域光源。 例如，sun (非常小的錐形角度) 。              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | 評估兩個色彩之間的線性插補， (球) 的每個極點。         |

    

     

3.  計算 exit radiance。

    現在必須使用頂點或圖元著色器在每個點上評估方程式1。 在評估著色器之前，必須先預先計算常數，並將其載入常數資料表 (如需詳細資料，請參閱 [PRT 示範範例](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)) 。 著色器本身是此方程式的直接執行。

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a>參考資料

如需 PRT 和球面諧波的詳細資訊，請參閱下列白皮書：


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> <dt>

[PRT 方 (Direct3D 9) ](prt-equations.md)
</dt> <dt>

[使用 (Direct3D 9) 的材質表示 PRT ](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[預先計算 Radiance 傳送函式](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



