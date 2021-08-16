---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 382ac1e436eff4108a2179aeefd4395fbc52c7af304bb719cbadf87a3c1f3d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724869"
---
# <a name="texture1d"></a>Texture1D

一維紋理類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件還支援下列方法。



| 方法                                                                  | 描述                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | 取得資源維度。                                                              |
| [**載入**](texture1d-load.md)                                          | 讀取紋理資料。                                                                        |
| [**運算子\[\]**](sm5-object-texture1d-operatorindex.md)              | 取得唯讀的資源變數。                                                        |
| [**Mips。運算元\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | 取得唯讀的資源變數。                                                        |
| [**範例**](texture1d-sample.md)                                      | 範例材質。                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | 將偏差值套用至 mipmap 層級之後，將材質取樣。                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | 使用比較值來拒絕範例，以取樣材質。                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              |  (只) 使用比較值來拒絕範例的材質的材質。       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | 使用漸層來取樣材質，以影響範例位置的計算方式。 |
| [**SampleLevel**](texture1d-samplelevel.md)                            | 針對指定的 mipmap 層級進行紋理取樣。                                           |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




