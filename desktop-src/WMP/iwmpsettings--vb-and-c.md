---
title: 'IWMPSettings (VB 和 C ) 介面 (Wmp. h) '
description: 提供屬性和方法，以取得或設定 Windows Media Player 設定的值。IWMPSettings 介面會公開下列屬性。
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- IWMPSettings (VB 和 C ) 介面 Windows Media Player
- IWMPSettings (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPSettings (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a537efcd9b39f993705244020e579b9d667164180fd5cd70ab05fc692bed8fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996468"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>IWMPSettings (VB 和 c # ) 介面

提供屬性和方法，以取得或設定 Windows Media Player 設定的值。

**IWMPSettings** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPSettings (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPSettings (VB 和 c # )** 介面都有這些方法。



| 方法                                                               | 描述                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | 傳回值，這個值表示迴圈模式或隨機播放模式是否為使用中狀態。<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | 將迴圈模式或隨機模式設定為 [使用中] 或 [非使用中]。<br/>               |



 

### <a name="properties"></a>屬性

**IWMPSettings (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                              | 存取類型           | 描述                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**啟動**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | 讀取/寫入<br/> | 取得或設定值，這個值表示目前的媒體專案是否會自動開始播放。 <br/>                                     |
| [**平衡**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | 讀取/寫入<br/> | 取得或設定目前的立體餘額。<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | 讀取/寫入<br/> | 取得或設定基底 URL，這個基底 URL 用於以數位媒體內容內嵌的 URL 指令碼命令進行相對路徑解析。 <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | 讀取/寫入<br/> | 取得或設定用來顯示 **scriptCommand** 事件中所接收之 URL 的框架名稱。 <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | 讀取/寫入<br/> | 取得或設定值，這個值表示是否會自動顯示錯誤對話方塊。<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | 讀取/寫入<br/> | 取得或設定值，指出 URL 事件是否應啟動網頁瀏覽器。 <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | 唯讀<br/>  | 取得值，這個值表示是否可以執行指定的動作。 在 c # 中，這是 **get \_ isAvailable** 方法。<br/>             |
| [**靜音**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | 讀取/寫入<br/> | 取得或設定值，指出音訊是否為靜音。 <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | 讀取/寫入<br/> | 取得或設定媒體專案將播放的次數。 <br/>                                                                         |
| [**率**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | 讀取/寫入<br/> | 取得或設定影片目前的播放速率。 <br/>                                                                                |
| [**體積**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | 讀取/寫入<br/> | 取得或設定目前的播放磁片區。 <br/>                                                                                        |



 

使用下列屬性來取得 **IWMPSettings** 介面。



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

[**IWMPSettings2 介面 (VB 和 c # )**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





