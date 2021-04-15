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
# <a name="iagentcommandssetvoice"></a><span data-ttu-id="d8e24-103">IAgentCommands::SetVoice</span><span class="sxs-lookup"><span data-stu-id="d8e24-103">IAgentCommands::SetVoice</span></span>

<span data-ttu-id="d8e24-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d8e24-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

<span data-ttu-id="d8e24-105">設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**語音**](voice-property.md)文字屬性。</span><span class="sxs-lookup"><span data-stu-id="d8e24-105">Sets the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="d8e24-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="d8e24-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d8e24-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="d8e24-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="d8e24-108">指定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合之 [**Voice**](voice-property.md) TEXT 屬性值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="d8e24-108">A BSTR that specifies the value for the [**Voice**](voice-property.md) text property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="d8e24-109">[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**語音**](voice-property.md)文字屬性必須設定為可供語音存取。</span><span class="sxs-lookup"><span data-stu-id="d8e24-109">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Voice**](voice-property.md) text property set to be voice-accessible.</span></span> <span data-ttu-id="d8e24-110">它也必須將其 [ [**VoiceCaption**](voicecaption-property.md) ] 或 [ [**標題**](caption-property.md) ] 屬性設定為出現在 [語音命令] 視窗中，並將其 [ [**可見**](visible-property.md) ] 屬性設定為 [ **True** ]，才會出現在字元的快顯功能表上。</span><span class="sxs-lookup"><span data-stu-id="d8e24-110">It also must have its [**VoiceCaption**](voicecaption-property.md) or [**Caption**](caption-property.md) property set to appear in the Voice Commands Window and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span>

