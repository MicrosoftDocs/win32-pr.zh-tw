---
title: MediaCollectionAttributeStringAdded 事件
description: 將屬性值新增至程式庫時，就會發生 MediaCollectionAttributeStringAdded 事件。 |MediaCollectionAttributeStringAdded 事件
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- MediaCollectionAttributeStringAdded 事件 Windows Media Player
- MediaCollectionAttributeStringAdded 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionAttributeStringAdded 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993616"
---
# <a name="playermediacollectionattributestringadded-event"></a>MediaCollectionAttributeStringAdded 事件

將屬性值新增至程式庫時，就會發生 **MediaCollectionAttributeStringAdded** 事件。

## <a name="syntax"></a>語法


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

指定屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**字串** ，指定屬性的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當媒體專案加入至程式庫時，它的中繼資料會加入至 **MediaCollection** 物件，而且會針對每個加入的屬性引發此事件。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**MediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





