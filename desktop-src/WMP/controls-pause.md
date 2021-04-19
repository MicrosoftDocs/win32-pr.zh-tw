---
title: Controls. pause 方法
description: Pause 方法會暫停播放媒體專案。 |Controls. pause 方法
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- pause 方法 Windows Media Player
- pause 方法 Windows Media Player、Controls 類別
- 控制項類別 Windows Media Player、pause 方法
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979517"
---
# <a name="controlspause-method"></a>Controls. pause 方法

**Pause** 方法會暫停播放媒體專案。

## <a name="syntax"></a>語法


```JScript
Controls.pause()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當檔案暫停時，Windows Media Player 不會提供任何系統資源，例如音訊裝置。

某些媒體類型無法暫停，例如即時資料流。 若要判斷特定媒體類型是否可以暫停，請使用 *控制項*。**isAvailable ( ' Pause ' )**。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，以使用 **pause** 來暫停播放。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
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

[**IsAvailable**](controls-isavailable.md)
</dt> </dl>

 

 





