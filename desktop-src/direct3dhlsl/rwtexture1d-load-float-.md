---
title: RWTexture1D：： Load (int) 函數
description: 讀取紋理資料。 |RWTexture1D：： Load (int) 函數
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: f8d502d6e4fd1f13355c17fbd1ef9c42b3c6de2ec5aa20176aec562af807dd3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981618"
---
# <a name="rwtexture1dloadint-function"></a>RWTexture1D：： Load (int) 函數

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

傳回型別符合 [**RWTexture1D**](sm5-object-rwtexture1d.md) 物件宣告中的型別。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwtexture1d-load.md)
</dt> </dl>

 

 




