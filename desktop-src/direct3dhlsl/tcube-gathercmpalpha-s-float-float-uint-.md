---
title: TextureCube：： GatherCmpAlpha (S，float，float，uint) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較，以及磚對應狀態。 |TextureCube：： GatherCmpAlpha (S，float，float，uint) 函數
ms.assetid: 8DC43B02-0B3C-49F0-AA94-80894A1A54BD
keywords:
- GatherCmpAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 447328be61709dfe6cfdf0910f0ee468fa59e2b16095f1b59eb087434aedd822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506507"
---
# <a name="texturecubegathercmpalphasfloatfloatuint-function"></a>TextureCube：： GatherCmpAlpha (S，float，float，uint) 函數

針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較，以及磚對應狀態。

## <a name="syntax"></a>語法


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[GatherCmpAlpha 方法](texturecube-gathercmpalpha.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
