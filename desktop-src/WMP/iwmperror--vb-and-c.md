---
title: 'IWMPError (VB 和 C ) 介面 (h.264. h) '
description: 提供屬性和方法，以存取 IWMPErrorItem 介面的集合，以取得錯誤資訊。IWMPError 介面會公開下列屬性。
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- IWMPError (VB 和 C ) 介面 Windows Media Player
- IWMPError (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289a39093c38e7a4b0cc43cb8f318e321ae8ef53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978714"
---
# <a name="iwmperror-vb-and-c-interface"></a>IWMPError (VB 和 c # ) 介面

提供屬性和方法，以存取 **IWMPErrorItem** 介面的集合，以取得錯誤資訊。

**IWMPError** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPError (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPError (VB 和 c # )** 介面都有這些方法。



| 方法                                                                         | 描述                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | 清除錯誤佇列中的錯誤。<br/>                                                                                            |
| [**webHelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | 啟動 Microsoft Windows Media Player Web 說明頁面，以顯示錯誤佇列中第一個錯誤的進一步資訊。<br/> |



 

### <a name="properties"></a>屬性

**IWMPError (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                        | 存取類型           | Description                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | 唯讀<br/>  | 取得錯誤佇列中的錯誤數目。<br/>                                                                            |
| [**項目**](iwmperror-item--vb-and-c.md)<br/>                             | 讀取/寫入<br/> | 取得在錯誤佇列中指定索引處的 **IWMPErrorItem** 介面。 在 c # 中，這是 **取得 \_ 專案** 方法。<br/> |



 

使用下列屬性來取得 **IWMPError** 介面。



| Object                                                                   | 屬性                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [AxWindowsMediaPlayer 物件](axwindowsmediaplayer-object--vb-and-c.md) | [**錯誤**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPErrorItem 介面 (VB 和 c # )**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





