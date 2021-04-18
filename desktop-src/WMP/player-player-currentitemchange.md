---
title: CurrentItemChange 事件
description: CurrentItem 變更時，就會發生 CurrentItemChange 事件。
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- CurrentItemChange 事件 Windows Media Player
- CurrentItemChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentItemChange 事件
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996474"
---
# <a name="playercurrentitemchange-event"></a>CurrentItemChange 事件

當 *控制項* 時，就會發生 **CurrentItemChange** 事件。**currentItem** 變更。

## <a name="syntax"></a>語法


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="examples"></a>範例

下列 JScript 範例示範 *播放* 程式的事件處理常式。**currentItemChange** 事件。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CurrentItem**](controls-currentitem.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





