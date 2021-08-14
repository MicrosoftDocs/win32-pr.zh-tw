---
title: Controls. stop 方法
description: Stop 方法會停止播放媒體專案。 |Controls. stop 方法
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- stop 方法 Windows Media Player
- stop 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，stop 方法
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882f462903c2c5f75a3655cd26b927e7439043828dad41fcce7d0e64e4ce812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580157"
---
# <a name="controlsstop-method"></a>Controls. stop 方法

**Stop** 方法會停止播放媒體專案。

## <a name="syntax"></a>語法


```JScript
Controls.stop()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會使 Windows Media Player 釋出它所使用的任何系統資源，例如音訊裝置。 但目前的媒體專案則不會釋出。

當播放程式停止時，播放軌會倒轉至一開始。 然後呼叫 **play** 將開始播放剪輯。 若要在不變更目前位置的情況下暫停播放操作，請使用 **pause** 方法。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 元素，以使用 **stop** 停止播放。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**控制項。下一步**](controls-next.md)
</dt> <dt>

[**控制項。暫停**](controls-pause.md)
</dt> <dt>

[**控制項。上一個**](controls-previous.md)
</dt> </dl>

 

 





