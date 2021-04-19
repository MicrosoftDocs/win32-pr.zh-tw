---
title: IsIdentical 方法
description: IsIdentical 方法會抓取值，指出提供的物件是否與目前的物件相同。 |IsIdentical 方法
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- isIdentical 方法 Windows Media Player
- isIdentical 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，isIdentical 方法
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999268"
---
# <a name="mediaisidentical-method"></a>IsIdentical 方法

**IsIdentical** 方法會抓取值，指出提供的物件是否與目前的物件相同。

## <a name="syntax"></a>語法


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*媒體* \[在\]
</dt> <dd>

要與目前 **媒體** 物件比較的 **媒體** 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**isIdentical** ，檢查名為 newMedia 的媒體專案是否與目前的媒體專案相同。 如果兩者不同，則會播放新的媒體專案。 否則，目前的媒體會繼續播放不中斷的。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> </dl>

 

 





