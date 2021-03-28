---
title: 'dcl_output_sgv (sm4-asm) '
description: 'dcl \_ 輸出 \_ sgv (sm4-asm) '
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373911"
---
# <a name="dcl_output_sgv-sm4---asm"></a>dcl \_ 輸出 \_ sgv (sm4-asm) 

宣告包含 [系統值](dx-graphics-hlsl-semantics.md) 參數的輸出暫存器。



| \_ \_ sgv 上的 dcl 輸出：*\[ mask \]*、 *systemValue* |
|-----------------------------------------------|



 



| 項目                                                                                                                               | 描述                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[在 \] 輸出資料註冊中; *N* 是表示註冊編號的整數。<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[mask\]*<br/>                                                         | \[（ \] 選擇性）。 元件遮罩 ( xyzw) ，可指定要使用的註冊元件。<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*<br/> | \[在 \] 系統值名稱中是字串 (請參閱 [系統值語義](dx-graphics-hlsl-semantics.md)) ，但不含 "SV \_ " 前置詞。<br/> |



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_output_sgv o4.x, primitiveID
```



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

 

 





