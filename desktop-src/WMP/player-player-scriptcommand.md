---
title: ScriptCommand 事件
description: 收到同步處理的命令或 URL 時，就會發生 ScriptCommand 事件。 |ScriptCommand 事件
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- ScriptCommand 事件 Windows Media Player
- ScriptCommand 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，ScriptCommand 事件
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f54aac54cf56e65b71dbd604d57d5ae9404a0148db139779ced3aa9e0da0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572426"
---
# <a name="playerscriptcommand-event"></a>ScriptCommand 事件

收到同步處理的命令或 URL 時，就會發生 **ScriptCommand** 事件。

## <a name="syntax"></a>語法


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*scType* 
</dt> <dd>

字串，指定指令碼命令的類型。

</dd> <dt>

*參數* 
</dt> <dd>

指定指令碼命令的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

您可以將命令內嵌在 Windows 媒體檔案或資料流程的聲音和影像中。 這些命令是與資料流程中指定時間相關聯的一對 Unicode 字串。 當資料流程到達與命令相關聯的時間時，Windows Media Player 控制項會傳送具有兩個參數的 **ScriptCommand** 事件。 其中一個參數指定要傳送的命令類型，另一個參數則指定命令。 參數的類型是用來決定如何處理命令參數。 任何類型的命令都可以內嵌在檔案或資料流程中，以供 **ScriptCommand** 事件處理。

下表列出 Windows Media Player 自動處理的指令碼命令類型。



| 類型                   | 描述                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | 控制項會在 *ClosedCaption* 所指定的 DIV 中顯示相關聯的文字。**captioningID**。                                                                  |
| 事件                  | 告訴控制項執行針對指定事件所定義的指示。                                                                                          |
| 檔案名               | 控制項會重設其 **URL** 屬性、嘗試開啟指定的檔案，並立即開始播放新的資料流程。                                        |
| OPENEVENT              | 緩衝相關聯的事件種類命令，以及時執行事件腳本。                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | *Param* 參數包含已同步處理的歌詞文字。 Windows Media Player 會在 [**立即播放**] 功能的 [隱藏式輔助字幕] 區域中顯示歌詞文字。 |
| TEXT                   | 控制項會在 *ClosedCaption* 所指定的 DIV 中顯示相關聯的文字。**captioningID**。                                                                  |
| URL                    | 如果 *設定*，控制項會自動開啟使用預設網際網路瀏覽器指定的 URL。**invokeURLs** 屬性設定為 true。                      |



 

只要您提供交互程式碼來處理命令，您就可以內嵌任何其他類型的命令。 雖然 Windows Media Player 控制項會忽略未知的命令，但是仍會將它們移交給 **ScriptCommand** 事件。

如果 *設定*，Windows Media Player 控制項所收到的 URL 命令會在預設網頁瀏覽器中自動叫用。**invokeURLs** 屬性設定為 true。 您可以使用 *設定*。**defaultFrame** 屬性，以指定網頁出現的目標框架。

傳送給 Windows Media Player 的 URL 會相對於 *設定* 所指定的基底 URL 進行處理。**baseURL** 屬性。 基底 URL 會與相對指定的 URL 串連，以產生完整指定的 URL，以 **ScriptCommand** 事件的命令參數形式傳遞。

Windows Media Player 控制項一律會以下列方式處理傳入的 URL 類型命令：

1.  收到 URL 類型命令。
2.  *設定*。**baseURL** 是用來從指令碼命令中指定的相對 URL 建立完整的 url。
3.  呼叫 *ScriptCommand* 。
4.  *ScriptCommand* 傳回之後，*設定*。**invokeURLs** 已核取。
5.  如果 *設定*，則為。**invokeURLs** 為 true，而且命令是 URL 類型，會叫用指定的 url。 如果 *設定*，則為。**invokeURLs** 為 false，或如果命令不是 URL 類型，則會忽略此命令。

撰寫 Windows 媒體檔案時，您可以在參數欄位中串連兩個符號和框架的名稱，以指定要在其中顯示新 URL 的框架。 下列範例說明一般 *ScriptCommand* 參數。 它會指定必須在 *myframe* 框架中啟動 URL *mypage.aspx* 。


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



如果正在掃描檔案 (向前轉送或快速反轉) ，則不會呼叫 ScriptCommand 事件。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**設定. baseURL**](settings-baseurl.md)
</dt> <dt>

[**設定. defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**設定. invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





