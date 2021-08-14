---
title: 'sampleinfo (sm 4.1-asm) '
description: 查詢指定著色器資源檢視或轉譯器中的樣本數。
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2227afbf7a08a0010efc2efb8fcf87bae85c8f5775e596d92b761b556f8bfb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510466"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (sm 4.1-asm) 

查詢指定著色器資源檢視或轉譯器中的樣本數。



| \[\_uint \] dest \[ . mask \] 、srcResource \[ . swizzle\] |
|---------------------------------------------------|



 



| 項目                                                                                                               | 描述                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                    | \[在 \] 操作結果的位址中。<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[在 \] 著色器資源中。<br/>                         |



 

## <a name="remarks"></a>備註

此指令會傳回指定資源或轉譯器的樣本數。 它只適用于可以使用 [**ld2dms**](ld2dms--sm4-1---asm-.md) 載入的資源，除非轉譯器已指定為 *srcResource*。 *srcResource* 可以是 \# (著色器資源檢視) 或轉譯器註冊的 t 註冊。

指令會計算向量 (SampleCount、0、0、0) 。

*SrcResource* 上的 swizzle 允許在將傳回的值寫入目的地之前，任意加以 swizzled。 除非使用 uint 修飾詞，否則傳回的值為浮點數， \_ 在這種情況下，傳回的值為整數。 如果沒有任何資源系結至指定的位置，則會傳回0。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





