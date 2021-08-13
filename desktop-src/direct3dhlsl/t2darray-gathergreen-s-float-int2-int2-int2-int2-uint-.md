---
title: Texture2DArray：： GatherGreen (S、float、int2、int2、int2、int2、uint) 函數
description: 傳回四個材質值的綠色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。 |Texture2DArray：： GatherGreen (S、float、int2、int2、int2、int2、uint) 函數
ms.assetid: 994320C6-3BE5-40F9-9B9F-1913134DA71A
keywords:
- GatherGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bdadf3f4260c39581d77d8334bf418494cf57596c03841a785756fbff797784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788474"
---
# <a name="texture2darraygathergreensfloatint2int2int2int2uint-function"></a>Texture2DArray：： GatherGreen (S、float、int2、int2、int2、int2、uint) 函數

傳回四個材質值的綠色元件，這些值會用於雙線性篩選作業，以及磚對應狀態。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
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



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[GatherGreen 方法](texture2darray-gathergreen.md)
</dt> </dl>

 

 
