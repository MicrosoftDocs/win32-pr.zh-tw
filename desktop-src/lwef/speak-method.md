---
title: 說話方法
description: 說話方法
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8798809dc4cdfa38438bee2fa9449f879871e4018b0e6b046d95a73583b03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475340"
---
# <a name="speak-method"></a>說話方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

為指定的字元說出指定的文字或音效檔。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。說_ 出 *  \[ *文字* \] ， \[ *Url*\]



| 部分   | 描述                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | 選擇性。 字串，指定字元所顯示的內容。                                                                                                                                                                                                   |
| *Url*  | 選擇性。 字串運算式，指定音訊檔 ( 的位置。WAV 或。) 的 LWV 格式。 您可以將位置指定為檔案 (包括 UNC 路徑規格) 或 URL (當字元動畫資料也透過 HTTP 通訊協定) 進行抓取時。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

雖然 *Text* 和 *Url* 參數是選擇性的，但必須提供其中一個。 若要使用這個方法，並將字元設定為只在其文字提示字元中說話，或使用文字轉換語音 (TTS) 引擎，只要提供 *text* 參數即可。 請在單字之間加上空格，以在文字氣球中定義適當的斷字元號，即使通常不包含空格的語言也是如此。

您也可以 \| 在 *Text* 參數中包含分隔號字元 () 來指定替代字串，讓伺服器在每次處理方法時隨機播放不同的字串。

使用 Microsoft Agent 字元編輯器編譯字元時，會定義 TTS 輸出的字元支援。 若要產生 TTS 輸出，必須先安裝相容的 TTS 引擎，才能呼叫這個方法。 如需詳細資訊，請參閱 [存取語音服務](accessing-speech-services.md)。

如果您使用錄製的音效檔 (。WAV 或。LWV 格式：只) 字元的輸出，請在 *Url* 參數中指定檔案的位置。 此檔案規格可以包含本機 (絕對或相對) 或通用命名慣例 (UNC) 路徑。 檔案名不能包含美國字碼頁1252中未包含的任何字元。 但是，如果您使用 HTTP 通訊協定來存取字元動畫資料，請使用 [**Get**](get-method.md) 方法來載入動畫，然後再呼叫 **說話** 方法。 如需創意的詳細資訊，請參閱 [使用 Microsoft 語言資訊音效編輯工具](using-the-microsoft-linguistic-information-sound-editing-tool.md) 。LWV 檔案。

當您使用錄製的音效檔案輸出時，仍然可以使用 *Text* 參數來指定出現在字元之文字批註中的單字。 但是，如果您指定語言增強的音效檔 (。LWV *Url* 參數的) ，而不指定文字給文字提示，則 *text* 參數會使用儲存在檔案中的文字。

您也可以使用包含在 *文字* 參數中的特殊標籤，來改變語音輸出的參數。 如需詳細資訊，請參閱 [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md)。

如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。 您可以使用這個來同步處理常式代碼的其他部分與字元的語音輸出，如下列範例所示：


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



您也可以使用 [**要求**](/windows/desktop/lwef/the-request-object) 物件來檢查特定的錯誤狀況。 例如，如果您使用「 **說話** 」方法來說出但未安裝相容的 TTS 引擎，則伺服器會將 **要求** 物件的 [**Status**](status-property.md) 屬性設為「失敗」，並將其 [**Description**](description-property.md) 屬性設定為「類別未註冊」或「未知或物件傳回的錯誤」。 若要判斷是否已安裝 TTS 引擎，請使用 [**TTSModeID**](ttsmodeid-property.md) 屬性。

同樣地，如果您有嘗試說出音效檔的字元，而且檔案尚未載入或音訊裝置有問題，則伺服器也會將 [**要求**](/windows/desktop/lwef/the-request-object) 物件的 [**Status**](status-property.md) 屬性設為「失敗」，並提供適當的錯誤碼號碼。

您也可以在說出的文字中包含書簽聲控標籤，以同步處理您的程式碼：


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



如需書簽聲控標籤的詳細資訊，請參閱 [語音輸出標記](mrk-tag.md)。

**說話** 方法會使用最後播放的動作來判斷要播放的說話動畫。 例如，如果您在「**說話**」命令前面加上「**GestureRight**」，伺服器將會播放 **GestureRight** ，然後 [**再播放**](play-method.md) **GestureRight** 說話動畫。 如果播放的最後一個動畫沒有說話動畫，則代理程式會播放指派給字元 **說話** 狀態的動畫。

如果您呼叫 **說話** 且音訊頻道忙碌中，則不會聽到字元的音訊輸出，但文字會顯示在文字提示字元中。

代理程式自動斷詞字提示字元會中斷使用空白字元的單字 (例如，空格鍵或 Tab) 。 但是，如果無法使用，它可能會中斷文字以符合氣球。 在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。

> [!Note]  
> 文字氣球的 [**Enabled**](enabled-property.md) 屬性也必須為 **True** ，才能顯示文字。

 

> [!Note]  
> 設定字元的語言識別項 (，方法是在使用 [**朗讀**] 方法之前，先設定字元的 **LanguageID** ，以確保文字氣球內適當的文字顯示。

 

## <a name="see-also"></a>另請參閱

[**Bookmark 事件**](bookmark-event.md)、 [**RequestStart 事件**](requeststart-event.md)、 [**RequestComplete 事件**](requestcomplete-event.md)


 

 