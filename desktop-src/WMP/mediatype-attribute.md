---
title: 媒體屬性
description: '[媒體類型] 屬性是專案中的內容類型。'
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- 媒體屬性 Windows Media Player
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977678"
---
# <a name="mediatype-attribute"></a>媒體屬性

[ **媒體** 類型] 屬性是專案中的內容類型。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [相片專案](photo-item-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [單選項目](radio-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在程式庫中。

此屬性具有下列其中一個值：「音訊」、「其他」、「相片」、「播放清單」、「單選」或「影片」。 將此屬性與 *MediaCollection* 搭配使用。**getByAttribute** 方法，以取得包含特定類型之所有專案的播放清單。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> <dt>

[**MediaCollection.getByAttribute**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





