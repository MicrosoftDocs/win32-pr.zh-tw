---
title: 'dcl_immediateConstantBuffer (sm4-asm) '
description: 'dcl \_ immediateConstantBuffer (sm4-asm) '
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313767"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a>dcl \_ immediateConstantBuffer (sm4-asm) 

宣告著色器的立即常數緩衝區。



| \_ *(s)* 的 dcl immediateConstantBuffer 值 |
|-----------------------------------------|



 

<dl> <dt>

<span id="value_s_"></span><span id="VALUE_S_"></span>*值 (s)*
</dt> <dd>

\[\]緩衝區中必須包含至少一個值，但不能超過4096的值。

</dd> </dl>

### <a name="remarks"></a>備註

著色器允許一個立即常數緩衝區。 直接常數緩衝區的存取方式就像是具有動態索引的常數緩衝區。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

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

 

 




