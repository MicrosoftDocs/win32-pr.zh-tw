---
title: 'dcl_tgsm_raw (sm5-asm) '
description: 宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679176"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>dcl \_ tgsm \_ 原始 (sm5-asm) 

宣告可供計算著色器執行緒群組使用之共用記憶體空間區域的參考。



| dcl \_ tgsm \_ 原始 g \# ，byteCount |
|-------------------------------|



 



| 項目                                                                                                       | 描述                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                 | \[在不具 \] 類型的共用記憶體的大小 *byteCount* 的參考中。 <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[in \] 必須是4的倍數。 <br/>                                             |



 

## <a name="remarks"></a>備註

所有 g 的總儲存空間 \# 必須 <= 每個執行緒群組可用的共用記憶體數量（32kB）。

在極端情況下，您可以宣告 8192 total g \# s，每個都有4個 *byteCount* 。

在相反的極端情況下，您可以宣告 \# *byteCount* 為32768的單一 g。

> [!Note]  
> cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援 [ \_ tgsm \_ 結構化](dcl-tgsm-structured--sm5---asm-.md)，但不 **支援 \_ tgsm \_ 原始** 的 dcl。

 

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





