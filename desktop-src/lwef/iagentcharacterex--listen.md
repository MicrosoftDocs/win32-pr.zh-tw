---
title: IAgentCharacterEx 接聽
description: IAgentCharacterEx 接聽
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301227"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx：：接聽

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

開啟或關閉語音辨識輸入 () 的接聽模式。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

接聽模式旗標。 如果此參數為 **True**，則會開啟接聽模式;如果 **為 False**，則表示接聽模式為關閉狀態。

</dd> </dl>

將此方法設定為 **True** ，可讓接聽模式 (在一段固定時間內開啟語音辨識) 。 當您無法設定超時值時，您可以在超時時間到期之前關閉接聽模式。 此外，如果已開啟接聽模式，因為您 (或其他用戶端) 成功將方法設為 **True** ，在超時時間到期之前，方法會成功，並重設超時時間。不過，如果已開啟接聽模式，因為使用者按下接聽鍵，方法會成功，但是會忽略超時，而且接聽模式會根據使用者與接聽鍵的互動而結束。

只有當輸入-主動用戶端呼叫這個方法時，此方法才會成功。 因此，如果您的用戶端不是最上層字元的作用中用戶端，方法將會失敗。 如果您嘗試將方法設為 **False** ，且使用者按下接聽鍵，方法也會失敗。 如果沒有相容的語音引擎可符合字元的語言識別項設定，或使用者已使用 Microsoft Agent 屬性工作表停用語音輸入，則也可能會失敗。 不過，若音訊裝置忙碌中，此方法將不會失敗。

當您成功將此方法設定為 **True** 時，伺服器會觸發 [**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md) 事件。 當接聽模式超時時間完成時，或當您將 [**IAgentCharacterEx：：接聽**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**)設為 **False** 時，伺服器也會傳送 **IAgentNotifySinkEx：： ListeningState** 。

這個方法不會自動呼叫 [**IAgentCharacter：： StopAll**](iagentcharacter--stopall.md) ，並且播放當使用者按下接聽鍵時所發生的字元接聽狀態動畫。 這可讓您使用 [**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md) 事件來判斷是否要停止目前的動畫，並播放您自己的適當動畫。 不過，一旦偵測到使用者語句，伺服器就會自動呼叫 **IAgentCharacter：： StopAll** 並播放聽力狀態動畫。

## <a name="see-also"></a>另請參閱

[**IAgentNotifySinkEx：： ListeningState**](iagentnotifysinkex--listeningstate.md)、 [ **IAgentSpeechInputProperties：： GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




