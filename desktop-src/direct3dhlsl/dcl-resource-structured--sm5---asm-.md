---
title: 'dcl_resource 結構化 (sm5-asm) '
description: '宣告著色器資源輸入，並將其指派給資源的 t-a 預留位置註冊。 |dcl_resource 結構化 (sm5-asm) '
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195925"
---
# <a name="dcl_resource-structured-sm5---asm"></a>dcl \_ 資源結構化 (sm5-asm) 

宣告著色器資源輸入，並將其指派給 \# 資源的 t a 預留位置暫存器。



| dcl \_ 資源 \_ 結構化 DstSRV，structByteStride |
|----------------------------------------------------|



 



| 項目                                                                                                                                   | 描述                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[在宣告 \] \# 為參考之結構化緩衝區 ShaderResourceView 的 t 暫存器中，具有指定的 stride 必須系結至 API 的 SRV \# 位置。 <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[以 \] 位元組為單位，指定要宣告的緩衝區中的結構大小（以位元組為單位）。 這個值必須大於零。<br/>                                   |



 

## <a name="remarks"></a>備註

結構的內容沒有類型;在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。

參考結構化 t 的指示 \# 會採用2d 位址，其中第一個元件挑選 \[ 結構 \] ，而第二個元件則挑選 \[ 結構內的位移，32位的倍數 \] 。

cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此指令。

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

 

 