<span data-ttu-id="d8e24-111">您提供的 BSTR 運算式可以包含方括弧字元 (\[ \]) 表示選擇性的單字和分隔號字元 (\|) 表示替代字串。</span><span class="sxs-lookup"><span data-stu-id="d8e24-111">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="d8e24-112">替代項必須以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="d8e24-112">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="d8e24-113">例如，「 (嗨， \[ 有很高的) 」會 \] \| 告訴語音引擎接受「hello，」或「嗨」的命令。</span><span class="sxs-lookup"><span data-stu-id="d8e24-113">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="d8e24-114">請記得在您包含括弧或括弧中的單字與其他文字之間包含適當的空格。</span><span class="sxs-lookup"><span data-stu-id="d8e24-114">Remember to include appropriate spaces between words you include in brackets or parentheses as well as other text.</span></span> <span data-ttu-id="d8e24-115">請記得在以括弧或括弧括住的文字與不在方括弧或括弧內的文字之間包含適當的空格。</span><span class="sxs-lookup"><span data-stu-id="d8e24-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="d8e24-116">您可以使用星狀 (\*) 運算子來指定包含在群組中之單字的零或多個實例，或使用加號 (+) 運算子來指定一個或多個實例。</span><span class="sxs-lookup"><span data-stu-id="d8e24-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="d8e24-117">例如，下列程式會產生支援「嘗試此項」、「請嘗試這項」和「請嘗試這項」的文法，但不限反覆運算「請」：</span><span class="sxs-lookup"><span data-stu-id="d8e24-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="d8e24-118">下列文法格式排除「試試這個」，因為 + 運算子至少定義了一個「請」實例：</span><span class="sxs-lookup"><span data-stu-id="d8e24-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="d8e24-119">重複運算子會遵循一般的優先順序規則，並套用至緊接在前面的文字專案。</span><span class="sxs-lookup"><span data-stu-id="d8e24-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="d8e24-120">例如，下列文法會產生 "紐約" 和 "紐約"，但不會產生 "紐約紐約"：</span><span class="sxs-lookup"><span data-stu-id="d8e24-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="d8e24-121">因此，您通常會想要搭配使用這些運算子與群組字元。</span><span class="sxs-lookup"><span data-stu-id="d8e24-121">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="d8e24-122">例如，下列文法包含 "紐約" 和 "紐約紐約"：</span><span class="sxs-lookup"><span data-stu-id="d8e24-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="d8e24-123">當您想要撰寫包含重複順序的文法時（例如電話號碼或專案清單的規格），重複運算子會很有用：</span><span class="sxs-lookup"><span data-stu-id="d8e24-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="d8e24-124">雖然運算子也可以搭配方括弧使用 (選擇性的分組字元) ，但這麼做可能會降低代理程式處理文法的效率。</span><span class="sxs-lookup"><span data-stu-id="d8e24-124">Although the operators can also be used with square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="d8e24-125">您也可以使用省略號 ( ... ) 來支援 *word 找出*，也就是告訴語音辨識引擎忽略在片語中這個位置所說出的單字 (有時也稱為 *垃圾* 字) 。</span><span class="sxs-lookup"><span data-stu-id="d8e24-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="d8e24-126">當您使用省略號時，無論是以連續的單字或片語說出時，語音引擎都會辨識字串中的特定字組。</span><span class="sxs-lookup"><span data-stu-id="d8e24-126">When you use ellipses, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="d8e24-127">例如，如果您將此屬性設定為 " \[ ... \] 檢查郵件 \[ ...」 \] 語音辨識引擎會比對像是「請檢查郵件」或「檢查 mail 請」這項命令的片語。</span><span class="sxs-lookup"><span data-stu-id="d8e24-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="d8e24-128">省略號可以用在字串內的任何位置。</span><span class="sxs-lookup"><span data-stu-id="d8e24-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="d8e24-129">不過，請小心使用這項技術，因為具有省略號的語音設定可能會增加不必要相符專案的可能性。</span><span class="sxs-lookup"><span data-stu-id="d8e24-129">However, be careful using this technique as voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="d8e24-130">定義命令的單字和文法時，請至少包含一個必要的單字;也就是說，請避免只提供選擇性的字組。</span><span class="sxs-lookup"><span data-stu-id="d8e24-130">When defining the words and grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="d8e24-131">此外，請確定單字只包含發音單字和字母。</span><span class="sxs-lookup"><span data-stu-id="d8e24-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="d8e24-132">如果是數位，最好是將單字拼寫出來，而不是使用不明確的標記法。</span><span class="sxs-lookup"><span data-stu-id="d8e24-132">For numbers, it is better to spell out the word rather than use an ambiguous representation.</span></span> <span data-ttu-id="d8e24-133">例如，"345" 不是很好的文法形式。</span><span class="sxs-lookup"><span data-stu-id="d8e24-133">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="d8e24-134">同樣地，請使用 "I 三重 E" 來取代 "IEEE"。</span><span class="sxs-lookup"><span data-stu-id="d8e24-134">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="d8e24-135">此外，請省略任何標點符號或符號。</span><span class="sxs-lookup"><span data-stu-id="d8e24-135">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="d8e24-136">例如，請 \# 使用「數位 1 10 元比薩」，而不是「$1 10 比薩」。</span><span class="sxs-lookup"><span data-stu-id="d8e24-136">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="d8e24-137">針對某個命令包含非發音的字元或符號，可能會導致語音引擎無法編譯所有命令的文法。</span><span class="sxs-lookup"><span data-stu-id="d8e24-137">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="d8e24-138">最後，從您所定義的其他語音命令盡可能讓您的語音參數盡可能不同。</span><span class="sxs-lookup"><span data-stu-id="d8e24-138">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="d8e24-139">命令的語音文法越相似，語音引擎就越可能提出辨識錯誤。</span><span class="sxs-lookup"><span data-stu-id="d8e24-139">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="d8e24-140">您也可以使用信賴分數，更清楚地區分兩個可能具有類似或類似發音語音文法的命令。</span><span class="sxs-lookup"><span data-stu-id="d8e24-140">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="d8e24-141">您可以用「*文字 \\ 發音*」形式包含文法文字，其中 "text" 是顯示的文字，而 "發音" 是說明發音的文字。</span><span class="sxs-lookup"><span data-stu-id="d8e24-141">You can include in your grammar words in the form of "*text\\pronunciation*", where "text" is the text displayed and "pronunciation" is text that clarifies the pronunciation.</span></span> <span data-ttu-id="d8e24-142">例如，當使用者說「第一次」時，會辨識文法「第1個」， \\ 但是 [**命令**](/windows/desktop/lwef/the-command-object) 事件會傳回「第1個」文字 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d8e24-142">For example, the grammar, "1st\\first", would be recognized when the user says "first," but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="d8e24-143">您也可以使用 IPA (國際注音字母) 來指定發音，方法是以井字型大小字元開頭的發音 ( " \# " ) ，然後是代表 IPA 發音的文字。</span><span class="sxs-lookup"><span data-stu-id="d8e24-143">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound-sign character ("\#"), then the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="d8e24-144">若為日文語音辨識引擎，您可以用 "*假名 \\ 漢字*" 格式來定義文法，以減少替代發音並提高精確度。</span><span class="sxs-lookup"><span data-stu-id="d8e24-144">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*," reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="d8e24-145"> (反轉順序的目的是為了回溯相容性。 ) 這對日文漢字中正確名稱的發音特別重要。</span><span class="sxs-lookup"><span data-stu-id="d8e24-145">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="d8e24-146">不過，您可以在不含假名的情況下傳遞「漢字」，在這種情況下，引擎應接聽所有可接受的漢字發音。</span><span class="sxs-lookup"><span data-stu-id="d8e24-146">However, you can just pass in "kanji," without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="d8e24-147">您也可以只傳入假名。</span><span class="sxs-lookup"><span data-stu-id="d8e24-147">You can also pass in just Kana.</span></span>

