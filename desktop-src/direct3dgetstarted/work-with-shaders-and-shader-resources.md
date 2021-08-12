---
title: 使用著色器和著色器資源
description: 現在就來瞭解如何使用著色器和著色器資源來開發 Windows 8 的 Microsoft DirectX 遊戲。
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0152ba74dcc8dd1c602b69d854634502c928a0deefe5521bcab8999954049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288548"
---
# <a name="work-with-shaders-and-shader-resources"></a>使用著色器和著色器資源

現在就來瞭解如何使用著色器和著色器資源來開發 Windows 8 的 Microsoft DirectX 遊戲。 我們已瞭解如何設定圖形裝置和資源，而且您可能甚至已開始修改其管線。 現在讓我們來看一下圖元和頂點著色器。

如果您不熟悉著色器語言，則會依序進行快速討論。 著色器是小型的低層級程式，會在圖形管線中的特定階段進行編譯和執行。 其專長是非常快速的浮點數學運算。 最常見的著色器程式如下：

-   **頂點著色器**—針對場景中的每個頂點執行。 此著色器會在呼叫端應用程式提供給它的頂點緩衝區元素上運作，而且會以最少的方式產生4個元件的位置向量，以將其柵格化到圖元位置。
-   **圖元著色器**—針對轉譯目標中的每個圖元執行。 此著色器會從最簡單管線中 (的上一個著色器階段接收柵格化座標，這會是頂點著色器) ，並傳回該圖元位置) 的色彩 (或其他4個元件值，然後寫入轉譯目標。

此範例包括非常基本的頂點和圖元著色器，只繪製幾何，以及更複雜的著色器，以新增基本的光源計算。

著色器程式是以 Microsoft 高階著色器語言撰寫 (HLSL) 。 HLSL 語法看起來很像 C，但是沒有指標。 著色器程式必須非常精簡且有效率。 如果您的著色器編譯為太多指示，則無法執行，而且會傳回錯誤。  (請注意，所允許的確切指令數目是 [Direct3D 功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)的一部分。 ) 

在 Direct3D 中，著色器不會在執行時間編譯;這些專案會在編譯器的其餘部分編譯時進行編譯。 當您使用 Microsoft Visual Studio 2013 來編譯應用程式時，HLSL 檔案會編譯成 cso () 您的應用程式必須先載入並置於 GPU 記憶體中的檔案，才能進行繪製。 當您封裝應用程式時，請確定您已將這些 CSO 檔案包含在您的應用程式中;這些資產就像是網格和材質一樣。

## <a name="understand-hlsl-semantics"></a>瞭解 HLSL 語義

在繼續之前，請務必花點時間討論 HLSL 語義，因為它們通常是新 Direct3D 開發人員的混淆點。 HLSL 語義是識別應用程式與著色器程式之間傳遞之值的字串。 雖然它們可以是各種可能的字串，但最佳做法是使用表示使用方式的字串 `POSITION` 或 `COLOR` 。 當您要建立常數緩衝區或輸入配置時，可以指派這些語義。 您也可以在語意後附加 0 到 7 的數字，在類似的值使用不同的登錄。 例如：COLOR0、COLOR1、COLOR2...

前置詞為 "SV" 的語義 \_ 是由著色器程式寫入的 *系統值* 語義; 您的遊戲本身 (在 CPU 上執行) 無法修改它們。 一般而言，這些語義包含的值，是來自圖形管線中另一個著色器階段的輸入或輸出，或是由 GPU 完全產生的輸入或輸出。

此外， `SV_` 當語義用來指定著色器階段的輸入或輸出時，也會有不同的行為。 例如， `SV_POSITION` (輸出) 包含在頂點著色器階段期間轉換的頂點資料，而 `SV_POSITION` (*輸入*) 包含圖元位置值，這些值是在點陣化階段期間由 GPU 所插入。

以下是一些常見的 HLSL 語義：

-   `POSITION` 針對頂點緩衝區資料 (*n*) 。 `SV_POSITION` 提供圖元的圖元位置給圖元著色器，且無法由您的遊戲撰寫。
-   `NORMAL` 針對頂點緩衝區所提供的一般資料， (*n*) 。
-   `TEXCOORD` (*n*) 提供給著色器的材質 UV 座標資料。
-   `COLOR` (n) 提供給著色器的 RGBA 色彩資料。 請注意，它的處理方式相同以協調資料，包括在點陣化期間插即值;此語義只是協助您識別它是色彩資料。
-   `SV_Target`\[n \] 用於從圖元著色器寫入目標材質或其他圖元緩衝區。

我們會在討論範例時看到 HLSL 語義的一些範例。

## <a name="read-from-the-constant-buffers"></a>從常數緩衝區讀取

如果該緩衝區以資源的形式附加到其階段，任何著色器都可以從常數緩衝區讀取。 在此範例中，只會指派常數緩衝區給頂點著色器。

常數緩衝區會在兩個位置中宣告：在 c + + 程式碼中，以及將存取它的對應 HLSL 檔中。

以下是在 c + + 程式碼中宣告常數緩衝區結構的方式。


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



當您在 c + + 程式碼中宣告常數緩衝區的結構時，請確定所有資料都已正確對齊16位元組的界限。 若要這麼做，最簡單的方式是使用 [DirectXMath](/windows/desktop/dxmath/directxmath-portal) 類型，例如 **XMFLOAT4** 或 **XMFLOAT4X4**，如範例程式碼所示。 您也可以藉由宣告靜態判斷提示，來防止未對齊的緩衝區：


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



如果 **ConstantBufferStruct** 未對齊16位元組，這行程式碼會在編譯時期造成錯誤。 如需常數緩衝區對齊和封裝的詳細資訊，請參閱 [常數變數的封裝規則](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)。

現在，以下是在頂點著色器 HLSL 中宣告常數緩衝區的方式。


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



所有緩衝區（常數、材質、取樣器或其他）都必須定義暫存器，以便 GPU 可以存取它們。 每個著色器階段最多可允許15個常數緩衝區，而且每個緩衝區最多可以容納4096個常數變數。 使用 register 宣告語法如下所示：

-   **b** _\#_ ：常數緩衝區的註冊 (**cbuffer**) 。
-   **t** _\#_ ： (**tbuffer**) 的材質緩衝區註冊。
-   **s** _\#_ ：為取樣器註冊。  (取樣器會定義材質資源中材質的查閱行為。 ) 

例如，圖元著色器的 HLSL 可能會採用材質和取樣器做為輸入，如下所示。

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

您可自行將常數緩衝區指派給暫存器—當您設定管線時，會將常數緩衝區附加至您在 HLSL 檔案中指派給它的相同位置。 例如，在上一個主題中，呼叫 [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) 會對第一個參數表示 ' 0 '。 這會告知 Direct3D 將常數緩衝區資源附加至 register 0，以符合緩衝區的指派，在 HLSL 檔中 **註冊 (b0)** 。

## <a name="read-from-the-vertex-buffers"></a>從頂點緩衝區讀取

頂點緩衝區會將場景物件的三角形資料提供給頂點著色器 (s) 。 如同常數緩衝區，頂點緩衝區結構是在 c + + 程式碼中使用類似的封裝規則來宣告。


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



在 Direct3D 11 中，沒有適用于頂點資料的標準格式。 相反地，我們會使用描述元來定義自己的頂點資料版面配置;資料欄位會使用 [**D3D11 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) 結構的陣列來定義。 在這裡，我們會顯示簡單的輸入版面配置，其描述與上述結構相同的頂點格式：


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



如果您在修改範例程式碼時，將資料新增至頂點格式，請務必更新輸入版面配置，否則著色器將無法解讀。 您可以修改頂點配置，如下所示：


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



在這種情況下，您將修改輸入版面配置定義，如下所示。


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



每個輸入設定項目定義的前面都會加上字串（例如「位置」或「一般」），這是我們稍早在本主題中討論的語法。 它就像一個控制碼，可協助 GPU 在處理頂點時識別出該元素。 為您的頂點元素選擇常用、有意義的名稱。

就像常數緩衝區一樣，頂點著色器具有連入頂點元素的對應緩衝區定義。  (這就是我們在建立輸入配置時提供端點著色器資源參考的原因-Direct3D 會使用著色器的輸入結構來驗證每個頂點的資料版面配置。 ) 請注意，輸入配置定義與這個 HLSL 緩衝區宣告之間的語義相符。 不過， `COLOR` 它後面會加上 "0"。 如果配置中只宣告一個元素，則不需要新增0，但如果您在 `COLOR` 未來加入宣告更多色彩元素，則最好將它附加。


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>在著色器之間傳遞資料

著色器會在執行時採用輸入類型，並從其主要函數傳回輸出類型。 在上一節中定義的頂點著色器中，輸入類型是 VS \_ 輸入結構，而且我們定義了相符的輸入配置和 c + + 結構。 此結構的陣列用來在 **CreateCube** 方法中建立頂點緩衝區。

頂點著色器會傳回 PS \_ 輸入結構，其至少必須包含4個元件 (float4) 最終頂點位置。 這個位置值必須具有系統值語義， `SV_POSITION` 並為其宣告，使 GPU 具有執行下一個繪製步驟所需的資料。 請注意，頂點著色器輸出和圖元著色器輸入之間沒有1:1 對應;頂點著色器會為每個指定的頂點傳回一個結構，但是圖元著色器會針對每個圖元執行一次。 這是因為每個頂點的資料會先經過點陣化階段。 這個階段會決定您所繪製幾何的「涵蓋」哪些圖元、計算每個圖元的每個頂點資料，然後針對每個圖元呼叫圖元著色器一次。 當您將輸出值進行柵格化時，插補是預設的行為，特別是為了正確處理輸出向量資料 (光向量、每個頂點法線和正切，以及其他) 。


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>檢查頂點著色器

範例頂點著色器非常簡單：採用頂點 (位置和色彩) 、將模型座標中的位置轉換成透視圖投影座標，並將其 (以及轉譯器的色彩) 傳回。 請注意，色彩值會與位置資料直接插入，為每個圖元提供不同的值，即使頂點著色器未對色彩值執行任何計算也是一樣。


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



較複雜的端點著色器，例如設定物件頂點以進行 Phong 的陰影，可能看起來更像這樣。 在此情況下，我們會利用將向量和法線插到接近美觀表面的事實。

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a>檢查圖元著色器

此範例中的這個圖元著色器很可能是您在圖元著色器中可以擁有的最小程式代碼數量。 它會採用在點陣化期間產生的插補圖元色彩資料，並將其傳回做為輸出，然後將它寫入轉譯目標。 乏味！


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



重要的部分是傳回 `SV_TARGET` 值的系統值語義。 它指出輸出會寫入主要轉譯目標，也就是提供給交換鏈的材質緩衝區以供顯示。 這是圖元著色器的必要項（沒有圖元著色器的色彩資料），Direct3D 沒有任何要顯示的資料！

更複雜的圖元著色器範例可執行 Phong 陰影，如下所示。 由於向量和法線是插補的，因此不需要以每圖元為基礎來計算。 不過，我們必須重新正規化它們，因為插補的運作方式;就概念而言，我們必須從頂點 A 方向的方向逐漸「旋轉」至頂點 B 的方向，以維持其長度— wheras 插補會改為在兩個向量端點之間的直線之間剪下。

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

在另一個範例中，圖元著色器會採用自己的常數緩衝區，其中包含燈光和材質資訊。 端點著色器中的輸入配置會展開成包含一般資料，而該頂點著色器的輸出應該包含頂點的轉換向量、燈光，以及視圖座標系統中的頂點。

如果您的材質緩衝區和取樣器具有指派的暫存器 (**t** 和 **s** 分別) ，您也可以在圖元著色器中存取它們。

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

著色器是功能強大的工具，可用來產生像是陰影地圖或雜訊紋理等程式性資源。 事實上，先進的技術要求您將紋理視為更以抽象方式，而不是視覺元素，但作為緩衝區。 它們包含高度資訊等資料，或其他可在最終圖元著色器階段中取樣的資料，或是在多階段效果通過時，可在該特定框架中取樣的資料。 多取樣是一種功能強大的工具，以及許多新式視覺效果的骨幹。

## <a name="next-steps"></a>後續步驟

希望您現在已熟悉 DirectX 11at，並已準備好開始處理您的專案。 以下連結可協助您回答使用 DirectX 和 c + + 進行開發時可能遇到的其他問題：

-   [開發遊戲](/previous-versions/windows/apps/hh452744(v=win.10))
-   [使用 Visual Studio 工具進行 DirectX 遊戲程式設計](/previous-versions/windows/apps/dn166877(v=win.10))
-   [DirectX 遊戲開發和範例逐步解說](/previous-versions/windows/apps/hh465149(v=win.10))
-   [其他遊戲程式設計資源](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectX 裝置資源](work-with-dxgi.md)
</dt> <dt>

[瞭解 Direct3D 11 轉譯管線](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 