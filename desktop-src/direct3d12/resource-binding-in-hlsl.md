---
title: HLSL 中的資源系結
description: 本主題說明使用高階著色器語言 (HLSL) 著色器模型5.1 與 Direct3D 12 的一些特定功能。
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548422"
---
# <a name="resource-binding-in-hlsl"></a>HLSL 中的資源系結

本主題說明使用高階著色器語言 (HLSL) [著色器模型 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) 與 Direct3D 12 的一些特定功能。 所有 Direct3D 12 硬體都支援著色器模型5.1，因此對此模型的支援不會相依于硬體功能層級。

-   [資源類型和陣列](#resource-types-and-arrays)
-   [描述元陣列和材質陣列](#descriptor-arrays-and-texture-arrays)
-   [資源別名](#resource-aliasing)
-   [發散和衍生](#divergence-and-derivatives)
-   [圖元著色器中的 UAVs](#uavs-in-pixel-shaders)
-   [常數緩衝區](#constant-buffers)
-   [SM 5.1 的位元組位元組變更](#bytecode-changes-in-sm51)
-   [範例 HLSL 宣告](#example-hlsl-declarations)
-   [相關主題](#related-topics)

## <a name="resource-types-and-arrays"></a>資源類型和陣列

著色器模型 5 (SM 5.0) 資源語法使用 `register` 關鍵字將資源的重要資訊轉送至 HLSL 編譯器。 例如，下列語句會宣告四個在插槽 t3、t4、t5 和 t6 系結的材質陣列。 t3 是出現在語句中的唯一暫存器位置，只是在四個數組中的第一個位置。

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

著色器模型 5.1 (SM 5.1) HLSL 中的資源語法是以現有的暫存器資源語法為基礎，可讓您更輕鬆地移植。 HLSL 中的 Direct3D 12 資源會系結至邏輯暫存器空間內的虛擬暫存器：

-   t –適用于著色器資源檢視 (SRV) 
-   s-適用于取樣器
-   u –適用于未排序的存取視圖 (UAV) 
-   b –適用于常數緩衝區視圖 (CBV) 

參考著色器的根簽章必須與宣告的註冊位置相容。 例如，下列部分的根簽章與使用材質槽 t3 至 t6 相容，因為它描述具有位置 t0 到 t98 的描述項資料表。

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

資源宣告可以是純量、1D 陣列或多維陣列：

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM 5.1 使用的資源類型和元素類型與 SM 5.0 相同。 SM 5.1 宣告限制較具彈性，且僅受限於執行時間/硬體限制。 `space`關鍵字會指定所宣告變數所系結的邏輯暫存器空間。 如果 `space` 省略關鍵字，則預設空間索引0會隱含地指派給範圍 (，因此上方的範圍位於 `tex2` `space0`) 。 `register(t3,  space0)` 永遠不會與 `register(t3,  space1)` 另一個空間中可能包含 t3 的任何陣列發生衝突。

陣列資源可能具有未系結的大小，其宣告方式是將第一個維度指定為空的，或0：

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

相符的描述項資料表可以是：

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

HLSL 中的未系結陣列與描述項資料表中的固定數位組相同 `numDescriptors` ，而且 HLSL 中的固定大小與描述項資料表中的未系結宣告相符。

允許多維度陣列，包括未系結的大小。 這些多維陣列會在暫存器空間中壓平合併。

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

不允許資源範圍的別名。 換句話說，對於每個資源類型 (t、s、u、b) ，宣告的登錄範圍不得重迭。 這也包括未系結的範圍。 在不同的暫存器空間中宣告的範圍絕不會重迭。 請注意，上述) 的未系結 `tex2` (存在於中 `space0` ，而未系結存在 `tex3` 于中 `space1` ，因此不會重迭。

存取已經宣告為數組的資源，就像編制它們的索引一樣簡單。

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

在使用索引時，有一個重要的預設限制 (在 `myMaterialID` `samplerID` 上述程式碼中) ，因為它們不允許在 [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)內改變。 甚至變更以實例為基礎的索引也會依變化計算。

如果需要改變索引 `NonUniformResourceIndex` ，請在索引上指定辨識符號，例如：

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

在某些硬體上，使用此限定詞會產生額外的程式碼，以強制執行正確性 (包括跨執行緒) 但以較小的效能成本。 如果在沒有此限定詞的情況下變更索引，並在繪製/分派內變更，則結果為未定義。

## <a name="descriptor-arrays-and-texture-arrays"></a>描述元陣列和材質陣列

自 DirectX 10 之後，已可使用材質陣列。 紋理陣列需要一個描述項，不過所有陣列配量都必須共用相同的格式、寬度、高度和 mip 計數。 此外，陣列必須在虛擬位址空間中佔用連續的範圍。 下列程式碼顯示從著色器存取材質陣列的範例。

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

在紋理陣列中，索引可以自由地改變，而不需要像這樣的限定詞 `NonUniformResourceIndex` 。

對等描述元陣列會是：

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

請注意，陣列索引的 float 用法不難用 `myTex2D[2]` 。 此外，描述元陣列也可提供更大的彈性給維度。 `Texture2D`這個範例中的型別不能改變，但 format、width、height 和 mip count 都可以與每個描述項不同。

有紋理陣列的描述元陣列是合法的：

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

宣告結構的陣列，每個包含描述項的結構都不合法，例如，不支援下列程式碼。

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

這會允許記憶體配置 **abcabcabc**...，但這是語言限制，不受支援。 其中一個支援的方法是如下所示，雖然在此案例中的記憶體配置是 **aaa .。。Bbb。。。ccc ...**

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

若要達到 **abcabcabc ...** 記憶體配置，請使用描述中繼資料表，而不使用 `myStruct` 結構。

## <a name="resource-aliasing"></a>資源別名

HLSL 著色器中指定的資源範圍是邏輯範圍。 它們會在執行時間透過根簽章機制系結至具體堆積範圍。 一般來說，邏輯範圍會對應至不會與其他堆積範圍重迭的堆積範圍。 不過，根簽章機制可 (重迭) 相容類型的堆積範圍。 例如， `tex2` 上述範例中的和 `tex3` 範圍可能會對應到相同的 (或重迭的) 堆積範圍，其具有在 HLSL 程式中對材質進行別名的影響。 如果需要這類別名，您必須使用 D3D10 \_ 著色器資源的別名選項來編譯著色器 \_ ，此 \_ \_ 選項是使用 [效果編譯器工具](/windows/desktop/direct3dtools/fxc) (fxc.exe) 的 [ */res] \_ 可能 \_ 別名* 選項來設定。 選項讓編譯器在假設資源可能為別名的情況下，防止特定的負載/存放區優化，以產生正確的程式碼。

## <a name="divergence-and-derivatives"></a>發散和衍生

SM 5.1 不會限制資源索引;亦即， ` tex2[idx].Sample(…)` 索引 idx 可以是常值常數、cbuffer 常數或插入值。 雖然程式設計模型提供極大的彈性，但有一些問題需要注意：

-   如果索引分歧在四個四個，則硬體計算的衍生和衍生數量（例如」 LOD）可能會未定義。 在此情況下，HLSL 編譯器會盡力發出警告，但不會防止編譯著色器。 此行為類似于分歧控制流程中的計算衍生。
-   如果資源索引是分歧的，則相較于統一索引的案例，效能會降低，因為硬體需要在多個資源上執行作業。 在 HLSL 程式碼中，必須以函式來標記可能是分歧的資源索引 `NonUniformResourceIndex` 。 否則會產生未定義的結果。

## <a name="uavs-in-pixel-shaders"></a>圖元著色器中的 UAVs

SM 5.1 不會限制圖元著色器中 UAV 範圍的條件約束，如同 SM 5.0 的情況。

## <a name="constant-buffers"></a>常數緩衝區

SM 5.1 常數緩衝區 (cbuffer) 語法已從 SM 5.0 變更，讓開發人員可以索引常數緩衝區。 為了啟用可編制索引的常數緩衝區，SM 5.1 引進了「 `ConstantBuffer` 範本」結構：

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

上述程式碼會宣告類型和大小為6的常數緩衝區變數 `myCB1` `Foo` ，以及純量常數緩衝區變數 `myCB2` 。 常數緩衝區變數現在可以在著色器中建立索引，如下所示：

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

欄位 ' a ' 和 ' b ' 不會成為全域變數，而是必須視為欄位。 為了回溯相容性，SM 5.1 針對純量 cbuffers 支援舊的 cbuffer 概念。 下列語句會使 ' a ' 和 ' b ' 全域唯讀變數（如同在 SM 5.0 中一樣）。 不過，這類舊樣式的 cbuffer 無法進行索引。

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

目前，著色器編譯器只支援 `ConstantBuffer` 使用者定義結構的範本。

基於相容性的理由，HLSL 編譯器可能會自動為中宣告的範圍指派資源暫存器 `space0` 。 如果在 register 子句中省略了 ' space '，則 `space0` 會使用預設值。 編譯器會使用第一個洞的啟發學習法來指派暫存器。 您可以透過反映 API 來抓取指派，該 API 已擴充為新增空間的 *空間* 欄位，而 *BindPoint* 欄位指出資源暫存器範圍的下限。

## <a name="bytecode-changes-in-sm51"></a>SM 5.1 的位元組位元組變更

SM 5.1 變更如何在指示中宣告和參考資源暫存器。 語法包含宣告暫存器「變數」，類似于針對群組共用記憶體暫存器進行的作業：

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

這會將它分解為：

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

每個著色器資源範圍現在都有一個識別碼， (著色器位元組程式碼的唯一) 名稱。 例如，在著色器位元組程式碼中，tex1 (t10) 材質陣列變成不是 1 '。 將唯一識別碼提供給每個資源範圍，可提供兩個專案：

-   明確識別哪些資源範圍 (請參閱 \_ \_) 的指令索引 (查看範例指示) 。
-   將一組屬性附加至宣告，例如元素類型、跨距大小、點陣作業模式等。

請注意，範圍的識別碼與 HLSL 下限宣告沒有關聯。

反映資源系結的順序 (在頂端的) 和著色器宣告指示 (\_ \*) 相同，以協助識別 HLSL 變數和位元組程式碼識別碼之間的對應。

SM 5.1 中的每個宣告指令都使用3D 運算元來定義：範圍識別碼、下限和上限。 發出額外的權杖來指定註冊空間。 可能也會發出其他標記，以傳達範圍的其他屬性，例如，cbuffer 或結構化的緩衝區宣告指令會發出 cbuffer 或結構的大小。 您可以在 d3d12TokenizedProgramFormat 和 **D3D10ShaderBinary：： CShaderCodeParser** 中找到編碼的確切詳細資料。

SM 5.1 指示將不會發出額外的資源運算元資訊做為指令 (的一部分，如同 SM 5.0) 。 這項資訊現在位於宣告指示中。 在 SM 5.0 中，為資源編制索引所需的資源屬性必須在擴充的 opcode 權杖中描述，因為索引將關聯性模糊至宣告。 在 SM 5.1 中，每個識別碼 (例如 ' t 1 ' ) 明確地與單一宣告相關聯，以描述所需的資源資訊。 因此，不會再發出用來描述資源資訊之指示的延伸操作碼權杖。

在非宣告的指示中，取樣器、SRVs 和 UAVs 的資源運算元是2D 運算元。 第一個索引是指定範圍識別碼的常值常數。 第二個索引代表索引的 linearized 值。 相對於對應的登錄空間的開頭，會計算此值， (不是相對於邏輯範圍的開頭) 為了讓與根簽章更好的相互關聯，以及降低調整索引的驅動程式編譯器負擔。

CBVs 的資源運算元是一種3D 運算元，包含：範圍的常值識別碼、常數緩衝區的索引，以及常數緩衝區特定實例中的位移。

## <a name="example-hlsl-declarations"></a>範例 HLSL 宣告

HLSL 程式不需要知道根簽章的任何相關資訊。 他們可以將系結指派給虛擬「註冊」系結空間、t \# For SRVs、u \# for UAVs、b \# for CBVs、s \# 進行取樣器，或是依賴編譯器來挑選指派 (，然後在) 之後使用著色器反映來查詢產生的對應。 根簽章會將描述中繼資料表、根描述元和根常數對應至此虛擬登錄空間。

以下是 HLSL 著色器可能具有的一些宣告範例。 請注意，沒有根簽章或描述中繼資料表的參考。

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 HLSL 5.1 的動態索引](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[效果-編譯器工具](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[依轉譯器排序的視圖](rasterizer-order-views.md)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> <dt>

[根簽章](root-signatures.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[著色器指定的樣板參考值](shader-specified-stencil-reference-value.md)
</dt> <dt>

[在 HLSL 中指定根簽章](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 