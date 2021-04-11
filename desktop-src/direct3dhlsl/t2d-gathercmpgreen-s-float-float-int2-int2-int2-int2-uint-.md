---
title: Texture2D：： GatherCmpGreen (S、float、float、int2、int2、int2、int2、uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較，以及磚對應狀態。 |Texture2D：： GatherCmpGreen (S、float、float、int2、int2、int2、int2、uint) 函數
ms.assetid: E7EB3D17-3110-4167-B255-C451BA4EFB27
keywords:
- GatherCmpGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b490fd47bd9346c4f514867de63df7a4d090e5b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196034"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2uint-function"></a>Texture2D：： GatherCmpGreen (S、float、float、int2、int2、int2、int2、uint) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較，以及磚對應狀態。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的 S\]
</dt> <dd>

類型： **SamplerState**

以零為基底的取樣器索引。

</dd> <dt>

*位置* \[在\]
</dt> <dd>

類型： **float**

此範例會協調 (u，v) 。

</dd> <dt>

*CompareValue* \[在\]
</dt> <dd>

類型： **float**

要針對每個取樣值進行比較的值。

</dd> <dt>

*Offset1* \[在\]
</dt> <dd>

類型： **int2**

第一個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*Offset2* \[在\]
</dt> <dd>

類型： **int2**

第二個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*Offset3* \[在\]
</dt> <dd>

類型： **int2**

第三個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*Offset4* \[在\]
</dt> <dd>

類型： **int2**

第四個位移元件會在取樣之前套用至材質座標。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

類型： **uint**

作業的狀態。 您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。 如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。 如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **TemplateType**

四個元件的值，其類型與範本類型相同。

## <a name="remarks"></a>備註

紋理範例可用於雙線性插補。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherCmpGreen 方法](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 
