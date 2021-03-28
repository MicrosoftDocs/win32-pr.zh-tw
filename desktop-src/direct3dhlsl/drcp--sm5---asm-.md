---
title: 'drcp (sm5-asm) '
description: 將元件雙向的雙精確度計算為反向。
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313694"
---
# <a name="drcp-sm5---asm"></a>drcp (sm5-asm) 

將元件雙向的雙精確度計算為反向。



| rcp \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 結果的位址中<br/> *目的地*  = **1.0**  / *src0*。 結果值必須正確到 1.0 ULP<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]要採用的數位。<br/>                                                                         |



 

## <a name="remarks"></a>備註

只有在使用 double 作為引數時，才會透過 rcp () 內建明確呼叫 DRCP 指令來發出 HLSL 編譯器。 此指令的精確度必須為 1.0 ULP。

使用此指令的著色器會標記為著色器旗標，除非符合下列所有條件，否則會導致無法系結。

-   系統支援 DirectX 11.1。
-   系統包含 WDDM 1.2 驅動程式。
-   驅動程式會透過 **D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項，向此指令報告支援。ExtendedDoublesShaderInstructions** 設定為 **TRUE**。

下表顯示使用各種不同的數位類別來執行指令時所取得的結果，前提是不會發生溢位或下溢。

在此表中，F 表示有限的實數。



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **Src**->  | **-inf** | **-F** | **-0** | **+0** | **+ F** | **+ inf** | **NaN** |
| **目標**-> | -0       | -F     | -inf   | +inf   | +F     | +0       | NaN     |



 

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>最小著色器模型

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

 

 





