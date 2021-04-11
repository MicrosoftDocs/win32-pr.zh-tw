---
title: 'dcl_resource 原始 (sm5-asm) '
description: '宣告著色器資源輸入，並將其指派給資源的 t-a 預留位置註冊。 |dcl_resource 原始 (sm5-asm) '
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195988"
---
# <a name="dcl_resource-raw-sm5---asm"></a>dcl \_ 資源原始 (sm5-asm) 

宣告著色器資源輸入，並將其指派給 \# 資源的 t a 預留位置暫存器。



| dcl \_ 資源 \_ 原始 dstSRV |
|---------------------------|



 



| 項目                                                                                           | 描述                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[在宣告 \] \# 為原始緩衝區之 ShaderResourceView 參考的 t 註冊程式中。<br/> |



 

## <a name="remarks"></a>備註

結構的內容沒有類型;在記憶體上執行的作業可能會隱含地將資料解讀為具有類型。

參考原始 t 的指示 \# 會採用1d 位址，這是一個不帶正負號的32位值，可指定緩衝區中32位對齊位置的位元組位移。 位址必須是 4 (個位元組) 的倍數。

系結至 t \# 但宣告為 raw 的視圖必須在其建立時指定 raw; 否則，從著色器存取時的行為未定義。

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

 

 





