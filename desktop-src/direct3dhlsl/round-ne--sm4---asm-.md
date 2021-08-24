---
title: 'round_ne (sm4-asm) '
description: '浮點數舍入整數浮點數。 |round_ne (sm4-asm) '
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe7088d9a6b577366fdaf169e21075188597ad4b761bb6fd3c555c809e91c41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853658"
---
# <a name="round_ne-sm4---asm"></a>四捨五入 \_ (sm4-asm) 

浮點數舍入整數浮點數。



| round \_ ne \[ \_ sat \] dest \[ \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在作業 \] 的元件中。<br/>             |



 

## <a name="remarks"></a>備註

此指令會在 *src0* 中執行以元件為依據的浮點舍入值，並將整數浮點值寫入至 *目的地*。 **四捨五入 \_** 會四捨五入到最接近的偶數。

下表顯示使用各種不同的數位類別來執行指令時所取得的結果。

F 表示有限實數。



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F** | **+ inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **目標** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

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

 

 





