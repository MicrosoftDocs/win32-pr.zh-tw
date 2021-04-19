---
title: AlbumID 屬性
description: AlbumID 屬性是專輯的唯一識別碼。
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- AlbumID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993683"
---
# <a name="albumid-attribute"></a>AlbumID 屬性

**AlbumID** 屬性是專輯的唯一識別碼。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在程式庫中。

唯一識別碼是專輯標題和專輯演出者名稱的組合。 在此屬性中，專輯標題優先。 當您使用 [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) 方法取得使用此屬性的 **StringCollection** 物件時，這些值會依專輯標題排序。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AlbumIDAlbumArtist 屬性**](albumidalbumartist-attribute.md)
</dt> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





