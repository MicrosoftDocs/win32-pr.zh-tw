---
title: RWTexture3D：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture3D：： Load (int) 函數
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322216"
---
# <a name="rwtexture3dloadint-function"></a>RWTexture3D：： Load (int) 函數

讀取紋理資料。

## <a name="syntax"></a>語法


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **int**

材質的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

輸入：

傳回型別符合 [**RWTexture3D**](sm5-object-rwtexture3d.md) 物件宣告中的型別。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwtexture3d-load.md)
</dt> </dl>

 

 




