---
title: 'ddiv (sm5-asm) '
description: 計算元件的雙精確度除法。
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999155"
---
# <a name="ddiv-sm5---asm"></a>ddiv (sm5-asm) 

計算元件的雙精確度除法。



| ddiv \[ \_ sat \] dest \[ . mask \] ， \[ - \] src0 \[ \_ abs \] \[ . swizzle \] \[ - \] src1 \[ \_ abs \] \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在作業的 \] 結果中。 結果值必須正確到 0.5 ULP。 <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[被 \] 除數。<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[\]除數。<br/>                                                                |



 

## <a name="remarks"></a>備註

每當使用除法運算子搭配雙精度浮點數時，HLSL 編譯器就會發出 DDIV 指令。 此指令的精確度將必須為 0.5 ULP。

使用此指令的著色器會標記為著色器旗標，除非符合下列所有條件，否則會導致無法系結。

-   系統支援 DirectX 11.1。
-   系統包含 WDDM 1.2 驅動程式。
-   驅動程式會透過 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項，向此指令報告支援。ExtendedDoublesShaderInstructions** 設定為 **TRUE**。

下表顯示使用各種不同的數位類別來執行指令時所 btained 的結果，前提是不會發生溢位或下溢。

在此表中，F 表示有限的實數。



| **src0 src1->** | **-inf** | **-F** | **-1。0** | **-0** | **+0** | **+ 1。0** | **+ F** | **+ inf** | **NaN** |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | +F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+ F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | +F     | +0       | NaN     |
| **+ inf**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 否        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





