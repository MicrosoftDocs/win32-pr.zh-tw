---
title: RWTexture1DArray：： Load (int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |RWTexture1DArray：： Load (int，uint) 函數
ms.assetid: EF1D51CC-E037-4E04-9DD6-6A9C5950E5B5
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
ms.openlocfilehash: 5a46dde9b75d3194cc081409fe2b450c5453d7c1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973992"
---
# <a name="rwtexture1darrayloadintuint-function"></a>RWTexture1DArray：： Load (int，uint) 函數

讀取材質資料並傳回作業的狀態。

## <a name="syntax"></a>語法


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **int**

材質的位置。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

類型： **uint**

作業的狀態。 您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。 如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。 如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

輸入：

傳回型別符合 [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) 物件宣告中的型別。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](rwtexture1darray-load.md)
</dt> </dl>

 

 
