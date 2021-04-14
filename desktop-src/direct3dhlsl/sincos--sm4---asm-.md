---
title: 'sincos (sm4-asm) '
description: 元件取向的 sin (theta) 和 cos (弧度的 theta) 。
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990719"
---
# <a name="sincos-sm4---asm"></a>sincos (sm4-asm) 

元件取向的 sin (theta) 和 cos (弧度的 theta) 。



| sincos \[ \_ sat \] destSIN \[ mask \] 、destCOS \[ mask \] 、 \[ - \] src0 \[ \_ abs \] \[ . swizzle\] |
|------------------------------------------------------------------------------------|



 



| 項目                                                                                               | 描述                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[在 \] sin (*src0*) 的位址中，每個元件都會計算。<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[在 \] cos (*src0*) 的位址中，每個元件都會計算。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[在 \] 要計算 sin 和 cos 的元件中。<br/>    |



 

## <a name="remarks"></a>備註

如果不需要結果，您可以將 *destSIN* 和 *DESTCOS* 指定為 Null，而不是指定註冊。

Theta 值可以是任何 IEEE 32 位浮點值。

從-100 \* pi 到 + 100 Pi 的間隔中，最大的絕對錯誤為 0.0008 \* 。

下表顯示使用各種不同的數位類別來執行指令時所取得的結果。

F 表示有限實數。



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **src**     | **-inf** | **-F**       | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**       | **+ inf** | **NaN** |
| **destSIN** | NaN      | \[-1 到 + 1\] | -0          | -0     | +0     | +0          | \[-1 到 + 1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[-1 到 + 1\] | +1          | +1     | +1     | +1          | \[-1 到 + 1\] | NaN      | NaN     |



 

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





