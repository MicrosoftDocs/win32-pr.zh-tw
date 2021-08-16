---
title: 控制項. play 方法
description: Play 方法會導致目前的媒體專案開始播放，或繼續播放暫停的專案。
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- play 方法 Windows Media Player
- play 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player、play 方法
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ce3c1572515b320a62b1b3c76aac72e44101e21f3b0f89d7c3356046ea95f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997448"
---
# <a name="controlsplay-method"></a>控制項. play 方法

**Play** 方法會導致目前的媒體專案開始播放，或繼續播放暫停的專案。

## <a name="syntax"></a>語法


```JScript
Controls.play()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果在快速轉送或倒轉時呼叫這個方法，*設定* 的值。**速率** 設定為1.0。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，此專案會使用 **播放** 來播放目前的媒體專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
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
</dt> </dl>

 

 





