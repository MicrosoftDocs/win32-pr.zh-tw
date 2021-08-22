---
title: 'f16tof32 (sm5-asm) '
description: 'Float16 至 float32 轉換的元件。 |f16tof32 (sm5-asm) '
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc4456737d5ddaaed351ae2a1cc76418c33af9c498e725099e1912d8fabe7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562649"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (sm5-asm) 

Float16 至 float32 轉換的元件。



| f16tof32 dest \[ . mask \] ， \[ - \] src \[ . swizzle\] |
|----------------------------------------------|



 



| 項目                                                            | 描述                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] float32 結果的位址中。<br/> |
| <span id="src"></span><span id="SRC"></span>*Src*<br/>    | \[\]要轉換的 float16 值。<br/>      |



 

## <a name="remarks"></a>備註

這項作業會執行從 LSB 位到 float32 結果之 float16 值的元件轉換。

這種作業遵循浮點數轉換的 D3D 規則。

針對著色器驅動的資料解壓縮，請使用此指令。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
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

 

 





