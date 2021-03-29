---
title: TextureCubeArray 物件
description: TextureCubeArray 類型 (存在於著色器模型 4) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件也支援這些方法。
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- TextureCubeArray 物件 HLSL
- TextureCubeArray 物件 HLSL，描述
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "104991846"
---
# <a name="texturecubearray-object"></a>TextureCubeArray 物件

**TextureCubeArray** 類型 ([存在於著色器模型 4](dx-graphics-hlsl-to-type.md)) 加上資源變數中。 除了著色器模型4中的方法之外，此材質物件也支援這些方法。

-   [方法](#methods)

### <a name="methods"></a>方法

**TextureCubeArray** 物件有這些方法。



| 方法                                                           | 描述                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**收集**](texturecubearray-gather.md)                         | 傳回要在雙線性篩選作業中使用的四個材質值。<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | 傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | 傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | 針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | 針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | 針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | 傳回雙線性篩選作業中所使用之四個材質值的綠色元件。<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | 傳回四個材質值的紅色元件，這些值會在雙線性篩選作業中使用。<br/>                                          |
| [**範例**](texturecubearray-sample.md)                         | 範例材質。<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | 將偏差值套用至 mipmap 層級之後，將材質取樣。<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | 使用比較值來拒絕範例，以取樣材質。<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) |  (只) 使用比較值來拒絕範例的材質的材質。<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | 使用漸層來取樣材質，以影響範例位置的計算方式。<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | 針對指定的 mipmap 層級進行紋理取樣。<br/>                                                                                                    |



 

## <a name="remarks"></a>備註

### <a name="minimum-shader-model"></a>最小著色器模型

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

 

 





