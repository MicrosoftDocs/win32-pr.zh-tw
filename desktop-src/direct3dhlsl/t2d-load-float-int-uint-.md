---
title: Texture2D：： Load (int，int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |Texture2D：： Load (int，int，uint) 函數
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
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
ms.openlocfilehash: 0c591b92b64641e169023f30663d8f5c6ef8a6c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322280"
---
# <a name="texture2dloadintintuint-function"></a>Texture2D：： Load (int，int，uint) 函數

讀取材質資料並傳回作業的狀態。

## <a name="syntax"></a>語法


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位置* \[在\]
</dt> <dd>

類型： **int**

材質座標。

</dd> <dt>

*位移* \[在\]
</dt> <dd>

類型： **int**

在取樣之前套用至材質座標的位移。

</dd> <dt>

*狀態* \[擴展\]
</dt> <dd>

類型： **uint**

作業的狀態。 您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。 如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。 如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

輸入：

傳回型別符合 [**Texture2D**](sm5-object-texture2d.md) 物件宣告中的型別。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](texture2d-load.md)
</dt> </dl>

 

 
