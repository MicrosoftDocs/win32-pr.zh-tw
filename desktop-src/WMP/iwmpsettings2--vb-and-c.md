---
title: 'IWMPSettings2 (VB 和 C ) 介面 (Wmp. h) '
description: 提供可補充 IWMPSettings 介面的屬性和方法。除了繼承自 IWMPSettings 的屬性和方法之外，IWMPSettings2 介面也會公開下列屬性。
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- IWMPSettings2 (VB 和 C ) 介面 Windows Media Player
- IWMPSettings2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPSettings2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e227cc255eee625df926031369ef8be0fe270e377b143adff2c3ed2d9ab0aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135351"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>IWMPSettings2 (VB 和 c # ) 介面

提供可補充 **IWMPSettings** 介面的屬性和方法。

除了繼承自 **IWMPSettings** 的屬性和方法之外， **IWMPSettings2** 介面也會公開下列屬性。

## <a name="members"></a>成員

**IWMPSettings2 (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPSettings2 (VB 和 c # )** 介面都有這些方法。



| 方法                                                                                                   | 描述                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | 要求指定的媒體櫃存取層級。<br/> |



 

### <a name="properties"></a>屬性

**IWMPSettings2 (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                                    | 存取類型          | 描述                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | 唯讀<br/> | 取得預設音訊語言 (LCID) 的地區設定識別碼。 <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | 唯讀<br/> | 取得值，指出目前授與存取程式庫的許可權。 <br/> |



 

藉由轉換 **AxWindowsMediaPlayer. settings** 屬性所傳回的值來取得 **IWMPSettings2** 介面。



| Object                                                                   | 屬性                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [AxWindowsMediaPlayer 物件](axwindowsmediaplayer-object--vb-and-c.md) | [**設置**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .net 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





