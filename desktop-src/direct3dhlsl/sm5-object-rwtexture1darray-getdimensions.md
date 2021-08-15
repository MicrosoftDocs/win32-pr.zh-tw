---
title: RWTexture1DArray：： GetDimensions 函數
description: 傳回資源的維度。 |RWTexture1DArray：： GetDimensions 函數
ms.assetid: 64f2757e-c03c-4f72-b081-1c57656d6e95
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a522fe31a62619134e86b2ed98da54570d693d1360ede1a8c0d41d28975b367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986018"
---
# <a name="rwtexture1darraygetdimensions-function"></a>RWTexture1DArray：： GetDimensions 函數

傳回資源的維度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Elements
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*寬度* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源寬度，以材質。

</dd> <dt>

*元素* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

陣列中的項目數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

這是此方法的多載版本清單。


```
void GetDimensions (out UINT Width,
  out UINT Elements);

void GetDimensions(out float Width,
  out UINT Elements);
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
