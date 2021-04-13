---
title: 語法變數
description: 使用下列語法規則來宣告 HLSL 變數。
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- '外部、變數語法 (DirectX HLSL) '
- 'nointerpolation， (DirectX HLSL 的變數語法) '
- " (DirectX HLSL) 的共用、變數語法"
- 'groupshared， (DirectX HLSL 的變數語法) '
- '靜態、變數語法 (DirectX HLSL) '
- " (DirectX HLSL) 的統一、變數語法"
- 'volatile、變數語法 (DirectX HLSL) '
- " (DirectX HLSL) 的精確、變數語法"
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/11/2020
ms.locfileid: "104991046"
---
# <a name="variable-syntax"></a>語法變數

使用下列語法規則來宣告 HLSL 變數。



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*儲存體 \_類別* \] \[ *類型 \_ 修飾* 詞 \] *類型名稱* \[ *索引* \] \[ *：語義* \] \[ *： Packoffset* \] \[ *： Register* \] ;   \[  \] 批註 \[*= 初始 \_值*                    \] |



 

## <a name="parameters"></a>參數

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*儲存 \_ 類別* 
</dt> <dd>

選擇性的儲存類別修飾詞，可提供關於變數範圍和存留期的編譯器提示;您可以依任何順序指定修飾詞。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>extern</strong></td>
<td>將全域變數標示為著色器的外部輸入;這是所有全域變數的預設標記。 無法與 <strong>static</strong>合併。</td>
</tr>
<tr class="even">
<td><strong>nointerpolation</strong></td>
<td>在將端點著色器傳遞給圖元著色器之前，請勿先插補其輸出。</td>
</tr>
<tr class="odd">
<td><strong>精確</strong></td>
<td>套用至變數的 <strong>精確</strong> 關鍵字會限制任何用來產生以下列方式指派給該變數之值的計算：

*   個別的作業會分開保存。 例如，mul 和 add 作業可能已融合到 mad 作業中， <strong>精確</strong> 地強制操作保持獨立。 相反地，您必須明確地使用 mad 內建函式。
*   維護作業的順序。 其中的指令順序可能已隨機放置，以改善效能， <strong>精確</strong> 地確保編譯器會保留所寫入的順序。
*   不受限於 IEEE unsafe 作業。 編譯器可能會使用的快速數學運算不會將其用於 NaN (而不是) ，而 INF (無限) 值的情況下，會 <strong>精確</strong> 地強制遵循與 NAN 和 inf 值有關的 IEEE 需求。 如果沒有 <strong>精確</strong>，則這些優化和數學運算不是 IEEE 安全的。
*   <strong>精確</strong>地限定變數並不會讓使用變數<strong>精確</strong>的作業。 由於 <strong>精確</strong> 地只會傳播至參與指派給 <strong>精確</strong>變數之值的作業，所以正確地 <strong>精確</strong> 地計算所需的計算可能會很困難，因此我們建議您在宣告著色器時 <strong>，直接將</strong> 著色器輸出標記為明確地，不論是在結構欄位上，或是在輸入函式的傳回型別上。

以這種方式控制優化的能力，會藉由停用可能會影響最終結果的優化（因為累積的精確度差異差異），來維持已修改之輸出變數的結果 invariance。 當您想要讓鑲嵌式的著色器維持水緊密的 patch 接縫，或比對多個行程的深度值時，它會很有用。

[範例程式碼](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)： 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><strong>共用</strong></td>
<td>標示變數以在效果之間共用;這是編譯器的提示。</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>標記執行緒群組的變數-計算著色器的共用記憶體。 在 D3D10 中，所有具有 groupshared 儲存類別之變數的總大小上限為16kb，D3D11 中的大小上限為32kb。 請參閱範例。</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>標記本機變數，使其初始化一次，並在函式呼叫之間保存。 如果宣告不包含初始化運算式，則值會設定為零。 應用程式看不到標記為 <strong>static</strong> 的全域變數。</td>
</tr>
<tr class="odd">
<td><strong>均勻</strong></td>
<td>在著色器 (（例如，頂點著色器中的材質色彩）中，標記其資料為常數的變數) ;全域變數預設會被視為 <strong>統一</strong> 。</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>標記經常變更的變數;這是編譯器的提示。 這個儲存類別修飾詞只適用于本機變數。<br/>
<blockquote>
[!Note]<br />
HLSL 編譯器目前會忽略這個儲存類別修飾詞。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*類型 \_ 修飾詞*
</dt> <dd>

選擇性的變數類型修飾詞。



| 值             | 描述                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | 標記無法由著色器變更的變數，因此必須在變數宣告中初始化。 全域變數預設會被視為 **const** (藉由提供編譯器) 的/Gec 旗標來抑制此行為。 |
| **資料列 \_ 主要**    | 標記將四個元件儲存在單一資料列中的變數，讓它們可以儲存在單一常數暫存器中。                                                                                                                             |
| **資料行 \_ 主要** | 標記將4個元件儲存在單一資料行中的變數，以優化矩陣數學。                                                                                                                                                         |



 

