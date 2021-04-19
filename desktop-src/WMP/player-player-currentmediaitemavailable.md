---
title: CurrentMediaItemAvailable 事件
description: 當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 CurrentMediaItemAvailable 事件。 |CurrentMediaItemAvailable 事件
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- CurrentMediaItemAvailable 事件 Windows Media Player
- CurrentMediaItemAvailable 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentMediaItemAvailable 事件
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990045"
---
# <a name="playercurrentmediaitemavailable-event"></a>CurrentMediaItemAvailable 事件

當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 **CurrentMediaItemAvailable** 事件。

## <a name="syntax"></a>語法


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrItemName* 
</dt> <dd>

包含目前媒體專案名稱的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

因為播放可以在媒體專案完全下載之前開始播放，所以媒體專案中包含的任何元資料圖形 (例如專輯封面) 在開始播放時可能無法使用。 此事件會在元資料圖形專案完成下載時發出警示。 然後，您可以藉由將 *bstrItemName* 的值傳遞給 *MediaCollection*，來取得 **媒體** 物件。**getByName** 方法，之後您就可以使用 *媒體* 來存取元資料圖形專案。**getItemInfoByType** 並為屬性名稱指定 **WM/圖片**。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**MediaCollection.getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





