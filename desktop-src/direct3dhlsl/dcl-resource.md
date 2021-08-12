---
title: 'dcl_resource (sm4-asm) '
description: 'dcl \_ 資源 (sm4-asm) '
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f23fac2f6671584c69ecad045d13e885e86fb260164675da3bc51f7edf847f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515633"
---
# <a name="dcl_resource-sm4---asm"></a>dcl \_ 資源 (sm4-asm) 

宣告非多重取樣的著色器輸入資源。



| dcl \_ 資源 *tN*、 *resourceType*、 *returnType (s)* |
|-----------------------------------------------------|



 

宣告多重取樣著色器輸入資源。



| dcl \_ 資源 *tN*、 *resourceType \[ 大小 \] NN*、 *returnType (s)* |
|---------------------------------------------------------------|



 



| Item                                                                                                                                                     | 描述                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[在材質暫存器中 \] ，其中 *N* 是表示註冊編號的整數。<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*<br/>                                   | \[在 \] [ [材質物件](dx-graphics-hlsl-to-type.md) ] 頁面中所列的任何物件類型中。<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ 大小 \] NN*<br/> | \[在 \] Texture2D 或 Texture2DArray 物件類型中 (查看 [材質物件](dx-graphics-hlsl-to-type.md) 頁面) ; *size* 是選擇性的整數，表示陣列中的元素數目; *NN* 是表示 multisamples 數目的整數。<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*<br/>                               | \[在 \] 每個元件的傳回型別中，這是下列其中一項： UNORM、SNORM、聖、UINT 或 FLOAT。 如果所有元件的類型都相同，則傳回型別的數目可以是 1 () ，但最多可以有四個。<br/>                                          |



 

使用 [load](dx-graphics-hlsl-to-load.md)在 HLSL 中存取資源;您也可以使用任何 HLSL [材質物件](dx-graphics-hlsl-to-type.md) 範例方法來存取非多重取樣材質。

如果資源系結至著色器階段，則會根據傳回類型來驗證資源格式。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_resource t3, buffer, UNORM
```



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

 

 





