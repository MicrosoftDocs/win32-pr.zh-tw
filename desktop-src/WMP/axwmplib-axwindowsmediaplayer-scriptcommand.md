---
title: AxWindowsMediaPlayer 物件的 ScriptCommand 事件
description: 收到同步處理的命令或 URL 時，就會發生 ScriptCommand 事件。 |AxWindowsMediaPlayer 物件的 ScriptCommand 事件
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- AxWindowsMediaPlayer 物件的 ScriptCommand 事件 Windows Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26724d8d2d86bd14be9aa5360678dd9caf54620e48d4b361ab120bc2b8927fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509328"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a>AxWindowsMediaPlayer 物件的 ScriptCommand 事件

收到同步處理的命令或 URL 時，就會發生 ScriptCommand 事件。

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a>事件資料

與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ ScriptCommandEventHandler**。 這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ ScriptCommandEvent**，其中包含與這個事件相關的下列屬性。



| 屬性 | 描述                                                   |
|----------|---------------------------------------------------------------|
| scType   | StringSpecifies 指令碼命令的類型。<br/> |
| 參數    | StringSpecifies 指令碼命令。<br/>         |



 

## <a name="remarks"></a>備註

您可以將命令內嵌在 Windows 媒體檔案或資料流程的聲音和影像中。 這些命令是與資料流程中指定時間相關聯的一對 Unicode 字串。 當資料流程到達與命令相關聯的時間時，Windows Media Player 控制項會傳送具有兩個參數的 **ScriptCommand** 事件。 其中一個參數指定要傳送的命令類型，另一個參數則指定命令。 參數的類型是用來決定如何處理命令參數。 任何類型的命令都可以內嵌在檔案或資料流程中，以供 **ScriptCommand** 事件處理。

下表列出 Windows Media Player 自動處理的指令碼命令類型。



| 類型                   | 描述                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | 控制項會在 IWMPClosedCaption 所指定的 HTML 元素中顯示相關聯的文字。**captioningId**。                                                       |
| 事件                  | 控制項會執行針對指定事件所定義的指示。                                                                                                  |
| 檔案名               | 控制項會重設其 **URL** 屬性、嘗試開啟指定的檔案，並立即開始播放新的資料流程。                                        |
| OPENEVENT              | 緩衝相關聯的事件種類命令，以及時執行事件腳本。                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | *Param* 參數包含已同步處理的歌詞文字。 Windows Media Player 會在 [**立即播放**] 功能的 [隱藏式輔助字幕] 區域中顯示歌詞文字。 |
| TEXT                   | 控制項會在 IWMPClosedCaption 所指定的 HTML 元素中顯示相關聯的文字。**captioningId**。                                                       |
| URL                    | 如果 IWMPSettings，控制項會自動開啟使用預設網際網路瀏覽器指定的 URL。**invokeURLs** 屬性設定為 true。                    |



 

只要您提供程式碼來處理命令，您就可以內嵌任何其他類型的命令。 雖然 Windows Media Player 控制項會忽略未知的命令，但是仍會將它們移交給 **ScriptCommand** 事件。

如果以向前快轉或倒轉模式掃描檔案，就不會呼叫 ScriptCommand 事件。

如果 IWMPSettings，則會在您的預設網頁瀏覽器中自動叫用 Windows Media Player 控制項所收到的 URL 命令。**invokeURLs** 屬性設定為 true。 您可以使用 IWMPSettings。**defaultFrame** 屬性，以指定網頁出現的目標框架。

傳送給 Windows Media Player 的 URL 會相對於 IWMPSettings 所指定的基底 url 進行處理。**baseURL** 屬性。 基底 URL 會與相對 URL 串連，以產生完整指定的 URL，該 URL 會以 **ScriptCommand** 事件的命令參數形式傳遞。

Windows Media Player 控制項一律會以下列方式處理傳入的 URL 命令：

1.  收到 URL 類型命令。
2.  IWMPSettings.**baseURL** 是用來從指令碼命令中指定的相對 URL 建立完整的 url。
3.  呼叫 **ScriptCommand** 。
4.  **ScriptCommand** 傳回之後，IWMPSettings。**invokeURLs** 已核取。
5.  如果為 IWMPSettings，則為。**invokeURLs** 為 true，而且命令是 URL 命令，會叫用指定的 url。 如果為 IWMPSettings，則為。**invokeURLs** 為 false，或如果命令不是 URL 命令，則會忽略此命令。

撰寫 Windows 媒體檔案時，您可以在參數欄位中串連兩個符號和框架的名稱，以指定要在其中顯示新 URL 的框架。 下列範例說明一般 **ScriptCommand** 參數。 它會指定必須在 *myframe* 框架中啟動 URL *mypage.aspx* 。


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



如果正在掃描檔案 (快速轉送或倒轉) ，則不會呼叫 ScriptCommand 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. captioningId (VB 和 c # )**](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





