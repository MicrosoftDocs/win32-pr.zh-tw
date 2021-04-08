---
title: Windows Media Player SDK) 的 Settings 物件 (
description: Settings 物件提供使用下列屬性和方法來修改各種 Windows Media Player 設定的方式。
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Settings 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "103841627"
---
# <a name="settings-object"></a>Settings 物件

**Settings** 物件提供使用下列屬性和方法來修改各種 Windows Media Player 設定的方式。

**Settings** 物件支援下列屬性。



| 屬性                                                  | 描述                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [啟動](settings-autostart.md)                       | 指定或抓取值，指出目前的媒體專案是否會自動開始播放。                           |
| [平衡](settings-balance.md)                           | 指定或抓取目前的立體餘額。                                                                               |
| [baseURL](settings-baseurl.md)                           | 使用內嵌在媒體檔案中的 URL 指令碼命令，指定或抓取用來解析相對路徑的基底 URL。 |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | 抓取 Windows Media Player 中指定之預設音訊語言 (LCID) 的地區設定識別碼。                          |
| [defaultFrame](settings-defaultframe.md)                 | 指定或抓取用來顯示 **ScriptCommand** 事件中所接收之 URL 的框架名稱。                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | 指定或抓取值，指出是否會自動顯示錯誤對話方塊。                                    |
| [invokeURLs](settings-invokeurls.md)                     | 指定或抓取值，指出 URL 事件是否應啟動網頁瀏覽器。                                        |
| [isAvailable](settings-isavailable.md)                   | 抓取指定的資訊類型是否可用，或是否可以執行指定的動作。                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | 抓取值，指出目前授與程式庫存取權的許可權。                                                    |
| [靜音](settings-mute.md)                                 | 指定或抓取值，指出音訊是否已靜音。                                                                |
| [playCount](settings-playcount.md)                       | 指定或抓取媒體專案將播放的次數。                                                               |
| [率](settings-rate.md)                                 | 指定或抓取目前的播放速率。                                                                                |
| [體積](settings-volume.md)                             | 指定或抓取目前的磁片區。                                                                                       |



 

**Settings** 物件支援下列方法。



| 方法                                                            | 描述                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | 判斷迴圈模式或隨機播放模式是否為使用中狀態。 |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | 要求指定的媒體櫃存取層級。        |
| [setMode](settings-setmode.md)                                   | 將迴圈模式或隨機模式設定為 [使用中] 或 [非使用中]。   |



 

您可以透過下列屬性來存取 **設定** 物件。



| Object                      | 屬性                        |
|-----------------------------|---------------------------------|
| [球員](player-object.md) | [設定](player-settings.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




