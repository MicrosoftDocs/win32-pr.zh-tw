---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022586"
---
# <a name="texture1darray"></a>Texture1DArray

Texture1DArray 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件還支援下列方法。



| 方法                                                                       | 描述                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | 取得資源維度。                                                              |
| [**載入**](texture1darray-load.md)                                          | 讀取紋理資料。                                                                        |
| [**Mips。運算元\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | 取得唯讀的資源變數。                                                        |
| [**運算子\[\]**](sm5-object-texture1darray-operatorindex.md)              | 取得唯讀的資源變數。                                                        |
| [**範例**](texture1darray-sample.md)                                      | 範例材質。                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | 將偏差值套用至 mipmap 層級之後，將材質取樣。                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | 使用比較值來拒絕範例，以取樣材質。                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              |  (只) 使用比較值來拒絕範例的材質的材質。       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | 使用漸層來取樣材質，以影響範例位置的計算方式。 |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | 針對指定的 mipmap 層級進行紋理取樣。                                           |



 

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

 

 




