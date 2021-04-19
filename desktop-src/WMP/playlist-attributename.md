---
title: 播放清單。 attributeName
description: AttributeName 屬性會在指定的索引處，抓取屬性的名稱。
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- 播放清單. attributeName Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995743"
---
# <a name="playlistattributename"></a>播放清單。 attributeName

**AttributeName** 屬性會在指定的索引處，抓取屬性的名稱。

## <a name="syntax"></a>Syntax

*玩家*。*currentPlaylist*。**attributeName** ( *索引* ) 

## <a name="parameters"></a>參數

*index*

包含索引的 (**長**) **數目**。

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

**AttributeCount** 屬性會抓取屬性數目。 有了索引， **attributeName** 會傳回可搭配 **setItemInfo** 或 **getItemInfo** 使用的 **字串**，以指定或抓取屬性的值。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

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

[**播放清單。 attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**播放清單。 getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**播放清單。 setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





