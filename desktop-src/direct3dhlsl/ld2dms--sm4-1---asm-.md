---
title: 'ld2dms (sm 4.1-asm) '
description: 從二維多範例紋理讀取個別樣本。
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092457"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (sm 4.1-asm) 

從二維多範例紋理讀取個別樣本。



| ld2dms \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource、swizzle \[ \] 、sampleIndex (純量運算元)  |
|------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在作業的 \] 結果位址中。 <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[在 \] 執行範例所需的材質座標中。<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在材質暫存器中 \] (t) 必須已經宣告， \# 以識別要從中提取的材質或緩衝區<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[在 \] Idendifies 中，從 *srcResource* 讀取的範例。<br/>                                                       |



 

## <a name="remarks"></a>備註

此指令是 [範例](sample--sm4---asm-.md) 指令的簡化替代方法。 它會從指定的材質中提取資料，而不需要任何篩選 (例如，使用提供的整數 *srcAddress* 和 *sampleIndex* 點取樣) 。

*srcAddress* 提供以不帶正負號整數形式執行範例所需的材質座標集合。 如果 *srcAddress* 超出 \[ 維度-1) 的範圍 0 ... (\# 材質 \] ， **ld2dms** 一律會在以資源格式呈現的所有元件中傳回0，並預設 (0、0、0、1.0 f/0x00000001) 用於遺漏的元件。

*sampleIndex* 不必是常值。 不需要在材質資源上指定多樣本計數，它可以搭配深度或樣板視圖使用。

希望能更靈活地控制超出範圍的位址行為的應用程式應該改用 **範例** 指令，因為它會接受定義為取樣器狀態的位址包裝/鏡像/夾具/框線行為。

Texture2Ds 會忽略 *srcAddress. b* (swizzle 後) 。 如果值超出可用陣列索引的範圍 \[ 0 ... (陣列大小-1) \] ，則 **ld2dms** 一律會在以資源格式呈現的所有元件中傳回0，並預設 (0、0、0、1.0 f/0x00000001) 用於遺漏的元件。

若是 Texture2D 陣列， *srcAddress. b* (swizzle 後) 會提供陣列索引。 Oherwise 與 Texture2D 具有相同的行為。

*srcAddress* swizzle 後 (的) 一律會被忽略。 HLSL 編譯器永遠不會輸出任何結果。

*srcResource* 是 (t) 的材質暫存器 \# ，必須宣告為 (22.3.11) ，以識別要從中提取的材質。

從沒有任何系結的 t 進行提取 \# ，會針對所有元件傳回0。

### <a name="address-offset"></a>位址位移

選擇性的 \[ \_ aoffimmi (u，v，w) \] 尾碼 (以立即整數的位址位移) 表示 **ld2dms** 的材質座標是以一組提供的立即材質空間整數常數值來位移。 常值是一組4位2的補數數位，具有整數範圍 \[ -8，7 \] 。

位移會新增至材質座標的材質空間中。

Texture1D/2D 陣列的陣列軸並不會套用位址位移。

*\_ Aoffimmi v （w）* 會忽略 Texture1Ds 的元件。

Texture2Ds 會忽略 *\_ aoffimmi w* 元件。

因為 **ld2dms** 的材質座標是不帶正負號的整數，所以如果位移導致位址小於零，則會將它換成較大的位址，並產生超出範圍的存取權，例如 **ld** 會在以資源格式呈現的所有元件中傳回0，而遺漏元件的預設值 (0、0、0、1.0 f/0x00000001) 。

### <a name="sample-number"></a>範例編號

**ld2dms** 可用於任何資源。 **ld2dms** 的運作方式與 **ld** 相同（除了 2d multsample 資源），方法是使用額外的 (0 為基礎的) *sampleIndex* 運算元來識別要從資源中讀取的範例。

指定 *sampleIndex* 超過資源中樣本數目的結果是未定義的，但無法傳回裝置內容之位址空間以外的資料。

### <a name="return-type-control"></a>傳回型別控制項

**Ld2dms** 所傳回的資料格式是以與 **範例** 指令所述的相同方式來決定。 它是以系結至 *srcResource* 參數 (t) 的格式為基礎 \# 。

如同 **範例** 指令一樣， **ld2dms** 的傳回值為4向量，以及格式不存在之元件的格式特定預設值。 *SrcResource* 上的 swizzle 會決定如何 swizzle 從材質載入傳回的4個元件結果。在 *目的地* 上的遮罩可判斷在 *dest* 中的哪些元件已更新。

當 **ld2dms** 將32位的 float 值讀入32位的暫存器時，不會改變位;也就是說，denormal 值仍維持 denormal。 這與 **範例** 指令不同。

### <a name="miscellaneous-details"></a>其他詳細資料

因為沒有與此指令相關聯的篩選，所以不適用」 LOD 偏差之類的概念。 因此，沒有任何 *取樣器 \# s* 參數。

### <a name="restrictions"></a>限制

-   *srcResource* 必須是 t \# 註冊，而不是 TextureCube、Texture1D 或 Texture1DArray。 *srcResource* 不能是無法系結至 t 註冊的 ConstantBuffer \# 。
-   不允許 *srcResource* 的相對定址。
-   *srcAddress* 和 *sampleIndex* 必須是 temp (r \# /x \#) 、常數 (cb \#) 或輸入 (v \#) register。
-   *dest* 必須是 temp (r \# /x \#) 或 output (o \* \#) register。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





