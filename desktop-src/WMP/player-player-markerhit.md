---
title: MarkerHit 事件
description: 當到達標記時，就會發生 MarkerHit 事件。 |MarkerHit 事件
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- MarkerHit 事件 Windows Media Player
- MarkerHit 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MarkerHit 事件
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b065b9c7499beb2433c0b7c76180a6073b13be589f710aec0810299ab249b91c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389108"
---
# <a name="playermarkerhit-event"></a>MarkerHit 事件

當到達標記時，就會發生 **MarkerHit** 事件。

## <a name="syntax"></a>語法


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*MarkerNum* 
</dt> <dd>

**Number** (**Long**) ，表示已點擊的標記數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





