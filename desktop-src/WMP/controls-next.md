---
title: Controls. next 方法
description: 下一個方法會將目前的專案設定為播放清單中的下一個專案。
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- next 方法 Windows Media Player
- next 方法 Windows Media Player，Controls 類別
- 控制項類別 Windows Media Player、next 方法
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a40c063163b0dadaa3db2d0d6281ace64312f68ee999763e6b27d4bd98f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997468"
---
# <a name="controlsnext-method"></a>Controls. next 方法

**下一個** 方法會將目前的專案設定為播放清單中的下一個專案。

## <a name="syntax"></a>語法


```JScript
Controls.next()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果叫用 [ **下一步]** 時，播放清單是最後一個專案，播放清單中的第一個專案就會成為目前的專案。

針對伺服器端播放清單，這個方法會跳至伺服器端播放清單中的下一個專案，而不是用戶端播放清單。

播放 DVD 時，此方法會跳到播放順序中的下一個邏輯章節，這可能不是播放清單中的下一章。 播放 DVD 靜止時，此方法會跳到下一個仍然的。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，使用 **[下一步]** 移至目前播放清單中的下一個專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
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

[**控制項。上一個**](controls-previous.md)
</dt> <dt>

[**控制項。停止**](controls-stop.md)
</dt> </dl>

 

 





