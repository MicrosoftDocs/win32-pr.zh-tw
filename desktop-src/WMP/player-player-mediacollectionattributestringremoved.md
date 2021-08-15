---
title: MediaCollectionAttributeStringRemoved 事件
description: 從程式庫移除屬性值時，就會發生 MediaCollectionAttributeStringRemoved 事件。 |MediaCollectionAttributeStringRemoved 事件
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- MediaCollectionAttributeStringRemoved 事件 Windows Media Player
- MediaCollectionAttributeStringRemoved 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionAttributeStringRemoved 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b89e46d4dbe86f185fb636b5c8de453e2addbf83c92d1231b5f067ce0b3b1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747404"
---
# <a name="playermediacollectionattributestringremoved-event"></a>MediaCollectionAttributeStringRemoved 事件

從程式庫移除屬性值時，就會發生 **MediaCollectionAttributeStringRemoved** 事件。

## <a name="syntax"></a>語法


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

指定屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**字串** ，指定屬性的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

從程式庫中移除媒體專案時，會從 **MediaCollection** 物件移除其中繼資料，並針對移除的每個屬性引發此事件。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

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

 

 





