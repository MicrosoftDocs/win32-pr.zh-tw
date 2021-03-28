---
title: '著色器模型 3 (HLSL 參考) '
description: 頂點著色器和圖元著色器會從舊版著色器中大幅簡化。
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375681"
---
# <a name="shader-model-3-hlsl-reference"></a>著色器模型 3 (HLSL 參考) 

頂點著色器和圖元著色器會從舊版著色器中大幅簡化。 如果您在硬體中執行著色器，您可能不會使用 vs \_ 3 \_ 0 或 ps \_ 3 \_ 0 搭配任何其他著色器版本，也不能使用任何著色器類型搭配固定函式管線。 這些變更可讓您簡化驅動程式和執行時間。 唯一的例外是，僅限軟體的 vs \_ 3 \_ 0 著色器可搭配任何圖元著色器版本使用。 此外，如果您使用僅限軟體的 vs \_ 3 \_ 0 著色器與先前的圖元著色器版本，頂點著色器只能使用與彈性頂點格式相容的輸出語義 (FVF) 代碼。

在頂點著色器輸出上使用的語義必須在圖元著色器輸入上使用。 此語義可用來將頂點著色器輸出對應至圖元著色器輸入，類似于頂點宣告對應至頂點著色器輸入暫存器和先前著色器模型的方式。 請參閱 vs 3.0 和 ps 3.0 著色器的 Match 語義。

已新增其他換行模式轉譯狀態，以涵蓋此新配置中額外紋理座標的可能性。 具有 D3DDECLUSAGE TEXCOORD 的屬性 \_ 和從0到15的使用方式索引，會在設定對應 [**的 \_ D3DRS \* 換行**](/windows/desktop/direct3d9/d3drenderstatetype)時，以 wrap 模式插補。

