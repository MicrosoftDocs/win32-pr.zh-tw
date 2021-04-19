---
title: FastReverse 方法
description: FastReverse 方法會以反向方向啟動媒體專案的快速掃描。
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- fastReverse 方法 Windows Media Player
- fastReverse 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，fastReverse 方法
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987079"
---
# <a name="controlsfastreverse-method"></a>FastReverse 方法

**FastReverse** 方法會以反向方向啟動媒體專案的快速掃描。

## <a name="syntax"></a>語法


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**FastReverse** 方法會以正常速度的五倍反向掃描剪輯，如果是影片檔案，則只會顯示主要畫面格。 叫用 **fastReverse** 會變更 *設定*。**rate** 屬性為5.0。 如果之後變更了 **速率** ，或呼叫了 **播放** 或 **停止** ，Windows Media Player 將會停止快速反轉。

如果專案是播放清單的一部分， **fastReverse** 就會在目前的播放軌開始時停止。比方說，如果 track 3 是在 **fastReverse** 中，當到達 track 3 的開頭時，Windows Media Player 將不會移至「追蹤2」。 呼叫 **fastReverse** 時，播放次數不會遞增。

如果您在 **fastReverse** 生效時呼叫 **fastForward** ， **fastReverse** 將會停止，而且 **fastForward** 將會開始。

這個方法不適用於即時廣播和特定媒體類型。 若要判斷您是否可以在剪輯中使用快速反轉，請呼叫 **isAvailable** ( "FastReverse" ) 。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，以使用 **fastReverse** 來啟動媒體專案的快速反向播放。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
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

[**FastForward**](controls-fastforward.md)
</dt> <dt>

[**IsAvailable**](controls-isavailable.md)
</dt> <dt>

[**控制項. play**](controls-play.md)
</dt> <dt>

[**控制項。停止**](controls-stop.md)
</dt> <dt>

[**設定。費率**](settings-rate.md)
</dt> </dl>

 

 





