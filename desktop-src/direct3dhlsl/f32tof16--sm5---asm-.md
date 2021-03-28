---
title: 'f32tof16 (sm5-asm) '
description: 'Float16 至 float32 轉換的元件。 |f32tof16 (sm5-asm) '
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974397"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (sm5-asm) 

Float16 至 float32 轉換的元件。



| f32tof16 dest \[ . mask \] ， \[ - \] src \[ . swizzle\] |
|----------------------------------------------|



 



| 項目                                                            | 描述                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] float16 結果的位址中。<br/> |
| <span id="src"></span><span id="SRC"></span>*Src*<br/>    | \[在 \] 要轉換的 float32 值中。<br/>  |



 

## <a name="remarks"></a>備註

此指令會執行將 float32 值轉換為 float16 值結果（放置於 LSB 16 位）的元件。

此指示遵循 D3D 規則來進行浮點數轉換。

針對著色器驅動的資料壓縮，請使用此指令。

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

 

 





