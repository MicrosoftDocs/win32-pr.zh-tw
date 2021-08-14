---
title: Texture2DMS：： Load (int，int) 函數
description: 取得一個值。 |Texture2DMS：： Load (int，int) 函數
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Load 函數 DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0997a1bd30b4912864674015057fcafec227d90ad05b16b88fd3f05b671f155c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285726"
---
# <a name="texture2dmsloadintint-function"></a>Texture2DMS：： Load (int，int) 函數

取得一個值。

## <a name="syntax"></a>語法

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*coord* \[在\]
</dt> <dd>

類型： **int2**

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
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](texture2dms-load.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
