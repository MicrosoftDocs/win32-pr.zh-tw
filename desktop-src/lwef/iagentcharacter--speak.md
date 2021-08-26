---
title: IAgentCharacter 話
description: IAgentCharacter 話
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693b40a00b34173976410391249d3fac1a7f0684e34a6e2ae82afbd8b8169ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014208"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter：：說話

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

說出文字或音效檔。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

字元要說出的文字。

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

要用於語音輸出的音效檔 (或檔案規格) 的 URL。 這可以是標準的音效檔 (。WAV) 或語言增強的音效檔 (。LWV) 。

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

接收 [**說話**](/windows/desktop/lwef/iagentcharacter--speak) 要求識別碼之變數的位址。

</dd> </dl>

若要使用此方法搭配設定為使用文字轉換語音 (TTS) 引擎的字元;只要提供 *bszText* 參數即可。 您可以 \| 在 *bszText* 參數中包含分隔號字元 () 來指定替代字串，如此一來，每當伺服器處理方法時，就會隨機播放不同的字串。 使用 Microsoft Agent 字元編輯器來編譯字元時，會定義 TTS 輸出的支援。

如果您想要使用音效檔輸出作為字元，請在 *bszURL* 參數中指定檔案的位置。 使用 HTTP 通訊協定下載音效檔時，請使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來確保檔案的可用性，然後再使用這個方法。 您可以使用 *bszText* 參數來指定出現在字元之文字批註中的單字。 如果您指定語言增強的音效檔 (。LWV) 針對 *bszURL* 參數，而且不指定文字， *bszText* 參數會使用儲存在檔案中的文字。

[**說話**](/windows/desktop/lwef/iagentcharacter--speak)方法會使用最後播放的動畫來判斷要播放的說話動畫。 例如，如果您在 **說話** 命令之前加上 [**IAgentCharacter：:P**](iagentcharacter--play.md) 配置 "**GestureRight**"，伺服器將會播放 **GestureRight** ，然後再播放 **GestureRight** 說話動畫。 如果播放的最後一個動畫沒有說話動畫，Microsoft Agent 會播放指派給該字元 **說話** 狀態的動畫。

如果您呼叫 [**說話**](/windows/desktop/lwef/iagentcharacter--speak) 且音訊頻道忙碌中，則不會聽到字元的音訊輸出，但文字會顯示在文字提示字元中。 文字氣球的 [Enabled](enabled-property.md) 屬性也必須為 **True** ，才會顯示文字。

Microsoft Agent 自動斷詞字組，使用空白字元來分隔文字 (例如，空格鍵和 tab) 。 不過，它也可能會中斷文字以容納球。 在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。

> [!Note]  
> 先使用 [**IAgentCharacterEx：： SetLanguageID**](iagentcharacterex--setlanguageid.md) 來設定字元的語言 (識別碼，然後再使用 [ [**朗讀**](/windows/desktop/lwef/iagentcharacter--speak) ] 方法，以確保文字氣球內適當的文字顯示。

 

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：:P 的版面**](iagentcharacter--play.md)配置、 [**IAgentBalloon：： GetEnabled**](iagentballoon--getenabled.md)、 [**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)


 

 