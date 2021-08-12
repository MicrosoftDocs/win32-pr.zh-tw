---
title: '[] 方法'
description: '[] 方法會建立新的播放清單物件。'
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，Player 類別'
- Player 類別 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380d1f2751487f5c648b154852be625a5c93103851541dea7e2488ba75080ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572828"
---
# <a name="playernewplaylist-method"></a>[] 方法

**[]** 方法會建立新的 **播放清單** 物件。

## <a name="syntax"></a>語法


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含新播放清單名稱的 **字串**。

</dd> <dt>

*URL* \[在\]
</dt> <dd>

**字串**，包含用來建立 **播放清單** 物件之 Windows 媒體中繼檔播放清單的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **播放清單** 物件。

## <a name="remarks"></a>備註

如果 *URL* 參數設定為 null 或 "" (空白字串) ，則會建立空白的 **播放清單** 物件。 如果 *name* 參數設定為 ""，則會使用中繼檔中的名稱。

使用這個方法建立的新播放清單，不會新增至程式庫。 若要將新的播放清單新增至程式庫，請使用 *PlaylistCollection*。**importPlaylist** 或 *PlaylistCollection*。**[]**。 新增至程式庫時，會自動移除播放清單名稱中的任何前置或尾端空格。

由於程式庫允許多個具有相同名稱的播放清單，因此您可能會想要先檢查具有指定名稱的播放清單是否存在，然後再新增一個。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. []**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Windows媒體中繼檔**](windows-media-metafiles.md)
</dt> </dl>

 

 





