---
title: AlbumIDAlbumArtist 屬性
description: AlbumIDAlbumArtist 屬性是專輯的唯一識別碼。
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- AlbumIDAlbumArtist 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001845"
---
# <a name="albumidalbumartist-attribute"></a>AlbumIDAlbumArtist 屬性

**AlbumIDAlbumArtist** 屬性是專輯的唯一識別碼。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在程式庫中。

唯一識別碼是專輯標題和專輯演出者名稱的組合。 在此屬性中，專輯演出者名稱優先。 當您使用 [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) 方法取得使用此屬性的 **StringCollection** 物件時，這些值會依專輯演出者名稱排序。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AlbumID 屬性**](albumid-attribute.md)
</dt> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





