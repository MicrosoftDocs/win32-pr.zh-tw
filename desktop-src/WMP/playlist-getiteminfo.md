---
title: GetItemInfo 方法
description: GetItemInfo 方法會捕獲播放清單屬性的值。
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48a9106a4aba6a5080724faccc856a1515e7a7398a1c75df2fa1e99bf86f342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118834875"
---
# <a name="playlistgetiteminfo-method"></a>GetItemInfo 方法

**GetItemInfo** 方法會捕獲播放清單屬性的值。

## <a name="syntax"></a>語法


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含要抓取的屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

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

[**播放清單。 setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





