---
title: IAgentCommands SetVoice
description: IAgentCommands SetVoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a8e29936dbca65ffded5f8a5e5ea5297b28362e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463017"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands::SetVoice

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**語音**](voice-property.md)文字屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合之 [**Voice**](voice-property.md) TEXT 屬性值的 BSTR。

</dd> </dl>

[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**語音**](voice-property.md)文字屬性必須設定為可供語音存取。 它也必須將其 [ [**VoiceCaption**](voicecaption-property.md) ] 或 [ [**標題**](caption-property.md) ] 屬性設定為出現在 [語音命令] 視窗中，並將其 [ [**可見**](visible-property.md) ] 屬性設定為 [ **True** ]，才會出現在字元的快顯功能表上。

您提供的 BSTR 運算式可以包含方括弧字元 (\[ \]) 表示選擇性的單字和分隔號字元 (\|) 表示替代字串。 替代項必須以括弧括住。 例如，「 (嗨， \[ 有很高的) 」會 \] \| 告訴語音引擎接受「hello，」或「嗨」的命令。 請記得在您包含括弧或括弧中的單字與其他文字之間包含適當的空格。 請記得在以括弧或括弧括住的文字與不在方括弧或括弧內的文字之間包含適當的空格。

您可以使用星狀 (\*) 運算子來指定包含在群組中之單字的零或多個實例，或使用加號 (+) 運算子來指定一個或多個實例。 例如，下列程式會產生支援「嘗試此項」、「請嘗試這項」和「請嘗試這項」的文法，但不限反覆運算「請」：

``` syntax
   "please* try this"
```

下列文法格式排除「試試這個」，因為 + 運算子至少定義了一個「請」實例：

``` syntax
   "please+ try this"
```

重複運算子會遵循一般的優先順序規則，並套用至緊接在前面的文字專案。 例如，下列文法會產生 "紐約" 和 "紐約"，但不會產生 "紐約紐約"：

``` syntax
   "New York+"
```

因此，您通常會想要搭配使用這些運算子與群組字元。 例如，下列文法包含 "紐約" 和 "紐約紐約"：

``` syntax
   "(New York)+"
```

當您想要撰寫包含重複順序的文法時（例如電話號碼或專案清單的規格），重複運算子會很有用：

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

雖然運算子也可以搭配方括弧使用 (選擇性的分組字元) ，但這麼做可能會降低代理程式處理文法的效率。

您也可以使用省略號 ( ... ) 來支援 *word 找出*，也就是告訴語音辨識引擎忽略在片語中這個位置所說出的單字 (有時也稱為 *垃圾* 字) 。 當您使用省略號時，無論是以連續的單字或片語說出時，語音引擎都會辨識字串中的特定字組。 例如，如果您將此屬性設定為 " \[ ... \] 檢查郵件 \[ ...」 \] 語音辨識引擎會比對像是「請檢查郵件」或「檢查 mail 請」這項命令的片語。 省略號可以用在字串內的任何位置。 不過，請小心使用這項技術，因為具有省略號的語音設定可能會增加不必要相符專案的可能性。

定義命令的單字和文法時，請至少包含一個必要的單字;也就是說，請避免只提供選擇性的字組。 此外，請確定單字只包含發音單字和字母。 如果是數位，最好是將單字拼寫出來，而不是使用不明確的標記法。 例如，"345" 不是很好的文法形式。 同樣地，請使用 "I 三重 E" 來取代 "IEEE"。 此外，請省略任何標點符號或符號。 例如，請 \# 使用「數位 1 10 元比薩」，而不是「$1 10 比薩」。 針對某個命令包含非發音的字元或符號，可能會導致語音引擎無法編譯所有命令的文法。 最後，從您所定義的其他語音命令盡可能讓您的語音參數盡可能不同。 命令的語音文法越相似，語音引擎就越可能提出辨識錯誤。 您也可以使用信賴分數，更清楚地區分兩個可能具有類似或類似發音語音文法的命令。

您可以用「*文字 \\ 發音*」形式包含文法文字，其中 "text" 是顯示的文字，而 "發音" 是說明發音的文字。 例如，當使用者說「第一次」時，會辨識文法「第1個」， \\ 但是 [**命令**](/windows/desktop/lwef/the-command-object) 事件會傳回「第1個」文字 \\ 。 您也可以使用 IPA (國際注音字母) 來指定發音，方法是以井字型大小字元開頭的發音 ( " \# " ) ，然後是代表 IPA 發音的文字。

若為日文語音辨識引擎，您可以用 "*假名 \\ 漢字*" 格式來定義文法，以減少替代發音並提高精確度。  (反轉順序的目的是為了回溯相容性。 ) 這對日文漢字中正確名稱的發音特別重要。 不過，您可以在不含假名的情況下傳遞「漢字」，在這種情況下，引擎應接聽所有可接受的漢字發音。 您也可以只傳入假名。

除了使用分組或重複格式化字元的錯誤之外，除非引擎本身回報錯誤，否則 Microsoft Agent 不會在您的文法中報告錯誤。 如果您在文法中傳遞無法編譯引擎的文字，但是引擎不會處理並傳回做為錯誤，代理程式就無法回報錯誤。 因此，用戶端應用程式必須小心定義 [**Voice**](voice-property.md) 屬性的文法。

> [!Note]  
> 可用的文法功能可能取決於語音辨識引擎。 您可能會想要檢查引擎的廠商，以判斷支援哪些文法選項。 使用 [**SRModeID**](srmodeid-property.md) 來使用特定的引擎。

 

這個屬性的操作取決於 Microsoft 代理程式伺服器的語音辨識狀態的狀態。 例如，如果已停用或未安裝語音辨識，此函式就不會立即生效。 但是，如果在會話期間啟用語音辨識，則當其用戶端應用程式為輸入-主動時，命令就會變成可存取。

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： GetVoice**](iagentcommands--getvoice.md)、 [**IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)、 [**IAgentCommands：： SetVisible**](iagentcommands--setvisible.md)


 

 