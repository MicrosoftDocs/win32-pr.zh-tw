---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966855"
---
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="55456-103">IAgentCommand::SetVoice</span><span class="sxs-lookup"><span data-stu-id="55456-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="55456-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="55456-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="55456-105">設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Voice**](voice-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="55456-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="55456-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="55456-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="55456-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="55456-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="55456-108">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**Voice**](voice-property.md)屬性文字的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="55456-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="55456-109">[**命令**](/windows/desktop/lwef/the-command-object)必須將其 [**Voice**](voice-property.md)屬性和 [**Enabled**](enabled-property.md)屬性設定為可供語音存取。</span><span class="sxs-lookup"><span data-stu-id="55456-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="55456-110">它也必須設定其 [**VoiceCaption**](voicecaption-property.md) 屬性，才會出現在 [ **語音命令] 視窗** 中。</span><span class="sxs-lookup"><span data-stu-id="55456-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="55456-111"> (為了回溯相容性，如果沒有 **VoiceCaption**，則會使用 [**標題**](caption-property.md) 設定。 ) </span><span class="sxs-lookup"><span data-stu-id="55456-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="55456-112">您提供的 BSTR 運算式可以包含方括弧字元 (\[ \]) 表示選擇性的單字和分隔號字元 (\|) 表示替代字串。</span><span class="sxs-lookup"><span data-stu-id="55456-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="55456-113">替代項必須以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="55456-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="55456-114">例如，「 (嗨， \[ 有很高的) 」會 \] \| 告訴語音引擎接受「hello，」或「嗨」的命令。</span><span class="sxs-lookup"><span data-stu-id="55456-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="55456-115">請記得在以括弧或括弧括住的文字與不在方括弧或括弧內的文字之間包含適當的空格。</span><span class="sxs-lookup"><span data-stu-id="55456-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="55456-116">您可以使用星狀 (\*) 運算子來指定包含在群組中之單字的零或多個實例，或使用加號 (+) 運算子來指定一個或多個實例。</span><span class="sxs-lookup"><span data-stu-id="55456-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="55456-117">例如，下列程式會產生支援「嘗試此項」、「請嘗試這項」和「請嘗試這項」的文法，但不限反覆運算「請」：</span><span class="sxs-lookup"><span data-stu-id="55456-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="55456-118">下列文法格式排除「試試這個」，因為 + 運算子至少定義了一個「請」實例：</span><span class="sxs-lookup"><span data-stu-id="55456-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="55456-119">重複運算子會遵循一般的優先順序規則，並套用至緊接在前面的文字專案。</span><span class="sxs-lookup"><span data-stu-id="55456-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="55456-120">例如，下列文法會產生 "紐約" 和 "紐約"，但不會產生 "紐約紐約"：</span><span class="sxs-lookup"><span data-stu-id="55456-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="55456-121">因此，您通常會想要搭配使用這些運算子與群組字元。</span><span class="sxs-lookup"><span data-stu-id="55456-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="55456-122">例如，下列文法包含 "紐約" 和 "紐約紐約"：</span><span class="sxs-lookup"><span data-stu-id="55456-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="55456-123">當您想要撰寫包含重複順序的文法時（例如電話號碼或專案清單的規格），重複運算子會很有用：</span><span class="sxs-lookup"><span data-stu-id="55456-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="55456-124">雖然運算子也可以與方括弧一起使用 (選擇性的群組字元) ，但這麼做可能會降低代理程式處理文法的效率。</span><span class="sxs-lookup"><span data-stu-id="55456-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="55456-125">您也可以使用省略號 ( ... ) 來支援 *word 找出*，也就是告訴語音辨識引擎忽略在片語中這個位置所說出的單字 (有時也稱為 *垃圾* 字) 。</span><span class="sxs-lookup"><span data-stu-id="55456-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="55456-126">因此，不論是以連續的單字或片語說出，語音引擎都只會辨識字串中的特定字組。</span><span class="sxs-lookup"><span data-stu-id="55456-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="55456-127">例如，如果您將此屬性設定為 " \[ ... \] 檢查郵件 \[ ...」 \] 語音辨識引擎會比對像是「請檢查郵件」或「檢查 mail 請」這項命令的片語。</span><span class="sxs-lookup"><span data-stu-id="55456-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="55456-128">省略號可以用在字串內的任何位置。</span><span class="sxs-lookup"><span data-stu-id="55456-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="55456-129">不過，請小心使用這項技術，因為具有省略號的聲音設定可能會增加不必要相符專案的可能性。</span><span class="sxs-lookup"><span data-stu-id="55456-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="55456-130">定義命令的單字和文法時，請務必至少包含一個必要的單字;也就是說，請避免只提供選擇性的字組。</span><span class="sxs-lookup"><span data-stu-id="55456-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="55456-131">此外，請確定單字只包含發音單字和字母。</span><span class="sxs-lookup"><span data-stu-id="55456-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="55456-132">如果是數位，最好是將單字拼寫出來，而不是使用數值標記法。</span><span class="sxs-lookup"><span data-stu-id="55456-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="55456-133">此外，請省略任何標點符號或符號。</span><span class="sxs-lookup"><span data-stu-id="55456-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="55456-134">例如，請 \# 使用「數位 1 10 元比薩」，而不是「$1 10 比薩」。</span><span class="sxs-lookup"><span data-stu-id="55456-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="55456-135">針對某個命令包含非發音的字元或符號，可能會導致語音引擎無法編譯所有命令的文法。</span><span class="sxs-lookup"><span data-stu-id="55456-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="55456-136">最後，從您所定義的其他語音命令盡可能讓您的語音參數盡可能不同。</span><span class="sxs-lookup"><span data-stu-id="55456-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="55456-137">命令的語音文法越相似，語音引擎就越可能提出辨識錯誤。</span><span class="sxs-lookup"><span data-stu-id="55456-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="55456-138">您也可以使用信賴分數，更清楚地區分兩個可能具有類似或類似發音語音文法的命令。</span><span class="sxs-lookup"><span data-stu-id="55456-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="55456-139">設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Voice**](voice-property.md)屬性會自動啟用代理程式的語音服務，讓接聽鍵和接聽提示可供使用。</span><span class="sxs-lookup"><span data-stu-id="55456-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="55456-140">不過，它不會載入語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="55456-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="55456-141">可用的文法功能可能取決於語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="55456-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="55456-142">您可能會想要檢查引擎的廠商，以判斷支援哪些文法選項。</span><span class="sxs-lookup"><span data-stu-id="55456-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="55456-143">使用 [**IAgentCharacterEx：： SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) 來指定引擎。</span><span class="sxs-lookup"><span data-stu-id="55456-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="55456-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55456-144">See Also</span></span>

<span data-ttu-id="55456-145">[**IAgentCommand：： GetVoice**](iagentcommand--getvoice.md)、 [**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="55456-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 