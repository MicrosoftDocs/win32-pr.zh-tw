---
title: 'IWMPMediaCollection2 (VB 和 C ) 介面 (h.264. h) '
description: 提供補充 IWMPMediaCollection 介面的方法。
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB 和 C ) 介面 Windows Media Player
- IWMPMediaCollection2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976125"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>IWMPMediaCollection2 (VB 和 c # ) 介面

提供補充 **IWMPMediaCollection** 介面的方法。

## <a name="members"></a>成員

**IWMPMediaCollection2 (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMPMediaCollection2 (VB 和 c # )** 介面都有這些方法。



| 方法                                                                                                                     | 描述                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**createQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | 傳回代表新查詢的 **IWMPQuery** 介面。<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | 傳回 **IWMPPlaylist** 介面，這個介面會提供具有指定屬性和媒體類型之媒體專案的存取權。<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | 傳回 **IWMPPlaylist** 介面，這個介面會提供符合查詢準則之媒體專案的存取權。<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | 傳回 **IWMPStringCollection** 介面，這個介面可讓您存取符合查詢準則之指定屬性的所有字串值集。<br/> |



 

藉由轉換 [**AxWindowsMediaPlayer mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)屬性所傳回的值，或由 [**IWMPLibrary. mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)屬性傳回的值來取得 **IWMPMediaCollection2** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





