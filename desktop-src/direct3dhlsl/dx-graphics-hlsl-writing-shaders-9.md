---
title: 在 Direct3D 9 撰寫 HLSL 著色器
description: 在 Direct3D 9 撰寫 HLSL 著色器
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e6fec265682dcdbe8ffa967ba757382eda2e17d55aff8b8a1ae168a96df3c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950108"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>在 Direct3D 9 撰寫 HLSL 著色器

-   [頂點-著色器基本概念](#vertex-shader-basics)
-   [圖元著色器基本概念](#pixel-shader-basics)
    -   [材質階段和取樣器狀態](#texture-stage-and-sampler-states)
    -   [圖元著色器輸入](#pixel-shader-inputs)
    -   [圖元著色器輸出](#pixel-shader-outputs)
-   [著色器輸入和著色器變數](#shader-inputs-and-shader-variables)
    -   [宣告著色器變數](#declaring-shader-variables)
    -   [統一著色器輸入](#uniform-shader-inputs)
    -   [不同的著色器輸入和語義](#varying-shader-inputs-and-semantics)
    -   [取樣器和材質物件](#samplers-and-texture-objects)
-   [撰寫函數](#writing-functions)
-   [Flow控制](#flow-control)
-   [相關主題](#related-topics)

## <a name="vertex-shader-basics"></a>Vertex-Shader 基本概念

在作業中，可程式化的頂點著色器會取代 Microsoft Direct3D 圖形管線所完成的頂點處理。 使用頂點著色器時，固定函式管線會忽略關於轉換和光源作業的狀態資訊。 當頂點著色器已停用，且傳回固定的函式處理時，會套用所有目前的狀態設定。

在頂點著色器執行之前，必須先完成高序位基本專案的鑲嵌。 著色器處理之後執行表面鑲嵌的執行必須以對應用程式和著色器程式碼不明顯的方式來執行。

頂點著色器最少必須在同質剪輯空間中輸出頂點位置。 （選擇性）頂點著色器可以輸出材質座標、頂點色彩、頂點光源、霧化因數等等。

## <a name="pixel-shader-basics"></a>Pixel-Shader 基本概念

圖元處理是由個別圖元上的圖元著色器所執行。 圖元著色器與頂點著色器搭配運作;頂點著色器的輸出會提供圖元著色器的輸入。 其他圖元運算 (霧化混色、樣板作業和轉譯目標混色) 在著色器執行之後發生。

### <a name="texture-stage-and-sampler-states"></a>材質階段和取樣器狀態

圖元著色器會完全取代多紋理 blender 所指定的圖元混合功能，包括材質階段狀態之前所定義的作業。 針對縮制、縮放比例、mip 篩選和 wrap 定址模式所控制的材質取樣和篩選作業，可以在著色器中初始化。 應用程式可自由變更這些狀態，而不需要重新產生目前系結的著色器。 如果您的著色器是在效果內設計，則設定狀態可以更容易進行。

### <a name="pixel-shader-inputs"></a>圖元著色器輸入

針對圖元著色器版本 ps \_ 1 \_ 1-ps \_ 2 \_ 0，擴散和反射色彩是在著色器使用之前的範圍 (壓制) 的飽和。

系統會假設圖元著色器的色彩值輸入是正確的，但並非所有硬體) 都能 (。 從紋理座標取樣的色彩會以正確的角度進行反覆運算，並在反復專案期間壓制至0到1的範圍。

### <a name="pixel-shader-outputs"></a>圖元著色器輸出

針對圖元著色器版本 ps \_ 1 \_ 1-ps \_ 1 \_ 4，圖元著色器發出的結果是 register r0 的內容。 著色器完成處理時所包含的任何內容都會傳送至霧化階段和轉譯目標 blender。

若是圖元著色器版本 ps \_ 2 \_ 0 和更新版本，則會從 OC0-oC4 發出輸出色彩。

## <a name="shader-inputs-and-shader-variables"></a>著色器輸入和著色器變數

-   [宣告著色器變數](#declaring-shader-variables)
-   [統一著色器輸入](#uniform-shader-inputs)
-   [不同的著色器輸入和語義](#varying-shader-inputs-and-semantics)
-   [取樣器和材質物件](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>宣告著色器變數

最簡單的變數宣告包括型別和變數名稱，例如：


```
float fVar;
```



您可以在相同的語句中初始化變數。


```
float fVar = 3.1f;
```



可以宣告變數陣列，


```
int iVar[3];
```



或在相同的語句中宣告和初始化。


```
int iVar[3] = {1,2,3};
```



以下是一些宣告，示範高階著色器語言 (HLSL) 變數的許多特性：


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



資料宣告可以使用任何有效的類型，包括：

-   [ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
-   [ (DirectX HLSL) 的向量類型 ](dx-graphics-hlsl-vector.md)
-   [ (DirectX HLSL) 的矩陣類型 ](dx-graphics-hlsl-matrix.md)
-   [ (DirectX HLSL) 的著色器類型 ](dx-graphics-hlsl-shader.md)
-   [ (DirectX HLSL) 的取樣器類型 ](dx-graphics-hlsl-sampler.md)
-   [ (DirectX HLSL) 的使用者自訂類型 ](dx-graphics-hlsl-user-defined.md)

著色器可以具有最上層變數、引數和函數。


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



最上層變數是在所有函式之外宣告的。 最上層引數是最上層函數的參數。 最上層函式是由應用程式所呼叫的任何函式 (，而不是由另一個函式) 所呼叫的函式所呼叫的函數。

### <a name="uniform-shader-inputs"></a>統一著色器輸入

頂點和圖元著色器接受兩種類型的輸入資料：差異和統一。 不同的輸入是每次執行著色器的唯一資料。 針對頂點著色器，不同的資料 (例如：位置、正常等 ) 來自于頂點資料流程。 統一資料 (例如：材質色彩、世界轉換等 ) 對於著色器的多個執行都是常數。 針對熟悉的元件著色器模型的人，會由常數暫存器和由 v 和 t 註冊的不同資料來指定統一的資料。

您可以透過兩種方法來指定統一的資料。 最常見的方法是宣告全域變數，並在著色器中使用它們。 在著色器中使用全域變數，會導致將該變數加入至該著色器所需的統一變數清單。 第二種方法是將最上層著色器函式的輸入參數標示為統一。 這項標示會指定應該將指定的變數加入至統一變數清單。

著色器所使用的統一變數會透過常數資料表傳回給應用程式。 常數資料表是符號表的名稱，定義著色器所使用的統一變數如何融入常數暫存器中。 統一函式參數會出現在常數資料表中，且前面加上貨幣符號 ($) ，與全域變數不同。 需要貨幣符號，以避免本機統一輸入與相同名稱的全域變數之間發生名稱衝突。

常數資料表包含著色器所使用之所有統一變數的常數註冊位置。 資料表也包含型別資訊和預設值（如果有指定的話）。

### <a name="varying-shader-inputs-and-semantics"></a>不同的著色器輸入和語義

最上層著色器函式 (的不同輸入參數) 必須以語義或統一關鍵字標示，表示執行著色器的值是常數。 如果最上層著色器輸入未以語義或統一關鍵字標示，則著色器將無法編譯。

輸入語義是用來將指定的輸入連結至圖形管線上一個部分之輸出的名稱。 例如，頂點著色器會使用輸入語義 POSITION0 來指定應從頂點緩衝區連結位置資料的位置。

圖元和頂點著色器有不同的輸入語義集合，因為圖形管線的不同部分會送入每個著色器單位。 頂點著色器輸入語義描述每個頂點的資訊 (例如：位置、標準、材質座標、色彩、正切、binormal 等 ) 要從頂點緩衝區載入至可供頂點著色器使用的表單。 輸入語義會直接對應到頂點宣告的使用方式和使用方式索引。

圖元著色器輸入語義會描述由點陣化單位提供的每個圖元所提供的資訊。 資料是藉由在目前基本物件的每個頂點的頂點著色器輸出之間插上插上而產生。 基本圖元著色器輸入語義會將輸出色彩和材質座標資訊連結至輸入參數。

您可以透過兩種方法將輸入語義指派給著色器輸入：

-   將冒號和語義名稱附加至參數宣告。
-   使用指派給每個結構成員的輸入語義來定義輸入結構。

頂點和圖元著色器會將輸出資料提供給後續的圖形管線階段。 輸出語義可用來指定著色器產生的資料應該如何連結至下一個階段的輸入。 例如，頂點著色器的輸出語義會用來連結轉譯器中 interpolators 的輸出，以產生圖元著色器的輸入資料。 圖元著色器輸出是針對每個轉譯目標提供給 Alpha 混色單位的值，或寫入深度緩衝區的深度值。

頂點著色器輸出語義是用來將著色器連結到圖元著色器和轉譯器階段。 由轉譯器取用但未公開給圖元著色器的頂點著色器，必須以最小值產生位置資料。 產生材質座標和色彩資料的頂點著色器會在插補完成之後，將該資料提供給圖元著色器。

圖元著色器輸出語義會以正確的轉譯目標來系結圖元著色器的輸出色彩。 圖元著色器輸出色彩會連結到 Alpha blend 階段，以決定如何修改目的地呈現目標。 圖元著色器深度輸出可以用來變更目前點陣位置的目的地深度值。 只有某些著色器模型支援深度輸出和多個呈現目標。

輸出語義的語法與指定輸入語義的語法相同。 您可以直接在宣告為 "out" 參數或在結構定義期間（以 "out" 參數或函式的傳回值形式傳回）的參數上指定語義。

語法可識別資料的來源。 語義是識別著色器輸入和輸出的選擇性識別碼。 語義會出現在下列三個位置之一：

-   結構成員之後。
-   在函數的輸入引數清單中的引數之後。
-   在函數的輸入引數清單之後。

此範例會使用結構來提供一或多個頂點著色器輸入，並使用另一個結構來提供一或多個頂點著色器輸出。 每個結構成員都使用語義。


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



輸入結構會識別可提供著色器輸入之頂點緩衝區中的資料。 這個著色器會將資料從頂點緩衝區的位置、標準和 blendweight 元素對應到頂點著色器暫存器。 輸入資料類型不需要完全符合頂點宣告資料類型。 如果它不完全相符，頂點資料會在寫入著色器暫存器時自動轉換成 HLSL 的資料類型。 比方說，如果一般資料定義為應用程式的 UINT 型別，則會在著色器讀取時將它轉換成 float3。

如果頂點資料流程中的資料包含的元件比對應的著色器資料類型少，遺漏的元件將會初始化為 0 (但 w 除外，後者會初始化為 1) 。

輸入語義類似于 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage)中的值。

輸出結構會識別位置和色彩的頂點著色器輸出參數。 管線會使用這些輸出 (基本處理) 中的三角形柵格化。 標示為位置資料的輸出會代表頂點在同質空間中的位置。 頂點著色器至少必須產生位置資料。 藉由將 (x，y，z) 座標除以 w，在頂點著色器完成後，會計算螢幕空間位置。 在螢幕空間中，-1 和1是區界界限的最小和最大 x 和 y 值，而 z 則用於 z 緩衝區測試。

輸出語義也類似于 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage)中的值。 一般而言，頂點著色器的輸出結構也可以當做圖元著色器的輸入結構使用，但前提是圖元著色器不會讀取任何標記有位置、點大小或霧化語義的變數。 這些語義與圖元著色器未使用的每個頂點純量值相關聯。 如果圖元著色器需要這些值，則可以將它們複製到另一個使用圖元著色器語義的輸出變數。

全域變數會由編譯器自動指派給註冊。 全域變數也稱為統一參數，因為每次呼叫著色器時所處理的所有圖元的變數內容都相同。 暫存器包含在常數資料表中，您可以使用 [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) 介面來讀取這些暫存器。

圖元著色器的輸入語義可將值對應至端點著色器和圖元著色器之間傳輸的特定硬體暫存器。 每個註冊類型都有特定屬性。 由於色彩和材質座標目前只有兩個語義，因此大部分的資料通常會被標示為材質座標（即使沒有的話）。

請注意，頂點著色器輸出結構使用的輸入具有位置資料，而圖元著色器不會使用此輸入。 HLSL 可讓頂點著色器的有效輸出資料不是圖元著色器的有效輸入資料，前提是它不是在圖元著色器中參考。

輸入引數也可以是陣列。 編譯器會針對陣列的每個元素自動遞增語法。 例如，請考慮下列明確宣告：


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



上述的明確宣告相當於下列宣告，此宣告將會自動遞增編譯器的語義：


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



就像輸入語義一樣，輸出語義也會識別圖元著色器輸出資料的資料使用狀況。 許多圖元著色器只會寫入一個輸出色彩。 圖元著色器也可以同時將深度值寫出一個或多個轉譯目標， (多達四個) 。 和頂點著色器一樣，圖元著色器會使用結構來傳回多個輸出。 此著色器會將0寫入色彩元件以及深度元件。


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



圖元著色器輸出色彩的類型必須是 float4。 撰寫多個色彩時，必須連續使用所有的輸出色彩。 換句話說，除非已寫入[COLOR0](dx-graphics-hlsl-semantics.md) ，否則[COLOR1](dx-graphics-hlsl-semantics.md)不能是輸出。 圖元著色器深度輸出的類型必須是 float1。

### <a name="samplers-and-texture-objects"></a>取樣器和材質物件

取樣器包含取樣器狀態。 取樣器狀態會指定要取樣的材質，並控制取樣期間完成的篩選。 範例材質需要三個專案：

-   材質
-   使用取樣器狀態的取樣器 () 
-   取樣指令

您可以使用紋理和取樣器狀態來初始化取樣器，如下所示：


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



以下是範例2D 材質的程式碼範例：


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



紋理會以材質變數 tex0 來宣告。

在此範例中，會宣告名為 s 2d 的取樣器變數 \_ 。 取樣器包含大括弧內的取樣器狀態。 這包括將取樣的材質，以及（選擇性）篩選狀態 (也就是包裝模式、篩選模式等 ) 。 如果省略取樣器狀態，則會套用預設取樣器狀態，並指定紋理座標的線性篩選和換行模式。 取樣器函式會採用雙元件浮點紋理座標，並傳回兩個元件的色彩。 這會以 float2 傳回類型表示，並代表紅色和綠色元件中的資料。

定義了四種類型的取樣器 (請參閱 [關鍵字](dx-graphics-hlsl-appendix.md)) 和材質查閱是由內建函式執行： [**tex1D (s、t)  (directx HLSL)**](dx-graphics-hlsl-tex1d.md)、 [**tex2D (s、t)  (directx HLSL)**](dx-graphics-hlsl-tex2d.md) [**、tex3D (**](dx-graphics-hlsl-tex3d.md)s、t)  (directx HLSL) 、TEXCUBE (s、t)  ([**directx HLSL)**](dx-graphics-hlsl-texcube.md)。 以下是3D 取樣的範例：


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



這個取樣器宣告使用篩選設定和位址模式的預設取樣器狀態。

以下是對應的 cube 取樣範例：


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



最後，以下是1D 取樣範例：


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



因為執行時間不支援1D 紋理，所以編譯器會使用2D 材質，並知道 y 座標不重要。 由於 [**tex1D (s，t)  (DIRECTX HLSL)**](dx-graphics-hlsl-tex1d.md) 會實作為2d 材質查閱，因此編譯器可以用有效率的方式自由選擇 y 元件。 在某些罕見的情況下，編譯器無法選擇有效率的 y 元件，在此情況下會發出警告。


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



此特定範例效率不佳，因為編譯器必須將輸入座標移至另一個暫存器 (，因為1D 查閱會實作為2D 查閱，並將材質座標宣告為 float1) 。 如果使用 float2 輸入（而非 float1）來重寫程式碼，則編譯器可以使用輸入材質座標，因為它知道 y 會初始化為某個東西。


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



所有紋理查閱都可以使用「偏差」或「proj」 (，也就是 [**tex2Dbias (DIRECTX HLSL)**](dx-graphics-hlsl-tex2dbias.md) [**TEXCUBEPROJ (directx HLSL)**](dx-graphics-hlsl-texcubeproj.md)) 。 使用 "proj" 尾碼時，材質座標會除以 w 元件。 使用「偏差」時，會以 w 元件移位 mip 層級。 因此，所有具有尾碼的材質查閱一律會採用 float4 輸入。 [**tex1D (s、t)  (DIRECTX HLSL)**](dx-graphics-hlsl-tex1d.md) 和 [**tex2D (s，t)  (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) 會分別忽略 yz 和 z 元件。

您也可以在陣列中使用取樣器，雖然沒有後端目前支援取樣器的動態陣列存取。 因此，下列是有效的，因為它可以在編譯時期解決：


```
tex2D(s[0],tex)
```



不過，此範例無效。


```
tex2D(s[a],tex)
```



取樣器的動態存取主要適用于使用常值迴圈來撰寫程式。 下列程式碼說明存取的取樣器陣列：


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> 使用 Microsoft Direct3D debug runtime 可協助您捕捉材質中的元件數目與取樣器之間的不符情形。

 

## <a name="writing-functions"></a>撰寫函數

函式會將大型工作分成較小的工作。 您可以輕鬆地進行較小的工作，而且可以在經過證實之後重複使用。 函數可用來隱藏其他函式的詳細資料，讓函式組成的程式更容易遵循。

HLSL 函式類似于 C 函式，有數種方式：它們都包含定義和函式主體，而且兩者都宣告傳回型別和引數清單。 如同 C 函式，HLSL 驗證會在著色器編譯期間，針對引數、引數類型和傳回值進行型別檢查。

與 C 函式不同的是，HLSL 進入點函式會使用語義將函式引數系結至著色器輸入和輸出 (HLSL 函式會在內部忽略語義) 。 這可讓您更輕鬆地將緩衝區資料系結至著色器，並將著色器輸出系結至著色器輸入。

函式包含宣告和主體，且宣告必須在主體之前。


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



函式宣告包含大括弧前面的所有專案：


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



函式宣告包含：

-   傳回型別
-   函數名稱
-   引數清單 (選擇性) 
-   輸出語義 (選擇性) 
-   批註 (選擇性) 

傳回類型可以是任何 HLSL 基本資料類型，例如 float4：


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



傳回型別可以是已定義的結構：


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



如果函式不會傳回值，void 可以當做傳回型別使用。


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



傳回型別一律會先出現在函式宣告中。


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



引數清單會宣告函式的輸入引數。 它也可以宣告將傳回的值。 某些引數同時為輸入和輸出引數。 以下是採用四個輸入引數的著色器範例。


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



此函式會傳回最終色彩，也就是材質樣本和淺色色彩的 blend。 此函數會接受四個輸入。 兩個輸入具有語義： LightDir 具有 [TEXCOORD1](dx-graphics-hlsl-semantics.md) 語義，而 Texcrd 具有 [TEXCOORD0](dx-graphics-hlsl-semantics.md) 語義。 此語義表示這些變數的資料將來自頂點緩衝區。 雖然 LightDir 變數有 [TEXCOORD1](dx-graphics-hlsl-semantics.md) 語義，但參數可能不是材質座標。 TEXCOORDn 語義型別通常用來提供未預先定義之型別的語義， (沒有淺色方向) 的頂點著色器輸入語義。

另外兩個輸入 LightColor 和 samp 會以 [統一](dx-graphics-hlsl-appendix.md) 關鍵字標記。 這些是不會在繪製呼叫之間變更的統一常數。 這些參數的值來自于著色器全域變數。

您可以使用 in 關鍵字將引數標記為輸入，並使用 out 關鍵字來標記輸出引數。 無法以傳址方式傳遞引數;但是，如果是使用 inout 關鍵字宣告，則引數可以是輸入和輸出。 傳遞給以 inout 關鍵字標記之函式的引數會被視為原來的複本，直到函式傳回為止，然後再複製回來。 以下是使用 inout 的範例：


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



此函式會遞增 A 和 B 中的值，並傳回這些值。

函數主體是函式宣告之後的所有程式碼。


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



主體是由以大括弧括住的語句所組成。 函數主體會使用變數、常值、運算式和語句來執行所有功能。

著色器主體會執行兩項作業：它會執行矩陣相乘，並傳回 float4 結果。 矩陣相乘是利用 [**mul (DIRECTX HLSL)**](dx-graphics-hlsl-mul.md) 函式來完成，這會執行4x4 矩陣相乘。 **mul (DIRECTX HLSL)** 稱為內建函式，因為它已經內建在函式的 HLSL 程式庫中。 下一節將更詳細地討論內建函式。

矩陣乘合併輸入向量 Pos 和複合矩陣 WorldViewProj。 結果是將資料轉換為螢幕空間。 這是我們可以進行的最小頂點著色器處理。 如果我們使用的是固定函式管線，而不是頂點著色器，則可以在執行這項轉換之後繪製頂點資料。

函數主體中的最後一個語句是 return 語句。 就像 C 一樣，這個語句會將 control 從函式傳回給呼叫函數的語句。

函數傳回類型可以是在 HLSL 中定義的任何單一資料型別，包括 bool、int 半形、float 和 double。 傳回類型可以是其中一種複雜的資料類型，例如向量和矩陣。 參考物件的 HLSL 類型不能當做傳回類型使用。 這包括無效、vertexshader、材質和取樣器。

以下是使用傳回型別之結構的函式範例。


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



Float4 傳回型別已取代為結構和 \_ 輸出，現在包含單一 float4 成員。

Return 語句表示函式的結尾。 這是最簡單的 return 語句。 它會將函數的控制權傳回給呼叫程式。 它不會傳回任何值。


```
void main()
{
    return ;
}
```



Return 語句可以傳回一或多個值。 此範例會傳回常值：


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



此範例會傳回運算式的純量結果：


```
return  light.enabled;
```



此範例會傳回由區域變數和常值所構成的 float4：


```
return  float4(color.rgb, 1) ;
```



此範例會傳回從內建函式傳回的結果所建立的 float4，以及一些常值：


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



這個範例會傳回包含一或多個成員的結構：


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a>流量控制

最新的頂點和圖元著色器硬體設計為逐行執行著色器，並執行每個指令。 HLSL 支援 flow 控制，其中包括靜態分支、前提指示、靜態迴圈、動態分支和動態迴圈。

先前，使用 if 語句會產生組合語言著色器程式碼，該程式碼會同時執行程式碼流程的 if 端和 else 端。 以下是針對 vs 1 1 編譯的 HLSL 程式碼範例 \_ \_ ：


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



以下是產生的元件程式碼：


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



有些硬體允許靜態或動態迴圈，但大部分都需要線性執行。 在不支援迴圈的模型上，所有迴圈都必須是展開。 例如，即使是 ps 1 1 著色器，也會使用展開迴圈的 [DepthOfField 範例](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) 範例 \_ \_ 。

HLSL 現在支援下列每種類型的流量控制：

-   靜態分支
-   前提指示
-   靜態迴圈
-   動態分支
-   動態迴圈

靜態分支可讓您根據布林著色器常數，開啟或關閉著色器程式碼區塊。 這是一種方便的方法，可根據目前轉譯的物件類型來啟用或停用程式碼路徑。 您可以使用目前的著色器來決定要支援的功能，然後設定取得該行為所需的布林值旗標，以進行繪製呼叫。 在著色器執行期間，會略過布林值常數停用的任何語句。

最熟悉的分支支援是動態分支。 使用動態分支時，比較準則位於變數中，這表示會在執行時間針對每個頂點或每個圖元進行比較 (而不是在編譯時期進行比較，或在兩個繪製呼叫之間) 。 效能衝擊是分支的成本加上所採用之分支端的指示成本。 動態分支是在著色器模型3或更高版本中執行。 將使用這些模型的著色器優化，類似于將 CPU 上執行的程式碼優化。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HLSL 的程式設計指南](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
