---
title: MediaCollectionAttributeStringChanged 事件
description: 當程式庫中的屬性值變更時，就會發生 MediaCollectionAttributeStringChanged 事件。 |MediaCollectionAttributeStringChanged 事件
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- MediaCollectionAttributeStringChanged 事件 Windows Media Player
- MediaCollectionAttributeStringChanged 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionAttributeStringChanged 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9435be90761abf88927789fad4380172f0ef6f31427848195d3aa14ea4112cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747394"
---
# <a name="playermediacollectionattributestringchanged-event"></a>MediaCollectionAttributeStringChanged 事件

當程式庫中的屬性值變更時，就會發生 **MediaCollectionAttributeStringChanged** 事件。

## <a name="syntax"></a>語法


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

指定屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**字串** ，指定屬性的舊值。

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**字串** ，指定屬性的新值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當使用者修改程式庫中繼資料時，會更新 **MediaCollection** 物件，並針對每個屬性變更引發此事件。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**MediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





