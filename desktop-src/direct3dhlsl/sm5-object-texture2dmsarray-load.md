---
title: Texture2DMSArray：： Load (int，int) 函數
description: 取得一個值。 |Texture2DMSArray：： Load (int，int) 函數
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Load function HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945993"
---
# <a name="texture2dmsarrayloadintint-function"></a>Texture2DMSArray：： Load (int，int) 函數

取得一個值。

## <a name="syntax"></a>語法

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*coord* \[在\]
</dt> <dd>

類型： **int3**

輸入位置。

</dd> <dt>

*sampleindex* \[在\]
</dt> <dd>

類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**

範例索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **T**

一個值，其類型符合紋理範本類型。

## <a name="remarks"></a>備註

這是此方法的多載版本清單。


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](texture2dmsarray-load.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
