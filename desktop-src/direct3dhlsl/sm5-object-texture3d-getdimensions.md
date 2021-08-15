---
title: Texture3D：： GetDimensions 函數
description: 傳回資源的維度。 |Texture3D：： GetDimensions 函數
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 8a7dd6248b7b6effc08e510ea56da6426c41dc54418bf7ee5da8cdc3c9ad965a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985708"
---
# <a name="texture3dgetdimensions-function"></a>Texture3D：： GetDimensions 函數

傳回資源的維度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*MipLevel* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

選擇性。 如果) 使用 *NumberOfLevels* ，則必須指定 Mipmap 層級 (。

</dd> <dt>

*寬度* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源寬度，以材質。

</dd> <dt>

*高度* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源高度，以材質。

</dd> <dt>

*深度* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源深度，以材質。

</dd> <dt>

*NumberOfLevels* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

 (的 mipmap 層級數目需要 *MipLevel* 也) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

Nothing

## <a name="remarks"></a>備註

這是此方法的多載版本清單。


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
