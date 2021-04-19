---
title: 'IWMPControls3 (VB 和 C ) 介面 (h.264. h) '
description: 提供適用于音訊語言選取的屬性和方法，以及補充 IWMPControls2 介面的支援。除了繼承自 IWMPControls2 的屬性和方法之外，IWMPControls3 介面也會公開下列屬性。
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- IWMPControls3 (VB 和 C ) 介面 Windows Media Player
- IWMPControls3 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9788dbd1b5910d655cbaa17055c76a0ae6d0280e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991131"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>IWMPControls3 (VB 和 c # ) 介面

提供適用于音訊語言選取的屬性和方法，以及補充 **IWMPControls2** 介面的支援。

除了繼承自 **IWMPControls2** 的屬性和方法之外， **IWMPControls3** 介面也會公開下列屬性。

## <a name="members"></a>成員

**IWMPControls3 (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPControls3 (VB 和 c # )** 介面都有這些方法。



| 方法                                                                                                         | 描述                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | 傳回對應至指定之以一為基礎之索引的音訊語言描述。<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | 傳回指定之音訊語言索引的 LCID。<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | 傳回具有指定之 LCID 的音訊語言名稱。<br/>                                |



 

### <a name="properties"></a>屬性

**IWMPControls3 (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                                              | 存取類型           | Description                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | 唯讀<br/>  | 取得支援的音訊語言計數。 <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | 讀取/寫入<br/> | 取得或設定用來播放之音訊語言 (LCID) 的地區設定識別碼。 <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | 讀取/寫入<br/> | 取得或設定對應至播放音訊語言的單一索引。 <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | 讀取/寫入<br/> | 使用時間代碼格式，取得或設定目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。 <br/> |



 

藉由轉換 [**AxWindowsMediaPlayer Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)屬性所傳回的值來取得 **IWMPControls3** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls2 介面 (VB 和 c # )**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





