---
title: 著色器常數 (HLSL)
description: 在著色器模型4中，著色器常數會儲存在記憶體中的一或多個緩衝區資源中。
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- 常數緩衝區
- 材質緩衝區
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685390"
---
# <a name="shader-constants-hlsl"></a>著色器常數 (HLSL)

在著色器模型4中，著色器常數會儲存在記憶體中的一或多個緩衝區資源中。 它們可以組織成兩種類型的緩衝區：常數緩衝區 (cbuffers) 和材質緩衝區 (tbuffers) 。 常數緩衝區最適合用於常數變數的使用方式，其以較低延遲的存取和 CPU 較頻繁的更新為特徵。 基於這個理由，其他大小、配置和存取限制適用于這些資源。 紋理緩衝區會像材質一樣存取，並針對任意索引的資料執行得更好。 無論您使用哪種類型的資源，應用程式可以建立的常數緩衝區或紋理緩衝區數目沒有任何限制。

宣告常數緩衝區或紋理緩衝區看起來很像 C 中的結構宣告，而是新增 **register** 和 **packoffset** 關鍵字以手動指派暫存器或封裝資料。



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[*名稱* \]\[： **register** (b \#) \] { *VariableDeclaration* \[ ： **packoffset** (c. \# xyzw) \] ;     ... }; |



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[在 \] 緩衝區類型中。



| BufferType | Description     |
|------------|-----------------|
| cbuffer    | 常數緩衝區 |
| tbuffer    | 材質緩衝區  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

\[\]（選擇性）包含唯一緩衝區名稱的 ASCII 字串。

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**註冊** (b \#) 
</dt> <dd>

\[\]使用選擇性的關鍵字，用來手動封裝常數資料。 常數只能在常數緩衝區中封裝于暫存器中，而在此情況下， () 的暫存器編號會提供開始登錄 *\#* 。

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[在 \] 變數宣告中，類似于結構成員宣告。 這可以是任何 HLSL 類型或效果物件 (但) 的材質或取樣器物件除外。

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset** (c. \# xyzw) 
</dt> <dd>

\[\]使用選擇性的關鍵字，用來手動封裝常數資料。 常數可以封裝在任何常數緩衝區中，其中的暫存器編號是由 (*\#*) 指定。 使用 xyzw swizzling) 的子元件封裝 (可用於大小符合單一登入 (不會跨越暫存器界限) 的常數。 比方說，float4 無法封裝在開頭為 y 元件的單一登入中，因為它無法容納在四個元件的暫存器中。

</dd> </dl>

## <a name="remarks"></a>備註

常數緩衝區透過允許著色器常數群組在一起並且同時認可，而不是進行個別呼叫以分別認可每一個常數，來減少更新著色器常數所需的頻寬。

常數緩衝區是像緩衝區一樣存取的特製化緩衝區資源。 每個常數緩衝區最多可容納4096個 [向量](dx-graphics-hlsl-vector.md);每個向量最多包含 4 32 位值。 您最多可以在每個管線階段系結14個常數緩衝區 (2 個額外的插槽保留供內部使用) 。

材質緩衝區是以材質形式存取的特製化緩衝區資源。 材質存取 (相較于緩衝區存取，) 可為任意索引的資料提供更好的效能。 您最多可以為每個管線階段系結128紋理緩衝區。

緩衝區資源的設計目的是要將設定著色器常數的額外負荷降到最低。 效果架構 (查看 [**ID3D10Effect 介面**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) 將會管理更新常數和材質緩衝區，或您可以使用 direct3d API 來更新緩衝區 (如需資訊) ，請參閱 [複製和存取資源資料 (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) 。 應用程式也可以將資料從另一個緩衝區 (例如轉譯目標或資料流程輸出目標) 複製到常數緩衝區。

如需在 D3D10 應用程式中使用常數緩衝區的詳細資訊，請參閱 [ (direct3d 10) 的資源類型 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) ，以及 [ (Direct3d 10) 建立緩衝區資源 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)。

如需在 D3D11 應用程式中使用常數緩衝區的 morel 資訊，請參閱 [Direct3D 11 中的緩衝區簡介](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) 和 [如何：建立常數緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)。

常數緩衝區不需要將 [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) 系結至管線。 不過，材質緩衝區需要一個視圖，而且必須系結至材質位置 (或在使用效果) 時必須與 [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) 系結。

有兩種方式可以封裝常數資料：使用 [register (DIRECTX HLSL) ](dx-graphics-hlsl-variable-register.md) 和 [PACKOFFSET (directx HLSL) ](dx-graphics-hlsl-variable-packoffset.md) 關鍵字。



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 10 和11之間的差異：<br/> 不同于 Direct3D 9 中未執行封裝，而改為將每個變數指派給一組 float4 暫存器的常數的自動設定，HLSL 常數變數在 Direct3D 10 和11中遵循封裝規則。<br/> |



 

### <a name="organizing-constant-buffers"></a>組織常數緩衝區

常數緩衝區透過允許著色器常數群組在一起並且同時認可，而不是進行個別呼叫以分別認可每一個常數，來減少更新著色器常數所需的頻寬。

有效使用常數緩衝區的最佳方法是根據它們的更新頻率，將著色器變數組織到常數緩衝區。 這可讓應用程式將更新著色器常數所需的頻寬降至最低。 例如，著色器可能會宣告兩個常數緩衝區，並根據更新的頻率來組織每個常數的資料：需要針對每個物件更新的資料 (例如世界矩陣) 會分組到可針對每個物件更新的常數緩衝區。 這與場景的特性不同，因此可能會在場景變更) 時較不常更新 (。


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a>預設常數緩衝區

有兩個預設的常數緩衝區可用，$Global 和 $Param。 放在全域範圍中的變數，會使用用於 cbuffers 的相同封裝方法，隱含地新增至 $Global cbuffer。 當著色器在效果架構之外編譯時，函式參數清單中的統一參數會出現在 $Param 常數緩衝區中。 在效果架構內進行編譯時，所有 uniforms 都必須解析為全域範圍中定義的變數。

## <a name="examples"></a>範例

以下是來自 [Skinning10 範例](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) 的範例，此範例是由矩陣陣列組成的材質緩衝區。


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



這個範例宣告會手動指派常數緩衝區以從特定的暫存器開始，也會依子元件封裝特定的元素。


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

