---
title: Texture2D：： GetDimensions 函數
description: 傳回資源的維度。 |Texture2D：： GetDimensions 函數
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: 46eb5101dc119d2779f60d2e2b39a42c695933a5bffd477b407fea56c930038c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067698"
---
# <a name="texture2dgetdimensions-function"></a>Texture2D：： GetDimensions 函數

傳回資源的維度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*MipLevel* \[在\]
</dt> <dd>

類型： **uint**

選擇性。 如果) 使用 *NumberOfLevels* ，則必須指定 mipmap 層級 (。

</dd> <dt>

*寬度* \[擴展\]
</dt> <dd>

類型： **uint**

資源寬度，以材質。

</dd> <dt>

*高度* \[擴展\]
</dt> <dd>

類型： **uint**

資源高度，以材質。

</dd> <dt>

*NumberOfLevels* \[擴展\]
</dt> <dd>

類型： **uint**

 (的 mipmap 層級數目需要 *MipLevel* 也) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

Nothing

## <a name="remarks"></a>備註

這是此方法的多載版本清單。


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




