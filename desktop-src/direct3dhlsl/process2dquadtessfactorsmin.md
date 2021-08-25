---
title: Process2DQuadTessFactorsMin 函式
description: 產生四個修補程式的已更正鑲嵌因數。 |Process2DQuadTessFactorsMin 函式
ms.assetid: 45adf78a-9386-4460-97df-59d7739a1eee
keywords:
- Process2DQuadTessFactorsMin 函式 HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 77f62ff1b55b9c0c36a70bd64f2b0d5ad95be747d5fd11cae33e82eb896d21d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067898"
---
# <a name="process2dquadtessfactorsmin-function"></a>Process2DQuadTessFactorsMin 函式

產生四個修補程式的已更正鑲嵌因數。

## <a name="syntax"></a>語法

``` syntax
void Process2DQuadTessFactorsMin(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*RawEdgeFactors* \[在\]
</dt> <dd>

類型： **float4**

傳遞至鑲嵌階段的邊緣鑲嵌因數。

</dd> <dt>

*InsideScale* \[在\]
</dt> <dd>

類型： **float2**

調整因數會套用至鑲嵌式階段所計算的 UV 鑲嵌因數。 InsideScale 的允許範圍是0.0 到1.0。

</dd> <dt>

*RoundedEdgeTessFactors* \[擴展\]
</dt> <dd>

類型： **float4**

鑲嵌階段所計算的圓角邊緣鑲嵌因數。

</dd> <dt>

*RoundedInsideTessFactors* \[擴展\]
</dt> <dd>

類型： **float2**

鑲嵌階段針對內部邊緣計算的圓角鑲嵌因數。

</dd> <dt>

*UnroundedInsideTessFactors* \[擴展\]
</dt> <dd>

類型： **float2**

鑲嵌階段針對內部邊緣所計算的鑲嵌因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

產生四個修補程式的已更正鑲嵌因數，以最小的邊緣鑲嵌因數來計算內鑲嵌因數。 您和 V 鑲嵌式因素的計算方式是使用網域的最小邊緣來個別計算，然後以 InsideScale 進行調整。 結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactors 參數可使用 unrounded 結果。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