<span data-ttu-id="d8e24-148">除了使用分組或重複格式化字元的錯誤之外，除非引擎本身回報錯誤，否則 Microsoft Agent 不會在您的文法中報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="d8e24-148">Except for errors using the grouping or repetition formatting characters, Microsoft Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="d8e24-149">如果您在文法中傳遞無法編譯引擎的文字，但是引擎不會處理並傳回做為錯誤，代理程式就無法回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="d8e24-149">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="d8e24-150">因此，用戶端應用程式必須小心定義 [**Voice**](voice-property.md) 屬性的文法。</span><span class="sxs-lookup"><span data-stu-id="d8e24-150">Therefore, the client application must be careful defining the grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="d8e24-151">可用的文法功能可能取決於語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="d8e24-151">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="d8e24-152">您可能會想要檢查引擎的廠商，以判斷支援哪些文法選項。</span><span class="sxs-lookup"><span data-stu-id="d8e24-152">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="d8e24-153">使用 [**SRModeID**](srmodeid-property.md) 來使用特定的引擎。</span><span class="sxs-lookup"><span data-stu-id="d8e24-153">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="d8e24-154">這個屬性的操作取決於 Microsoft 代理程式伺服器的語音辨識狀態的狀態。</span><span class="sxs-lookup"><span data-stu-id="d8e24-154">The operation of this property depends on the state of Microsoft Agent server's speech recognition state.</span></span> <span data-ttu-id="d8e24-155">例如，如果已停用或未安裝語音辨識，此函式就不會立即生效。</span><span class="sxs-lookup"><span data-stu-id="d8e24-155">For example, if speech recognition is disabled or not installed, this function has no immediate effect.</span></span> <span data-ttu-id="d8e24-156">但是，如果在會話期間啟用語音辨識，則當其用戶端應用程式為輸入-主動時，命令就會變成可存取。</span><span class="sxs-lookup"><span data-stu-id="d8e24-156">If speech recognition is enabled during a session, however, the command will become accessible when its client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8e24-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8e24-157">See Also</span></span>

<span data-ttu-id="d8e24-158">[**IAgentCommands：： GetVoice**](iagentcommands--getvoice.md)、 [**IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)、 [**IAgentCommands：： SetVisible**](iagentcommands--setvisible.md)</span><span class="sxs-lookup"><span data-stu-id="d8e24-158">[**IAgentCommands::GetVoice**](iagentcommands--getvoice.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md)</span></span>


 

 