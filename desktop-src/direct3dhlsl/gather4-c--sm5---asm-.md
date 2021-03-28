---
title: 'gather4_c (sm5-asm) '
description: 與 gather4 相同，不同之處在于此 instrution 會在材質上執行比較，類似于範例 \_ c。
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990791"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (sm5-asm) 

與 [**gather4**](gather4--sm5---asm-.md)相同，不同之處在于此 instrution 會在材質上執行比較，類似于 [**範例 \_ c**](sample-c--sm4---asm-.md)。



| gather4 \_ c \[ \_ aoffimmi (u、v) \] dest \[ \] 、srcAddress \[ . swizzle \] 、srcResource. swizzle \[ \] 、srcSampler \[ 。R \] 、srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| 項目                                                                                                                                       | 描述                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/>                                                                            | \[在 \] 操作結果的位址中<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[在 \] 一組材質座標中。<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[在材質暫存器中 \] 。<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[在 \] 取樣器註冊中。<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[在 \] 已選取單一元件的註冊中，用於比較。<br/> |



 

## <a name="remarks"></a>備註

如需有關 *srcReferenceValue* 如何與每個提取的材質進行比較的說明，請參閱 [**範例 \_ c**](sample-c--sm4---asm-.md) 。 不同于 **範例 \_ c**， **gather4 \_ c** 會傳回每個比較結果，而不是篩選它們。

若為 TextureCube 角落，其中有三個真正的材質，而第四個必須合成，則必須在比較步驟之後進行合成。 這表示 syntesized 材質傳回的比較結果可以是0、0.33、0.66 或1。 某些實作為合成材質可能只會傳回0或1。 除了這份可能的結果清單之外，未指定合成材質的方法。

針對具有 float32 元件的格式，如果要提取的值是正規化的或 +-INF，比較作業就會使用此值。 在比較作業中使用 NaN 做為 NaN，但 NaN 的精確位標記法可能會變更。 Denorms 會排清到零進行比較。 針對 TextureCubes，遺漏的第四個材質的部分合成必須在角落進行，因此未變更合成材質的未變更的概念。

*Gather4 \_ c* 支援的格式與 *範例 \_ c* 所支援的格式相同。 這些都是單一元件格式，因此。 *SrcSampler* 上的 R，而非任意 swizzle。 未系結資源上的 **gather4 \_ c** 會傳回0。

使用此指示進行自訂陰影對應篩選。

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

 

 





