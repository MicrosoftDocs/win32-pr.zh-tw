---
title: Player。錯誤事件
description: 發生錯誤情況時，就會發生錯誤事件。
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- 錯誤事件 Windows Media Player
- 錯誤事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，錯誤事件
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a7e4642eef19b4edc4b1aa5bc75022a307d279d0d60482af0c7e2f0a9368c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134811"
---
# <a name="playererror-event"></a>Player。錯誤事件

發生錯誤情況時，就會發生 **錯誤** 事件。

## <a name="syntax"></a>語法


```JScript
Player.Error()
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="examples"></a>範例

下列 JScript 範例會建立事件處理常式，以顯示錯誤佇列中第一個錯誤的描述文字。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**錯誤。專案**](error-item.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





