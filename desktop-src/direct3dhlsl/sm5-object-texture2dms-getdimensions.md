---
title: Texture2DMS：： GetDimensions 函數
description: 傳回資源的維度。 |Texture2DMS：： GetDimensions 函數
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: dbe034b6484b80efb58712196c4bd4d0aa67800c51f659c97b0d400e934eeecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985828"
---
# <a name="texture2dmsgetdimensions-function"></a>Texture2DMS：： GetDimensions 函數

傳回資源的維度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a>參數

<dl> <dt>

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

*NumberOfSamples* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

範例位置的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

這是此方法的多載版本清單。


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
