---
title: Texture2DArray：： Load (int，int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |Texture2DArray：： Load (int，int，uint) 函數
ms.assetid: 551EA931-6D24-478B-B741-3DD5B1E030E2
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
ms.openlocfilehash: 0907ddb4f5100ae6bffc81214ed0bed0d7857462e12c4625f179d6b769915569
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723583"
---
# <a name="texture2darrayloadintintuint-function"></a>Texture2DArray：： Load (int，int，uint) 函數

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

傳回型別符合 [**Texture2DArray**](sm5-object-texture2darray.md) 物件宣告中的型別。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[載入方法](texture2darray-load.md)
</dt> </dl>

 

 
