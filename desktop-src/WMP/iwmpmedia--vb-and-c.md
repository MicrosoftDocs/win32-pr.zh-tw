---
title: 'IWMPMedia (VB 和 C ) 介面 (h.264. h) '
description: 提供一種方式來設定和取出媒體專案的屬性。IWMPMedia 介面會公開下列屬性。
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB 和 C ) 介面 Windows Media Player
- IWMPMedia (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980163"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>IWMPMedia (VB 和 c # ) 介面

提供一種方式來設定和取出媒體專案的屬性。

**IWMPMedia** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPMedia (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPMedia (VB 和 c # )** 介面都有這些方法。



| 方法                                                                             | 描述                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | 傳回對應至指定之索引的屬性名稱。<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | 傳回媒體專案的指定屬性值。<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | 傳回具有指定之索引編號的屬性值。<br/>                                |
| [**getMarkerName**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | 傳回指定索引處的標記名稱。<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | 傳回指定索引處之標記的時間。<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | 傳回值，指出指定的媒體專案是否為指定播放清單的成員。<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | 傳回值，這個值表示是否可以編輯指定之媒體專案的屬性。<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | 設定媒體專案的指定屬性值。<br/>                                      |



 

### <a name="properties"></a>屬性

**IWMPMedia (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                      | 存取類型          | Description                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | 唯讀<br/> | 取得可針對媒體專案查詢及/或設定的屬性數目。<br/>                                                          |
| [**時間**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | 唯讀<br/> | 取得目前媒體專案的持續時間（以秒為單位）。<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | 唯讀<br/> | 取得值，指出目前媒體專案的持續時間（以 HH： MM： SS 格式表示）。<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | 唯讀<br/> | 取得目前媒體專案的高度（以圖元為單位）。<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | 唯讀<br/> | 取得目前媒體專案的寬度（以圖元為單位）。<br/>                                                                                       |
| [**isIdentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | 唯讀<br/> | 取得值，指出指定的媒體專案是否與目前的專案相同。 在 c # 中，這是 **get \_ isIdentical** 方法。<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | 唯讀<br/> | 取得媒體專案中的標記數目。<br/>                                                                                             |
| [**名字**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | 唯讀<br/> | 取得或設定媒體專案的名稱。<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | 唯讀<br/> | 取得媒體專案的 URL。<br/>                                                                                                           |



 

使用透過下列物件或介面存取的下列屬性或方法，取得 **IWMPMedia** 介面。



| 物件或介面                                               | 屬性或方法                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)、 [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [](iwmpplaylist-item--vb-and-c.md) \_ 在 c # 中取得專案 (專案 )                                                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMedia2 介面 (VB 和 c # )**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3 介面 (VB 和 c # )**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





