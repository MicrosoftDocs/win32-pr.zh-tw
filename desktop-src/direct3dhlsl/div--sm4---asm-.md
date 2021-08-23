---
title: 'div (sm4-asm) '
description: 元件的細分。
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1df4e40032a2eaa2c4ef89ca5d1e227b4ebc35bbc8b13d7868eda5ea7a5b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625768"
---
# <a name="div-sm4---asm"></a>div (sm4-asm) 

元件的細分。



| div \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[被 \] 除數。<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[\]除數。<br/>                 |



 

## <a name="remarks"></a>備註

下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。

您應該記下兩個允許的除法除法： a/b 和 \* (1/b) 。

其中一個結果是，下表有一些例外狀況，適用于大型分母值 (大於 8.5070592 e + 37) ，其中 1/分母為 denorm。 因為實值可能會以 \* (1/b) （而不是直接）來執行，而且 1/ \[ 大值是可能會排清的 \] denorm，所以資料表中的某些案例會產生不同的結果。 例如， (+/-) INF/ (+/-) \[ 值 > 8.5070592 e + 37 \] 可能在某些實作為上產生 NaN，但在其他執行上 (+/-) INF

在此表中，F 表示有限的實數。



| **src0 src1->** | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**     | **+ inf** | **南** |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **-inf**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F 或 +-0 | +inf     | NaN     |
| **-denorm**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ denorm**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ F**              | -inf     | +-F 或 +-0 | src0        | src0   | src0   | src0        | +F         | +inf     | NaN     |
| **+ inf**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

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
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





