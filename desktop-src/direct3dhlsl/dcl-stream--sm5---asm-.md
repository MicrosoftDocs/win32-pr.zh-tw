---
title: 'dcl_stream (sm5-asm) '
description: 宣告幾何著色器輸出資料流程。
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373906"
---
# <a name="dcl_stream-sm5---asm"></a>dcl \_ 資料流程 (sm5-asm) 

宣告幾何著色器輸出資料流程。



| dcl \_ 資料流程 m\# |
|-----------------|



 



| 項目                                                       | 描述                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*m\#*<br/> | \[在 \] Stream 0 中 (m0。m3) 。<br/> |



 

## <a name="remarks"></a>備註

給定的資料流程只能宣告一次。

如果未宣告任何資料流程，則會假設資料流程0有輸出和輸出拓撲宣告。

第一個 **dcl \_ 資料流程** 不能出現在任何 **dcl \_ 輸出** 或 **dcl \_ outputTopology** 語句之後。

任何 **dcl \_ 資料流程** m 語句之後的任何 **dcl \_ 輸出** 或 **dcl \_ outputToplogy** 語句都會 \# 定義資料流程 m 的輸出 \# 。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





