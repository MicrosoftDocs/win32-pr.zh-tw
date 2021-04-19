---
title: MediaChange 事件
description: 當媒體專案變更時，就會發生 MediaChange 事件。 |MediaChange 事件
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- MediaChange 事件 Windows Media Player
- MediaChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaChange 事件
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995446"
---
# <a name="playermediachange-event"></a>MediaChange 事件

當媒體專案變更時，就會發生 **MediaChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Item* 
</dt> <dd>

代表已變更之專案的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="examples"></a>範例

下列 JScript 範例會使用名為 MediaName 的 HTML DIV 元素，來顯示目前媒體專案的名稱。 程式碼會更新 DIV 中每次出現 **mediaChange** 事件的文字。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





