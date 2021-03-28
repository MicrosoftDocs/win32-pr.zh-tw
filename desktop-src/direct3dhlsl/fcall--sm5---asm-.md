---
title: 'fcall (sm5-asm) '
description: 介面函式呼叫。
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373891"
---
# <a name="fcall-sm5---asm"></a>fcall (sm5-asm) 

介面函式呼叫。



| fcall fp \# \[ arrayIndex \] \[ callSite\] |
|--------------------------------------|



 



| 項目                                                                                                           | 描述                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/>                                                  | \[在 \] 函數指標中。<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*<br/> | \[（ \] 選擇性）。 指定函式指標陣列中的位移。 如果 fp 未宣告為可索引，則此參數必須是常值不帶正負號的整數 \# 。 否則，arrayIndex 可能是來自著色器暫存器的表單常值基底 + 位移。 例如，fcall fp1 \[ r1. w + 0 \] \[ 0 \] 。<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*<br/>     | \[（ \] 選擇性）。 選取的函式資料表中不帶正負號的整數位移，選取了不常執行的函數主體 \# 。 <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>備註

*fp \#* \[ \] \[ arrayIndex \]解析為特定的函式表，從著色 *器的宣告 \#* 中所列的函式資料表選項，在著色器以外的 API 中選取。

\# *Fp \#* 和 *arrayIndex* 中的總和會選取函數資料表。 例如，如果介面宣告為 fp4 \[ 4 \] \[ 3 \] (陣列大小為 4) ，則下列 **fcall** 是相等的： fcall fp4 \[ 2 \] \[ 3 \] 和 fp5 \[ 1 \] \[ 3 \] ，因為 4 + 2 = 5 + 1。

### <a name="restrictions"></a>限制

-   如果 *arrayIndex* 使用動態索引，則如果 *arrayIndex* 分歧在連續的著色器調用（可能在密集建置中執行），則行為會是未定義的。 HLSL 編譯器會嘗試不允許這種情況。

    相鄰調用可能因為流量控制而處於非使用中狀態，因為它不會中斷密集建置執行。

-   如果 *fp \#*  +  *arrayIndex* 指定超出範圍的索引，則行為會是未定義的。
-   針對此處所述的未定義案例，這表示目前 D3D 裝置的行為變成未定義，包括裝置可能遺失的可能性。 不過，目前 D3D 裝置以外的記憶體不會以程式碼的形式存取或執行。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 不可以        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