> [!Note]  
> 如果您未指定類型修飾詞值，編譯器會使用 [資料 **行 \_ 主要** ] 作為預設值。

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*類型*
</dt> <dd>

資料類型中所列的任何 HLSL 類型 [ (DIRECTX HLSL) ](dx-graphics-hlsl-data-types.md)。

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*名稱* \[*索引*\]
</dt> <dd>

可唯一識別著色器變數的 ASCII 字串。 若要定義選擇性陣列，請使用 **index** 作為陣列大小，也就是正整數 = 1。

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*語義*
</dt> <dd>

選擇性的參數使用方式資訊，由編譯器用來連結著色器的輸入和輸出。 頂點和圖元著色器有數個預先定義的 [語義](dx-graphics-hlsl-semantics.md) 。 編譯器會忽略語義，除非宣告于全域變數上，或是傳遞至著色器的參數。

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

手動封裝著色器常數的選擇性關鍵字。 請參閱 [packoffset (DIRECTX HLSL) ](dx-graphics-hlsl-variable-packoffset.md)。

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*註冊*
</dt> <dd>

選擇性的關鍵字，可將著色器變數手動指派給特定的註冊。 請參閱 [註冊 (DIRECTX HLSL) ](dx-graphics-hlsl-variable-register.md)。

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*注釋 (s)*
</dt> <dd>

附加至全域變數的選擇性中繼資料（以字串形式）。 批註會由效果架構使用，並由 HLSL 忽略;若要查看更詳細的語法，請參閱 [批註語法](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax)。

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*初始值 \_*
</dt> <dd>

選擇性初始值 (s) ;值的數目應符合 *型* 別中的元件數目。 每個標記為 **extern** 的全域變數都必須使用常值來初始化;標記為 **static** 的每個變數都必須使用常數進行初始化。

未標記為 **static** 或 **extern** 的全域變數不會編譯成著色器。 編譯器不會自動設定全域變數的預設值，也無法在優化中使用它們。 若要初始化這種類型的全域變數，請使用反映來取得其值，然後將值複製到常數緩衝區。 例如，您可以使用 [**ID3D11ShaderReflection：： GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname)方法來取得變數、使用 [**ID3D11ShaderReflectionVariable：： GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc)方法取得著色器變數的描述，以及從 [**D3D11 \_ 著色器 \_ 變數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc)結構的 **DefaultValue** 成員取得初始值。 若要將值複製到常數緩衝區，您必須確定已使用 CPU 寫入存取建立緩衝區 ([**D3D11 \_ cpu \_ 存取 \_ 寫入**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)) 。 如需如何建立常數緩衝區的詳細資訊，請參閱 [如何：建立常數緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)。

您也可以使用 [效果架構](../direct3d11/d3d11-graphics-programming-guide-effects.md) 來自動處理反映和設定初始值。 例如，您可以使用 [**ID3DX11EffectPass：： Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) 方法。

</dd> </dl>

## <a name="examples"></a>範例

以下是一些著色器變數宣告的範例。


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a>群組共用

HLSL 可讓計算著色器的執行緒透過共用記憶體交換值。 HLSL 提供關卡基本類型（例如 [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)），依此類推以確保在著色器中讀取和寫入共用記憶體的正確順序，並避免資料競爭。

> [!Note]  
> 硬體會以群組 (warps 或 wave) 的方式來執行執行緒，而在只同步屬於相同群組的執行緒是正確的情況下，有時可能會省略關卡同步處理來提高效能。 但基於下列原因，我們強烈建議您省略：
>
> -   這項省略會導致無法移植的程式碼，這可能無法在某些硬體上運作，也不適用於通常以較小的群組執行執行緒的軟體 rasterizers。
> -   相較于使用所有線程屏障，您可能會使用此省略來達成的效能改進。

 

在 Direct3D 10 中，寫入至 **groupshared** 時，不會同步處理執行緒，這表示每個執行緒會限制為數組中的單一位置以進行寫入。 寫入時，請使用 [SV \_ GroupIndex](dx-graphics-hlsl-semantics.md) 系統值來編制此陣列的索引，以確保兩個執行緒都不會發生衝突。 就讀取而言，所有線程都可以存取整個陣列以進行讀取。


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a>包裝

封裝大小夠大的向量和純量子元件，以防止 boundarys 的註冊。 例如，這些都是有效的：


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



無法混合封裝類型。

就像 register 關鍵字一樣，packoffset 可以是特定的目標。 子元件封裝僅適用于 packoffset 關鍵字，而非 register 關鍵字。 在 cbuffer 宣告中，Direct3D 10 目標會忽略 register 關鍵字，因為它會被假設為跨平臺相容性。

封裝的元素可能會重迭，而編譯器將不會發出任何錯誤或警告。 在此範例中，Element2 和 Element3 會與 Element1. x 和 Element1 重迭。


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



使用 packoffset 的範例是： [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的變數 ](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

