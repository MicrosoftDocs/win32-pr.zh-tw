---
title: vs_3_0
description: 可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103842840"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。

頂點著色器版本與 \_ 3 \_ 0：擴充 vs 2 x 所支援的功能集 \_ \_ 。 Vs \_ 2 X 中需要設定端點的每個功能 \_ ，在 vs 3 0 中都有提供 \_ ， \_ 而不需要端點。

-   [指示-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) 包含可用指令的清單。
-   暫存器[-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)會列出頂點著色器 ALU 所使用的不同類型的暫存器。
-   [頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。
-   [頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。
-   [[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。
-   [目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。

## <a name="new-features"></a>新功能

\_下列各節列出頂點著色器版本與 3 0 的新功能 \_ 。

### <a name="indexing-registers"></a>索引暫存器

在先前的著色器模型中，只能編制常數暫存器 bank 的索引。 在此模型中，您可以使用迴圈計數器 register (aL) 來編制下列註冊銀行的索引：

-   輸入 register (v \#) 
-   Output register (o \#) 

### <a name="vertex-textures"></a>頂點紋理

此著色器模型支援使用 texldl 在頂點著色器中進行紋理查閱。 頂點引擎有四個紋理取樣器階段 (有別于置換圖取樣器和圖元引擎中的材質取樣器) ，可用來在這些階段設定紋理取樣。 請參閱 [vs \_ 3 \_ 0 (DirectX HLSL) 的頂點紋理 ](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)。

### <a name="vertex-stream-frequency"></a>頂點資料流程頻率

這項功能可讓您以不同于每個頂點一次的速率初始化輸入暫存器的子集。 請參閱 [繪圖非索引幾何](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)。

### <a name="shader-output"></a>著色器輸出

與 vs \_ 2 \_ 0 類似，著色器的輸出會隨著靜態流程式控制制而有所不同。 請小心使用動態分支，因為這可能會導致著色器輸出依頂點而異。 這將會在不同的硬體上產生無法預期的結果。

### <a name="dynamic-flow-control"></a>動態流程式控制制

支援所有動態流程式控制制指令。 允許的最大嵌套深度值為24。  (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md) ) 。

### <a name="temporary-registers"></a>臨時暫存器

支援 (r) 的總計32暫存暫存器 \# 。

### <a name="static-flow-control"></a>靜態流程式控制制

[迴圈-vs](loop---vs.md)rep 的最大嵌套深度為 / [](rep---vs.md) 4。 [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz pred-vs](callnz-pred---vs.md)的最大嵌套深度為4。 [若為 bool-vs](if-bool---vs.md)，則允許的最大嵌套深度值為24。  (如需詳細資料，請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md) ) 。

### <a name="predication"></a>預測

支援指令 predication。 使用 [setp \_ comp-vs](setp-comp---vs.md) 來設定述詞註冊。

### <a name="instruction-count"></a>指令計數

每個頂點著色器都允許從512到 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9)中 MaxVertexShader30InstructionSlots 的位置數目。 因為迴圈/rep 支援，所以執行的指令數目可能會更高。不過，這會由 D3DCAPS9 中的 MaxVShaderInstructionsExecuted 限制，其中至少應為0xFFFF。

### <a name="device-caps"></a>裝置 Cap

如果支援頂點著色器 3 \_ 0，硬體 (中最少) 支援下列 caps：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>筆蓋</th>
<th>功能</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>著色器 caps</td>
<td><ul>
<li>DynamicFlowControlDepth 是24</li>
<li>NumTemps 為32</li>
<li>StaticFlowControlDepth 為4</li>
<li>支援 Predication。</li>
</ul></td>
</tr>
<tr class="even">
<td>GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</td>
<td>8K</td>
</tr>
<tr class="odd">
<td>VertexShaderVersion</td>
<td>3_0</td>
</tr>
<tr class="even">
<td>MaxVertexShaderConst</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>霧化支援</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>VertexTextureFilterCaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>頂點宣告中的頂點元素可以共用相同的資料流程位移。</td>
</tr>
<tr class="odd">
<td>頂點格式</td>
<td><ul>
<li>D3DDECLTYPE_UBYTE4</li>
<li>D3DDECLTYPE_UBYTE4N</li>
<li>D3DDECLTYPE_SHORT2N</li>
<li>D3DDECLTYPE_SHORT4N</li>
<li>D3DDECLTYPE_FLOAT16_2</li>
<li>D3DDECLTYPE_FLOAT16_4</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 