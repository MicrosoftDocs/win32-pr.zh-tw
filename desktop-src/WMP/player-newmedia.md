---
title: NewMedia 方法
description: NewMedia 方法會建立新的媒體物件。
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- newMedia 方法 Windows Media Player
- newMedia 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，newMedia 方法
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984835"
---
# <a name="playernewmedia-method"></a>NewMedia 方法

**NewMedia** 方法會建立新的 **媒體** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* \[在\]
</dt> <dd>

**字串** ，包含要用來建立 **媒體** 物件之數位媒體檔案的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **媒體** 物件。

## <a name="remarks"></a>備註

*URL* 參數不得為空字串或 null。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





