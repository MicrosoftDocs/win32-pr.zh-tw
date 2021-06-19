---
title: 'Voice 屬性 (命令物件) '
description: 瞭解命令物件的 Voice 屬性，此屬性會傳回或設定傳遞至語音引擎文法 (的文字以進行辨識) 。
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7403075d8ec0b2d16c66130fc9534edf4fc391df
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396153"
---
# <a name="voice-property-commands-object"></a><span data-ttu-id="3fb79-103">Voice 屬性 (命令物件) </span><span class="sxs-lookup"><span data-stu-id="3fb79-103">Voice Property (Commands Object)</span></span>

<span data-ttu-id="3fb79-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3fb79-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3fb79-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="3fb79-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3fb79-106">傳回或設定傳遞至語音引擎文法 (的文字，以進行辨識) 。</span><span class="sxs-lookup"><span data-stu-id="3fb79-106">Returns or sets the text that is passed to the speech engine grammar (for recognition).</span></span>

</dd> <dt>

<span data-ttu-id="3fb79-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="3fb79-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3fb79-108">\*代理程式 \***。字元 ( "**_CharacterID_\*_" ) 命令。聲音_ \*  \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="3fb79-108">*agent\***.Characters ("**_CharacterID_*_").Commands.Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="3fb79-109">部分</span><span class="sxs-lookup"><span data-stu-id="3fb79-109">Part</span></span>     | <span data-ttu-id="3fb79-110">描述</span><span class="sxs-lookup"><span data-stu-id="3fb79-110">Description</span></span>                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb79-111">*string*</span><span class="sxs-lookup"><span data-stu-id="3fb79-111">*string*</span></span> | <span data-ttu-id="3fb79-112">字串運算式，對應至語音引擎用來辨識此命令的單字或片語。</span><span class="sxs-lookup"><span data-stu-id="3fb79-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fb79-113">備註</span><span class="sxs-lookup"><span data-stu-id="3fb79-113">Remarks</span></span>

<span data-ttu-id="3fb79-114">如果您未提供此參數，[**命令**](/windows/desktop/lwef/the-commands-collection-object)物件的 [**VoiceCaption**](voicecaption-property.md)將不會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="3fb79-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span>

