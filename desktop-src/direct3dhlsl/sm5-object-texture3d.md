---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022356"
---
# <a name="texture3d"></a>Texture3D

Texture3D 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件還支援下列方法。



| 方法                                                                  | 描述                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | 取得資源維度。                                                              |
| [**載入**](texture3d-load.md)                                          | 讀取紋理資料。                                                                        |
| [**Mips。運算元\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | 取得唯讀的資源變數。                                                        |
| [**運算子\[\]**](sm5-object-texture3d-operatorindex.md)              | 取得唯讀的資源變數。                                                        |
| [**範例**](texture3d-sample.md)                                      | 範例材質。                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | 將偏差值套用至 mipmap 層級之後，將材質取樣。                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | 使用漸層來取樣材質，以影響範例位置的計算方式。 |
| [**SampleLevel**](texture3d-samplelevel.md)                            | 針對指定的 mipmap 層級進行紋理取樣。                                           |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




