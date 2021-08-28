---
title: 媒體物件
description: 媒體物件提供使用下列屬性和方法來指定或取出媒體專案屬性的方法。
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- 媒體物件 Windows Media Player
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c1dbcb3dc662a431f279e03697620b80c242c99eb32e3bbcdc26d71796f7e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123308"
---
# <a name="media-object"></a>媒體物件

**媒體** 物件提供使用下列屬性和方法來指定或取出媒體專案屬性的方法。

**媒體** 物件支援下列屬性。



| 屬性                                         | 描述                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | 抓取可針對媒體專案查詢及/或設定的屬性數目。              |
| [duration](media-duration.md)                   | 抓取目前媒體專案的持續時間（以秒為單位）。                                       |
| [durationString](media-durationstring.md)       | 抓取 **字串** 值，指出目前媒體專案的持續時間（以 HH： MM： SS 格式表示）。 |
| [error](media-error.md)                         | 如果媒體專案有錯誤條件，則抓取 [ErrorItem](erroritem-object.md) 物件。    |
| [imageSourceHeight](media-imagesourceheight.md) | 抓取目前媒體專案的高度（以圖元為單位）。                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | 抓取目前媒體專案的寬度（以圖元為單位）。                                           |
| [markerCount](media-markercount.md)             | 捕獲媒體專案中的標記數目。                                                 |
| [name](media-name.md)                           | 指定或抓取媒體專案的名稱。                                                 |
| [sourceURL](media-sourceurl.md)                 | 抓取媒體專案的 URL。                                                               |



 

**媒體** 物件支援下列方法。



| 方法                                                       | 描述                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | 抓取與指定的屬性名稱和語言相關聯的屬性數目。            |
| [getAttributeName](media-getattributename.md)               | 抓取對應于指定索引之屬性的名稱。                                |
| [getItemInfo](media-getiteminfo.md)                         | 抓取媒體專案的指定屬性值。                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | 抓取具有指定之索引編號的屬性值。                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | 抓取對應于指定屬性名稱、語言和索引的屬性值。 |
| [getMarkerName](media-getmarkername.md)                     | 抓取位於指定之索引處的標記名稱。                                                 |
| [getMarkerTime](media-getmarkertime.md)                     | 抓取位於指定索引處之標記的時間。                                                 |
| [isIdentical](media-isidentical.md)                         | 抓取值，指出提供的物件是否與目前的物件相同。                 |
| [isMemberOf](media-ismemberof.md)                           | 抓取值，指出指定的媒體專案是否為指定播放清單的成員。     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | 抓取值，指出是否可以編輯指定之媒體專案的屬性。           |
| [setItemInfo](media-setiteminfo.md)                         | 設定媒體專案的指定屬性值。                                            |



 

**媒體** 物件可透過下列屬性和方法來存取。



| Object                          | 屬性或方法                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [控制項](controls-object.md) | [currentItem](controls-currentitem.md)                                  |
| [球員](player-object.md)     | [currentMedia](player-currentmedia.md)、 [newMedia](player-newmedia.md) |
| [播放 清單](playlist-object.md) | [item](playlist-item.md)                                                |



 

因為這是最常見的存取方式，也就是 *播放機*。**currentMedia** 是用於參考語法區段中的說明用途。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




