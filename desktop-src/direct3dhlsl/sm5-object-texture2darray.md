---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104973872"
---
# <a name="texture2darray"></a>Texture2DArray

Texture2DArray 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件還支援下列方法。



| 方法                                                                      | 描述                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**收集**](texture2darray-gather.md)                                      | 傳回要在雙線性篩選作業中使用的四個材質值。                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | 傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | 傳回雙線性篩選作業中所使用之四個材質值的綠色元件。                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | 傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | 傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | 針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。 |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | 針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | 針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。 |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | 取得資源維度。                                                                                                                       |
| [**載入**](texture2darray-load.md)                                          | 讀取紋理資料。                                                                                                                                 |
| [**Mips。運算元\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | 取得唯讀的資源變數。                                                                                                                 |
| [**運算子\[\]**](sm5-object-texture2darray-operatorindex.md)              | 取得唯讀的資源變數。                                                                                                                 |
| [**範例**](texture2darray-sample.md)                                      | 範例材質。                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | 將偏差值套用至 mipmap 層級之後，將材質取樣。                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | 使用比較值來拒絕範例，以取樣材質。                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              |  (只) 使用比較值來拒絕範例的材質的材質。                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | 使用漸層來取樣材質，以影響範例位置的計算方式。                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | 針對指定的 mipmap 層級進行紋理取樣。                                                                                                    |



 

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

 

 