<span data-ttu-id="3fb79-115">您提供的字串運算式可以包含方括弧字元 (\[ \]) 表示選擇性的單字和分隔號字元 (\|) 表示替代字串。</span><span class="sxs-lookup"><span data-stu-id="3fb79-115">The string expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="3fb79-116">替代項必須以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="3fb79-116">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="3fb79-117">例如，「 (嗨， \[ 有很高的) 」會 \] \| 告訴語音引擎接受「hello，」或「嗨」的命令。</span><span class="sxs-lookup"><span data-stu-id="3fb79-117">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="3fb79-118">請記得在以括弧或括弧括住的文字與不在方括弧或括弧內的文字之間包含適當的空格。</span><span class="sxs-lookup"><span data-stu-id="3fb79-118">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span> <span data-ttu-id="3fb79-119">您可以使用星狀 (\*) 運算子來指定包含在群組中之單字的零或多個實例，或使用加號 (+) 運算子來指定一個或多個實例。</span><span class="sxs-lookup"><span data-stu-id="3fb79-119">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="3fb79-120">例如，下列結果會產生支援「試試這個」、「請嘗試這項」、「請試著」、無限制反覆運算的「請」：</span><span class="sxs-lookup"><span data-stu-id="3fb79-120">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="3fb79-121">下列文法格式排除「試試這個」，因為 + 運算子至少定義了一個「請」實例：</span><span class="sxs-lookup"><span data-stu-id="3fb79-121">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="3fb79-122">重複運算子會遵循一般的優先順序規則，並套用至緊接在前面的文字專案。</span><span class="sxs-lookup"><span data-stu-id="3fb79-122">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="3fb79-123">例如，下列文法會產生 "紐約" 和 "紐約"，但不會產生 "紐約紐約"：</span><span class="sxs-lookup"><span data-stu-id="3fb79-123">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="3fb79-124">因此，您通常會想要搭配使用這些運算子與群組字元。</span><span class="sxs-lookup"><span data-stu-id="3fb79-124">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="3fb79-125">例如，下列文法包含 "紐約" 和 "紐約紐約"：</span><span class="sxs-lookup"><span data-stu-id="3fb79-125">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="3fb79-126">當您想要撰寫包含重複順序的文法（例如電話號碼或專案清單的規格）時，重複運算子會很有用。</span><span class="sxs-lookup"><span data-stu-id="3fb79-126">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="3fb79-127">雖然運算子也可以搭配選擇性的方括弧群組字元使用，但這麼做可能會降低代理程式處理文法的效率。</span><span class="sxs-lookup"><span data-stu-id="3fb79-127">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="3fb79-128">您也可以使用省略號 ( ... ) 來支援 *word 找出*，也就是告訴語音辨識引擎忽略在片語中這個位置所說出的單字 (有時也稱為 *垃圾* 字) 。</span><span class="sxs-lookup"><span data-stu-id="3fb79-128">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="3fb79-129">因此，不論是以連續的單字或片語說出，語音引擎都只會辨識字串中的特定字組。</span><span class="sxs-lookup"><span data-stu-id="3fb79-129">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="3fb79-130">例如，如果您將此屬性設定為 " \[ ... \] 檢查郵件 \[ ...」 \] ，語音辨識引擎會比對像是「請檢查郵件」或「檢查 mail 請」這項命令的片語。</span><span class="sxs-lookup"><span data-stu-id="3fb79-130">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="3fb79-131">省略號可以用在字串內的任何位置。</span><span class="sxs-lookup"><span data-stu-id="3fb79-131">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="3fb79-132">不過，請小心使用這項技術，因為它可能會提高不必要相符專案的可能性。</span><span class="sxs-lookup"><span data-stu-id="3fb79-132">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="3fb79-133">定義命令的文字文法時，請至少包含一個必要的單字;也就是說，請避免只提供選擇性的字組。</span><span class="sxs-lookup"><span data-stu-id="3fb79-133">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="3fb79-134">此外，請確定單字只包含發音單字和字母。</span><span class="sxs-lookup"><span data-stu-id="3fb79-134">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="3fb79-135">如果是數位，最好是將單字拼寫出來，而不是使用不明確的標記法。</span><span class="sxs-lookup"><span data-stu-id="3fb79-135">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="3fb79-136">例如，"345" 不是很好的文法形式。</span><span class="sxs-lookup"><span data-stu-id="3fb79-136">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="3fb79-137">同樣地，請使用 "I 三重 E" 來取代 "IEEE"。</span><span class="sxs-lookup"><span data-stu-id="3fb79-137">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="3fb79-138">此外，請省略任何標點符號或符號。</span><span class="sxs-lookup"><span data-stu-id="3fb79-138">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="3fb79-139">例如，請 \# 使用「數位 1 10 元比薩」，而不是「$1 10 比薩」。</span><span class="sxs-lookup"><span data-stu-id="3fb79-139">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="3fb79-140">針對某個命令包含非發音的字元或符號，可能會導致語音引擎無法編譯所有命令的文法。</span><span class="sxs-lookup"><span data-stu-id="3fb79-140">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="3fb79-141">最後，從您所定義的其他語音命令盡可能讓您的語音參數盡可能不同。</span><span class="sxs-lookup"><span data-stu-id="3fb79-141">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="3fb79-142">命令的語音文法越相似，語音引擎就越可能提出辨識錯誤。</span><span class="sxs-lookup"><span data-stu-id="3fb79-142">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="3fb79-143">您也可以使用信賴分數，更清楚地區分兩個可能具有類似或類似發音語音文法的命令。</span><span class="sxs-lookup"><span data-stu-id="3fb79-143">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="3fb79-144">您可以用「*文字 \\ 發音*」的形式包含文法文字，其中 *文字* 是顯示的文字，而 *發音* 是說明發音的文字。</span><span class="sxs-lookup"><span data-stu-id="3fb79-144">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="3fb79-145">例如，當使用者說出 "first" 時，就會辨識文法「第1個」， \\ 但是 [**命令**](command-event.md) 事件會傳回「第1個」文字 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3fb79-145">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](command-event.md) event will return the text, "1st\\first".</span></span> <span data-ttu-id="3fb79-146">您也可以使用 IPA (國際注音字母) 來指定發音，方法是以井字型大小字元 ( " \# " ) 開頭，然後包含代表 IPA 發音的文字。</span><span class="sxs-lookup"><span data-stu-id="3fb79-146">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="3fb79-147">若為日文語音辨識引擎，您可以用 "*假名 \\ 漢字*" 格式來定義文法，以減少替代發音並提高精確度。</span><span class="sxs-lookup"><span data-stu-id="3fb79-147">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="3fb79-148"> (反轉順序的目的是為了回溯相容性。 ) 這對日文漢字中正確名稱的發音特別重要。</span><span class="sxs-lookup"><span data-stu-id="3fb79-148">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="3fb79-149">不過，您可以在不含假名的情況下傳遞漢字，在這種情況下，引擎應接聽所有可接受的漢字發音。</span><span class="sxs-lookup"><span data-stu-id="3fb79-149">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="3fb79-150">您也可以只傳入假名。</span><span class="sxs-lookup"><span data-stu-id="3fb79-150">You can also pass in just Kana.</span></span>

<span data-ttu-id="3fb79-151">另請注意，對於日文、中文和泰文之類的語言，如果未使用空白字元來指定斷字元號，請將 Unicode 零寬度空白字元 (0x200B) ，以表示邏輯斷詞。</span><span class="sxs-lookup"><span data-stu-id="3fb79-151">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="3fb79-152">除了使用分組或重複格式化字元的錯誤之外，除非引擎本身回報錯誤，否則 Agent 不會在您的文法中報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="3fb79-152">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="3fb79-153">如果您在文法中傳遞無法編譯引擎的文字，但是引擎不會處理並傳回做為錯誤，代理程式就無法回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="3fb79-153">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="3fb79-154">因此，用戶端應用程式必須謹慎地定義 **Voice** 屬性的文法。</span><span class="sxs-lookup"><span data-stu-id="3fb79-154">Therefore, the client application must be carefully define grammar for the **Voice** property.</span></span>

> [!Note]  
> <span data-ttu-id="3fb79-155">可用的文法功能可能取決於語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="3fb79-155">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="3fb79-156">您可能會想要檢查引擎的廠商，以判斷支援哪些文法選項。</span><span class="sxs-lookup"><span data-stu-id="3fb79-156">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="3fb79-157">使用 [**SRModeID**](srmodeid-property.md) 來使用特定的引擎。</span><span class="sxs-lookup"><span data-stu-id="3fb79-157">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="3fb79-158">這個屬性的操作取決於伺服器的 [語音辨識] 屬性的狀態。</span><span class="sxs-lookup"><span data-stu-id="3fb79-158">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="3fb79-159">例如，如果已停用或未安裝「語音辨識」，則此屬性不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="3fb79-159">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
