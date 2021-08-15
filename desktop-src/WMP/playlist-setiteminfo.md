---
title: SetItemInfo 方法
description: SetItemInfo 方法會指定播放清單屬性的值。
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47208d1fad03a57e26d1f5591adf658c7553a9087254b49c7aecfd904bd4d95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335745"
---
# <a name="playlistsetiteminfo-method"></a>SetItemInfo 方法

**SetItemInfo** 方法會指定播放清單屬性的值。

## <a name="syntax"></a>語法


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含要設定之屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> <dt>

*值* \[在\]
</dt> <dd>

包含屬性之新值的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**SetItemInfo** 方法的特殊用途是使用 SortAttribute 屬性來排序播放清單中的專案。 下列 JScript 範例會依 UserLastPlayedTime 屬性的值來排序播放清單。 變數播放清單是 **播放清單** 物件的參考。


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

如需使用這個屬性的範例程式碼，請參閱 [attributeCount](playlist-attributecount.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**播放清單。 getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





