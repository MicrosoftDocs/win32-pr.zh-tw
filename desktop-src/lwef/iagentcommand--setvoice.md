---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45af753dea18e9fda7b613e3b800ac886d949eb6494fd969cd8b7ceb488dfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477238"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand::SetVoice

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Voice**](voice-property.md)屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**Voice**](voice-property.md)屬性文字的 BSTR。

</dd> </dl>

[**命令**](/windows/desktop/lwef/the-command-object)必須將其 [**Voice**](voice-property.md)屬性和 [**Enabled**](enabled-property.md)屬性設定為可供語音存取。 它也必須設定其 [**VoiceCaption**](voicecaption-property.md) 屬性，才會出現在 [ **語音命令] 視窗** 中。  (為了回溯相容性，如果沒有 **VoiceCaption**，則會使用 [**標題**](caption-property.md) 設定。 ) 

您提供的 BSTR 運算式可以包含方括弧字元 (\[ \]) 表示選擇性的單字和分隔號字元 (\|) 表示替代字串。 替代項必須以括弧括住。 例如，「 (嗨， \[ 有很高的) 」會 \] \| 告訴語音引擎接受「hello，」或「嗨」的命令。 請記得在以括弧或括弧括住的文字與不在方括弧或括弧內的文字之間包含適當的空格。

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

雖然運算子也可以與方括弧一起使用 (選擇性的群組字元) ，但這麼做可能會降低代理程式處理文法的效率。

您也可以使用省略號 ( ... ) 來支援 *word 找出*，也就是告訴語音辨識引擎忽略在片語中這個位置所說出的單字 (有時也稱為 *垃圾* 字) 。 因此，不論是以連續的單字或片語說出，語音引擎都只會辨識字串中的特定字組。 例如，如果您將此屬性設定為 " \[ ... \] 檢查郵件 \[ ...」 \] 語音辨識引擎會比對像是「請檢查郵件」或「檢查 mail 請」這項命令的片語。 省略號可以用在字串內的任何位置。 不過，請小心使用這項技術，因為具有省略號的聲音設定可能會增加不必要相符專案的可能性。

定義命令的單字和文法時，請務必至少包含一個必要的單字;也就是說，請避免只提供選擇性的字組。 此外，請確定單字只包含發音單字和字母。 如果是數位，最好是將單字拼寫出來，而不是使用數值標記法。 此外，請省略任何標點符號或符號。 例如，請 \# 使用「數位 1 10 元比薩」，而不是「$1 10 比薩」。 針對某個命令包含非發音的字元或符號，可能會導致語音引擎無法編譯所有命令的文法。 最後，從您所定義的其他語音命令盡可能讓您的語音參數盡可能不同。 命令的語音文法越相似，語音引擎就越可能提出辨識錯誤。 您也可以使用信賴分數，更清楚地區分兩個可能具有類似或類似發音語音文法的命令。

設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Voice**](voice-property.md)屬性會自動啟用代理程式的語音服務，讓接聽鍵和接聽提示可供使用。 不過，它不會載入語音辨識引擎。

> [!Note]  
> 可用的文法功能可能取決於語音辨識引擎。 您可能會想要檢查引擎的廠商，以判斷支援哪些文法選項。 使用 [**IAgentCharacterEx：： SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) 來指定引擎。

 

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： GetVoice**](iagentcommand--getvoice.md)、 [**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 