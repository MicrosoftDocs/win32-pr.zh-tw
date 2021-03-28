---
title: TextureCube：：搜集 (S、float、uint) 函數
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |TextureCube：：搜集 (S、float、uint) 函數
ms.assetid: 23FA8135-ECF0-4CAE-9A1C-B05DA3676453
keywords:
- 收集函數 HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9710343ff9b09e4425bc133db6dab4d118d807e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973964"
---
# <a name="texturecubegathersfloatuint-function"></a>TextureCube：：搜集 (S、float、uint) 函數

傳回要在雙線性篩選作業中使用的四個材質值。

## <a name="syntax"></a>語法


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
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

[收集方法](texturecube-gather.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