-   [頂點著色器模型3功能](#vertex-shader-model-3-features)
-   [圖元著色器模型3功能](#pixel-shader-model-3-features)
-   [Vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 著色器的 Match 語義](/windows)
-   [霧化、深度和網底模式變更](#fog-depth-and-shading-mode-changes)
-   [浮點數和整數轉換](#floating-point-and-integer-conversions)
-   [指定完整或部分有效位數](#specifying-full-or-partial-precision)
-   [軟體頂點和圖元著色器](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>頂點著色器模型3功能

頂點著色器輸出暫存器類型已折迭為十二個暫存器 (請參閱 [輸出](dx9-graphics-reference-asm-vs-registers-output.md) 暫存器) 。 每個使用的暫存器都必須使用 [dcl](dcl-usage---ps.md) 指令和語義 (（例如，dcl \_ color0 o0. xyzw) ）來宣告。

3 \_ 0 頂點著色器模型 (vs \_ 3 \_ 0) 使用更強大的暫存器 \_ \_ 索引、一組簡化的輸出暫存器、在頂點著色器中取樣材質的能力，以及控制著色器輸入初始化速度的能力，來擴充 vs 2 0 的功能。

### <a name="index-any-register"></a>編制任何註冊的索引

您可以使用[迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)暫存器來編制所有 ([輸入](dx9-graphics-reference-asm-vs-registers-input.md)登錄和[輸出](dx9-graphics-reference-asm-vs-registers-output.md)暫存器) 的暫存器 (只有常數暫存器可以在舊版中編制索引。 ) 

您必須先宣告輸入和輸出暫存器，再為它們編制索引。 不過，您不能為任何以位置或點大小語義宣告的輸出暫存器編制索引。 事實上，如果使用索引編制，就必須分別在 o0 和 o1 登錄中宣告位置和 psize 的語法。

您只允許為連續的暫存器範圍編制索引;也就是說，您無法在尚未宣告的暫存器之間進行索引。 雖然這種限制可能很不方便，但卻允許進行硬體優化。 嘗試在非連續的暫存器中編制索引，將會產生未定義的結果。 著色器驗證不會強制執行這種限制。

### <a name="simplify-output-registers"></a>簡化輸出暫存器

所有不同類型的輸出暫存器已折迭為十二個輸出暫存器：1代表位置、2表示色彩、8表示材質，1表示霧化或點大小。 這些暫存器將會插補任何針對圖元著色器所包含的資料。 輸出暫存器宣告是必要的，而且會將語義指派給每個註冊。

暫存器可以依照下列方式細分：

-   至少必須將一個暫存器宣告為四個元件的位置註冊。 這是唯一必要的頂點著色器暫存器。
-   著色器所耗用的前十個暫存器最多可以使用四個元件 (xyzw) 最大值。
-   最後一個 (或第十二個) 登錄只可包含純量 (例如) 的點大小。

如需暫存器的清單，請參閱暫存器 [-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)。

### <a name="texture-sample-in-a-vertex-shader"></a>頂點著色器中的材質範例

頂點著色器 3 \_ 0 支援使用 [texldl](texldl---vs.md)與頂點著色器中的材質查閱

## <a name="pixel-shader-model-3-features"></a>圖元著色器模型3功能

圖元著色器色彩和材質暫存器已折迭為十個輸入暫存器 (查看輸入暫存器 [類型](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)) 。 臉部暫存器是浮點純量暫存器。 只有此註冊的正負號有效。 如果正負號為負數，則基本型別會是背面的臉部。 例如，您可以在圖元著色器內使用它來達成雙面光源。 位置暫存器會參考目前的 (x，y) 圖元。

您可以使用下列內容來設定著色器常數暫存器：

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 著色器的 Match 語義

Vs \_ 3 \_ 0 和 ps \_ 3 0 有一些語義用法的限制 \_ 。 一般情況下，使用符合著色器輸出所使用之語義的著色器輸入時，您必須特別小心。

比方說，這個圖元著色器會將多個名稱封裝成一個暫存器：


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



每個註冊程式都有不同的語義。 請注意，您也可以使用不同 (多個) 的語法來命名 v0. x 和 yz，因為使用寫入遮罩。

由於圖元著色器的比較，以下的 vs \_ 3 \_ 0 著色器無法與其配對：


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



這兩個著色器與 [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) 和 **D3DDECLUSAGE \_ TEXCOORD1** 語義的使用衝突。

重寫類似的頂點著色器，以避免語義衝突：


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



同樣地，在圖元著色器中不同輸入暫存器上所宣告的語義名稱 (v0，而圖元著色器中的 v1) 不能用在這個頂點著色器的單一輸出暫存器中。 比方說，這個頂點著色器無法與圖元著色器配對，因為 D3DDECLUSAGE \_ TEXCOORD1 同時用於圖元著色器輸入暫存器 (v0、v1) 和頂點著色器輸出 register o3。


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



另一方面，此頂點著色器無法與圖元著色器配對，因為具有指定語義之參數的輸出遮罩不會提供圖元著色器所要求的資料：


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



此頂點著色器不會提供圖元著色器所要求的其中一個語義名稱的輸出，因此著色器配對無效：


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a>霧化、深度和網底模式變更

在 \_ 裁剪和三角形柵格化期間設定 D3DRS SHADEMODE 的平面陰影時，具有 D3DDECLUSAGE \_ 色彩的屬性會以平面陰影的方式插補。 如果登錄的任何元件是以色彩語義宣告，但相同暫存器的其他元件是以不同的語義來宣告，則在該暫存器中的元件上，不會有色彩語義來定義一般陰影插補 (線性和一般的) 。

如果需要霧化轉譯，vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 著色器必須執行霧化。 不會在著色器以外完成任何霧化計算。 Vs 3 0 中沒有任何霧化暫存器 \_ \_ ，以及額外的語義 D3DDECLUSAGE 會 \_ 針對每個頂點計算的霧化 blend 因數 (霧化) 和 D3DDECLUSAGE \_ 深度 (以將深度值傳遞給圖元著色器，以計算已加入的霧化 blend 因數) 。

\_使用圖元著色器3.0 時，會忽略材質階段狀態 D3DTSS TEXCOORDINDEX。

已新增下列值來容納這些變更：


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a>浮點數和整數轉換

浮點數數學會以不同的精確度和範圍 (在管線的不同部分中的16位、24位和32位) 。 值大於進入管線之管線的動態範圍 (例如，將32位的 float 紋理對應取樣為 ps 2 0 中的24位浮點管線 \_ \_) 建立未定義的結果。 針對可預測的行為，您應該將這類值固定到動態範圍的最大值。

從浮點值到整數的轉換會在數個位置發生，例如：

-   遇到 [mova vs](mova---vs.md) 指令時。
-   在紋理定址期間。
-   當寫出至非浮點數轉譯目標時。

## <a name="specifying-full-or-partial-precision"></a>指定完整或部分有效位數

Ps \_ 3 \_ 0 和 ps \_ 2 x 兩者都 \_ 提供兩種精確度層級的支援：



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| ps \_ 3 \_ 0 | ps \_ 2 \_ 0 | 準確率         | 值                |
| x        |          | 完整              | fp32 或更高版本       |
| x        |          | 部分有效位數 | fp16 = s10e5           |
| x        | x        | 完整              | fp24 = s16e7 或更高版本 |
| x        | x        | 部分有效位數 | fp16 = s10e5           |



 

ps \_ 3 \_ 0 支援的精確度比 ps \_ 2 \_ 0 更高。 依預設，所有作業都會以完整的精確度層級進行。

部分精確度 (請參閱 [圖元著色器](dx9-graphics-reference-asm-ps-registers-modifiers.md) 暫存器的) 要求，方法是將 \_ pp 修飾詞新增至著色器程式碼 (前提是基礎實作為支援) 。 您一律可以自由地忽略修飾詞，並以完整的精確度執行受影響的作業。

\_Pp 修飾詞可以出現在兩個內容中：

-   在紋理座標宣告上，將部分有效位數材質座標傳遞給圖元著色器。 當材質將轉送色彩資料座標為圖元著色器時，可使用這種方式，在某些實執行中，部分精確度可能會比完整有效位數更快。
-   在要求使用部分有效位數的任何指示上，包括材質載入指示。 這表示可以執行實作為部分有效位數的指令，並儲存部分精確度結果。 如果沒有明確的修飾詞，就必須以完整的精確度來執行指令， (無論輸入運算元) 的精確度為何。

應用程式可能會刻意選擇以效能的精確度來取捨。 有幾種著色器輸入資料是部分精確度處理的自然候選：

-   色彩反覆運算器以部分精確度值妥善表示。
-   大部分格式的材質值都可以精確地以部分有效位數值表示， (從32位取樣的值、浮點數格式材質) 的明顯例外狀況。
-   常數可以依適當的著色器，以局部精確度標記法表示。

在所有這些情況下，開發人員都可以選擇指定部分精確度來處理資料，並知道不會遺失任何輸入資料精確度。 在某些情況下，如果輸入和最終輸出值沒有超過部分有效位數，則著色器可能需要以完整的精確度執行計算的內部步驟。

## <a name="software-vertex-and-pixel-shaders"></a>軟體頂點和圖元著色器

軟體實 (針對頂點著色器的執行時間和參考，以及第2版著色器) 的圖元著色器參考，且 \_ 會放寬某些驗證。 這適用于偵錯工具和原型設計用途。 應用程式會向執行時間/組合器指出，它需要使用組合器中的 sw 旗標放寬某些驗證 \_ (例如 vs \_ 2 \_ sw) 。 軟體著色器不會與硬體搭配運作。

vs \_ 2 \_ sw 是 vs 2 x 上限的放寬 \_ \_ ; 同樣地，ps \_ 2 \_ sw 是 ps 2 x 最大上限的放寬 \_ \_ 。 具體而言，下列驗證是寬鬆的：



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 著色器模型                               | 資源                             | 限制                                                                                                                             |
| vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw | 指令計數                   | 無限制                                                                                                                         |
| vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw | Float 常數暫存器             | 8192                                                                                                                              |
| vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw | 整數常數暫存器           | 2048                                                                                                                              |
| vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw | 布林常數暫存器           | 2048                                                                                                                              |
| ps \_ 2 \_ sw                                  | 相依-讀取深度                 | 無限制                                                                                                                         |
| vs \_ 2 \_ sw                                  | 流程式控制制指示與標籤 | 無限制                                                                                                                         |
| vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw | 迴圈開始/步驟/計數               | Rep 和迴圈指示的反復專案開始和反覆運算步驟大小為32位帶正負號的整數。 Count 最多可達 \_ INT/64。 |
| vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw | 埠限制                          | 所有註冊檔案的埠限制都是寬鬆的。                                                                                   |
| vs \_ 3 \_ sw                                  | Interpolators 數目              | vs 3 sw 中的16個輸出暫存器 \_ \_ 。                                                                                                 |
| ps \_ 3 \_ sw                                  | Interpolators 數目              | 14 (16-2) 適用于 ps 3 sw 的輸入暫存器 \_ \_ 。                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 