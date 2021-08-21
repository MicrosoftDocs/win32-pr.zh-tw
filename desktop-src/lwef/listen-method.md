---
title: 接聽方法
description: 接聽方法
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc87a57d1ebdd3f36a2d56d85e0754f5005fd6c356fc9af98760bd0db90605f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748658"
---
# <a name="listen-method"></a>接聽方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

開啟接聽模式 (語音辨識在一段時間內) 。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 * * * * ( "**_CharacterID_*_" ) 。接聽_ *  *狀態*



| 部分    | 描述                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | 必要。 判斷要開啟或關閉接聽模式的布林值。 **True** 開啟接聽模式。 <br/> **False** 關閉接聽模式。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

將此方法設為 **True** 可啟用接聽模式 (在一段固定時間內開啟語音辨識)  (10 秒) 。 當您無法設定超時值時，您可以在超時時間到期之前關閉接聽模式。 如果您 (或其他用戶端) 成功設定接聽模式，而您嘗試在到期前將此屬性設定為 **True** ，則方法會成功，並重設超時時間。但是，如果接聽模式因為使用者按下接聽鍵而開啟，方法會成功，但是會忽略超時，而且接聽模式會根據使用者與接聽鍵的互動而結束。

只有當輸入-主動用戶端呼叫，且已啟動語音服務時，此方法才會成功。 若要確保語音服務已啟動，請查詢或設定 [**SRModeID**](srmodeid-property.md) ，或在您呼叫 **接聽** 之前設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**語音**](voice-property.md)設定，否則方法將會失敗。 若要偵測這個方法是否成功，請呼叫它作為函式，它會傳回布林值，指出方法是否成功。


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



如果使用者按下接聽鍵，而您嘗試將 **聆聽** 設定為 **False**，則此方法也會失敗。 不過，如果使用者已發行接聽金鑰，且接聽模式尚未超時，則會成功。

如果沒有相容的語音引擎可符合字元的 [**LanguageID**](languageid-property.md)設定、使用者已使用 Microsoft Agent 屬性工作表停用語音輸入，或是音訊裝置忙碌中，則 **接聽** 也會失敗。

當您成功將此方法設定為 **True** 時，伺服器會觸發 [**ListenStart**](listenstart-event.md) 事件。 當接聽模式超時時間完成或您將 [**接聽**] 設定為 [ **False**] 時，伺服器就會傳送 [**ListenComplete**](listencomplete-event.md) 。

當按下接聽鍵時，此方法不會自動呼叫 [**Stop**](stop-method.md) 並播放接聽狀態動畫。 這可讓您藉由呼叫「**停止**」並播放自己的適當動畫，判斷是否要使用 [**ListenStart**](listenstart-event.md)動畫來中斷目前的動畫。 但是，當偵測到使用者語句時，伺服器會呼叫 **Stop** 並播放聽力狀態動畫。

## <a name="see-also"></a>另請參閱

[**LanguageID 屬性**](languageid-property.md)、 [**ListenComplete 事件**](listencomplete-event.md)、 [**ListenStart 事件**](listenstart-event.md)


 

