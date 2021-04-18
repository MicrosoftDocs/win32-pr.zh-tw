---
title: 明確和限制選擇
description: 明確和限制選擇
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ed5f95c2e516f304ffa28bcca1d9fd67a9169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964984"
---
# <a name="clarify-and-limit-choices"></a><span data-ttu-id="f5290-103">明確和限制選擇</span><span class="sxs-lookup"><span data-stu-id="f5290-103">Clarify and Limit Choices</span></span>

<span data-ttu-id="f5290-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f5290-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f5290-105">當使用者學習適當文法的範圍時，語音辨識會變得更成功。</span><span class="sxs-lookup"><span data-stu-id="f5290-105">Speech recognition becomes more successful when the user learns the range of appropriate grammar.</span></span> <span data-ttu-id="f5290-106">當選擇範圍有限時，也會更好用。</span><span class="sxs-lookup"><span data-stu-id="f5290-106">It also works better when the range of choices is limited.</span></span> <span data-ttu-id="f5290-107">輸入愈少，語音引擎可以分析聲場資訊輸入的效果愈好。</span><span class="sxs-lookup"><span data-stu-id="f5290-107">The less open-ended the input, the better the speech engine can analyze the acoustic information input.</span></span>

<span data-ttu-id="f5290-108">Microsoft Agent 包含數個內建的布建，可提高語音輸入的成功。</span><span class="sxs-lookup"><span data-stu-id="f5290-108">Microsoft Agent includes several built-in provisions that increase the success of speech input.</span></span> <span data-ttu-id="f5290-109">第一個是當使用者說「開啟命令視窗」或「我可以說什麼？」時，所顯示的 [命令] 視窗。</span><span class="sxs-lookup"><span data-stu-id="f5290-109">The first is the Commands Window displayed when the user says, "Open Commands Window," or "What can I say?"</span></span> <span data-ttu-id="f5290-110"> (，或當使用者從字元的快顯功能表中選擇 [開啟命令視窗] 時) 。</span><span class="sxs-lookup"><span data-stu-id="f5290-110">(or when the user chooses Open Commands Window from the character's pop-up menu).</span></span> <span data-ttu-id="f5290-111">命令視窗可作為語音引擎之作用中文法的視覺化指南。</span><span class="sxs-lookup"><span data-stu-id="f5290-111">The Command Window serves as a visual guide to the active grammar of the speech engine.</span></span> <span data-ttu-id="f5290-112">它也會藉由只啟用輸入-主動應用程式和 Microsoft 代理程式全域命令的語音文法，來減少辨識錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5290-112">It also reduces recognition errors by activating only the speech grammar of the input-active application and Microsoft Agent's global commands.</span></span> <span data-ttu-id="f5290-113">因此，語音引擎的主動式文法會套用至立即內容。</span><span class="sxs-lookup"><span data-stu-id="f5290-113">Therefore, the active grammar of the speech engine applies to the immediate context.</span></span> <span data-ttu-id="f5290-114">如需 [命令] 視窗的詳細資訊，請參閱 [Microsoft Agent 程式設計介面總覽](microsoft-agent-programming-interface-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f5290-114">For more information on the Commands Window, see [Microsoft Agent Programming Interface Overview](microsoft-agent-programming-interface-overview.md).</span></span>

<span data-ttu-id="f5290-115">當您建立 Microsoft Agent 支援語音的命令時，您可以撰寫出現在 [命令] 視窗中的標題文字以及語音文字 (文法) ，也就是引擎應用來比對此命令的文字。</span><span class="sxs-lookup"><span data-stu-id="f5290-115">When you create Microsoft Agent voice-enabled commands, you can author the caption text that appears in Commands Window as well as its voice text (grammar), the words that the engine should use for matching this command.</span></span> <span data-ttu-id="f5290-116">請一律嘗試讓您的命令盡可能具特色。</span><span class="sxs-lookup"><span data-stu-id="f5290-116">Always try to make your commands as distinctive as possible.</span></span> <span data-ttu-id="f5290-117">命令的措辭（尤其是語音文字）之間的差異愈大，語音引擎可以分辨朗讀命令並提供精確的相符結果。</span><span class="sxs-lookup"><span data-stu-id="f5290-117">The greater the difference between the wording of commands, especially for the voice text, the more likely the speech engine will be able to discriminate between spoken commands and provide an accurate match.</span></span> <span data-ttu-id="f5290-118">也請避免單一單字或非常短的命令。</span><span class="sxs-lookup"><span data-stu-id="f5290-118">Also avoid single-word or very short commands.</span></span> <span data-ttu-id="f5290-119">一般而言，說話語句中的聲音資訊越多，就能讓引擎有更好的機會來精確符合。</span><span class="sxs-lookup"><span data-stu-id="f5290-119">Generally, more acoustic information in a spoken utterance gives the engine a better chance to make an accurate match.</span></span>

<span data-ttu-id="f5290-120">定義命令的語音文字時，請提供合理的不同用語。</span><span class="sxs-lookup"><span data-stu-id="f5290-120">When defining the voice text for a command, provide a reasonable variety of wording.</span></span> <span data-ttu-id="f5290-121">表示相同內容的要求可以片語非常不同，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="f5290-121">Requests that mean the same thing can be phrased very differently, as illustrated in the following example:</span></span>

<span data-ttu-id="f5290-122">新增一些辣肉腸。</span><span class="sxs-lookup"><span data-stu-id="f5290-122">Add some pepperoni.</span></span>

<span data-ttu-id="f5290-123">我喜歡一些辣肉腸。</span><span class="sxs-lookup"><span data-stu-id="f5290-123">I'd like some pepperoni.</span></span>

<span data-ttu-id="f5290-124">您可以新增一些辣肉腸嗎？</span><span class="sxs-lookup"><span data-stu-id="f5290-124">Could you add some pepperoni?</span></span>

<span data-ttu-id="f5290-125">辣肉腸，請。</span><span class="sxs-lookup"><span data-stu-id="f5290-125">Pepperoni, please.</span></span>

<span data-ttu-id="f5290-126">Microsoft 代理程式可讓您輕鬆地為應用程式指定語音文法的替代或選擇性單字。</span><span class="sxs-lookup"><span data-stu-id="f5290-126">Microsoft Agent enables you to easily specify alternatives or optional words for the voice grammar for your application.</span></span> <span data-ttu-id="f5290-127">您可以用括弧括住替代單字或片語，並以分隔號字元分隔。</span><span class="sxs-lookup"><span data-stu-id="f5290-127">You enclose alternative words or phrases between parentheses, separated by a vertical bar character.</span></span> <span data-ttu-id="f5290-128">您可以在方括弧字元之間加上括弧，以定義選擇性的單字。</span><span class="sxs-lookup"><span data-stu-id="f5290-128">You can define optional words by enclosing them between square bracket characters.</span></span> <span data-ttu-id="f5290-129">您也可以嵌套替代字或選擇性的單字。</span><span class="sxs-lookup"><span data-stu-id="f5290-129">You can also nest alternatives or optional words.</span></span> <span data-ttu-id="f5290-130">此外，您也可以使用省略號 ( ... ) 作為任何單字的預留位置。</span><span class="sxs-lookup"><span data-stu-id="f5290-130">In addition, you can also use an ellipsis (...) in voice text as a placeholder for any word.</span></span> <span data-ttu-id="f5290-131">不過，使用省略號太頻繁可能會讓引擎更難區分不同的語音命令。</span><span class="sxs-lookup"><span data-stu-id="f5290-131">However, using ellipses too frequently may make it more difficult for the engine to distinguish between different voice commands.</span></span> <span data-ttu-id="f5290-132">在任何情況下，請務必確定您的語音文字針對每個不是選擇性的命令都至少包含一個特殊字。</span><span class="sxs-lookup"><span data-stu-id="f5290-132">In any case, always make sure that your voice text includes at least one distinctive word for each command that is not optional.</span></span> <span data-ttu-id="f5290-133">一般而言，這應該符合您在 [命令] 視窗中所定義之標題文字中的單字或單字。</span><span class="sxs-lookup"><span data-stu-id="f5290-133">Typically, this should match a word or words in the caption text you define that appears in the Commands Window.</span></span>

<span data-ttu-id="f5290-134">雖然您可以在標題文字中包含符號、標點符號或縮寫，但請在您的聲音文字中避免這些符號、標點符號或縮寫。</span><span class="sxs-lookup"><span data-stu-id="f5290-134">Although you can include symbols, punctuation, or abbreviations in your caption text, avoid them in your voice text.</span></span> <span data-ttu-id="f5290-135">許多語音辨識引擎無法處理符號和縮寫，或可能會使用它們來設定特殊的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="f5290-135">Many speech recognition engines cannot handle symbols and abbreviations or may use them to set special input parameters.</span></span> <span data-ttu-id="f5290-136">此外，請將數位加上拼寫。</span><span class="sxs-lookup"><span data-stu-id="f5290-136">In addition, spell out numbers.</span></span> <span data-ttu-id="f5290-137">這也可確保更可靠的辨識支援。</span><span class="sxs-lookup"><span data-stu-id="f5290-137">This also ensures more reliable recognition support.</span></span>

<span data-ttu-id="f5290-138">您也可以使用指示詞提示，以避免開啟結束輸入。</span><span class="sxs-lookup"><span data-stu-id="f5290-138">You can also use directive prompts to avoid open-ended input.</span></span> <span data-ttu-id="f5290-139">指示詞會以隱含方式參考選擇或明確陳述它們，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="f5290-139">Directive prompts implicitly reference the choices or explicitly state them, as shown in the following examples:</span></span>



|                                            |                                                     |
|--------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="f5290-140">你想要什麼？</span><span class="sxs-lookup"><span data-stu-id="f5290-140">What do you want?</span></span>                          | <span data-ttu-id="f5290-141">太一般，開放式要求已結束</span><span class="sxs-lookup"><span data-stu-id="f5290-141">Too general, an open-ended request</span></span>                  |
| <span data-ttu-id="f5290-142">選擇比薩樣式或原料。</span><span class="sxs-lookup"><span data-stu-id="f5290-142">Choose a pizza style or ingredient.</span></span>        | <span data-ttu-id="f5290-143">好的，如果有選項可以看見，但仍是一般</span><span class="sxs-lookup"><span data-stu-id="f5290-143">Good, if choices are visible, but still general</span></span>     |
| <span data-ttu-id="f5290-144">說「夏威夷」、「芝加哥」或「Works」。</span><span class="sxs-lookup"><span data-stu-id="f5290-144">Say "Hawaiian," "Chicago," or "The Works."</span></span> | <span data-ttu-id="f5290-145">更好的，具有特定選項的明確指示詞</span><span class="sxs-lookup"><span data-stu-id="f5290-145">Better, an explicit directive with specific options</span></span> |



 

<span data-ttu-id="f5290-146">這會引導使用者發出有效的命令。</span><span class="sxs-lookup"><span data-stu-id="f5290-146">This guides the user toward issuing a valid command.</span></span> <span data-ttu-id="f5290-147">藉由建議單字或片語，您比較有可能會在傳回時產生預期的用語。</span><span class="sxs-lookup"><span data-stu-id="f5290-147">By suggesting the words or phrase, you are more likely to elicit expected wording in return.</span></span> <span data-ttu-id="f5290-148">若要避免非自然 repetitiveness，請變更用語或縮短原始的文字以進行後續的簡報，因為使用者會更體驗輸入樣式。</span><span class="sxs-lookup"><span data-stu-id="f5290-148">To avoid unnatural repetitiveness, change the wording or shorten the original for subsequent presentation as the user becomes more experienced with the input style.</span></span> <span data-ttu-id="f5290-149">指示詞提示也可以用於使用者無法在指定時間內發出命令的情況，或無法提供預期的命令。</span><span class="sxs-lookup"><span data-stu-id="f5290-149">Directive prompts can also be used in situations where the user fails to issue a command within a prescribed time or fails to provide an expected command.</span></span> <span data-ttu-id="f5290-150">您可以使用語音輸出、應用程式介面或兩者來提供指示詞提示。</span><span class="sxs-lookup"><span data-stu-id="f5290-150">Directive prompts can be provided using speech output, your application interfaces, or both.</span></span> <span data-ttu-id="f5290-151">關鍵是協助使用者知道適當的選擇。</span><span class="sxs-lookup"><span data-stu-id="f5290-151">The key is helping the user know the appropriate choices.</span></span>

<span data-ttu-id="f5290-152">用語會影響提示的成功與否。</span><span class="sxs-lookup"><span data-stu-id="f5290-152">Wording influences the success of a prompt.</span></span> <span data-ttu-id="f5290-153">例如，「您想要訂購比薩嗎？」的提示。</span><span class="sxs-lookup"><span data-stu-id="f5290-153">For example, the prompt, "Would you like to order your pizza?"</span></span> <span data-ttu-id="f5290-154">可能會產生「是」或「否」回應，但也可能產生訂單要求。</span><span class="sxs-lookup"><span data-stu-id="f5290-154">could generate either a "Yes" or "No" response, but it might also generate an order request.</span></span> <span data-ttu-id="f5290-155">定義不明確的提示，或準備接受更多可能的回應。</span><span class="sxs-lookup"><span data-stu-id="f5290-155">Define prompts to be non-ambiguous or be prepared to accept a larger variety of possible responses.</span></span> <span data-ttu-id="f5290-156">此外，請注意人們模仿單字和表達所聽到的趨勢。</span><span class="sxs-lookup"><span data-stu-id="f5290-156">In addition, note the tendency for people to mimic words and constructs they hear.</span></span> <span data-ttu-id="f5290-157">這通常可用來協助引起適當的回應，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="f5290-157">This can often be used to help evoke an appropriate response as in the following example:</span></span>



|            |                                 |
|------------|---------------------------------|
| <span data-ttu-id="f5290-158">使用者：</span><span class="sxs-lookup"><span data-stu-id="f5290-158">User:</span></span>      | <span data-ttu-id="f5290-159">顯示 Paul 的所有訊息。</span><span class="sxs-lookup"><span data-stu-id="f5290-159">Show me all messages from Paul.</span></span> |
| <span data-ttu-id="f5290-160">字元：</span><span class="sxs-lookup"><span data-stu-id="f5290-160">Character:</span></span> |                                 |



 

<span data-ttu-id="f5290-161">這比較可能會使用可能的前置詞 "I mean" 或 "I" 來產生其中一個合作物件的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="f5290-161">This is more likely to elicit the full name of one of the parties with the possible prefix of "I mean" or "I meant."</span></span>

<span data-ttu-id="f5290-162">由於 Microsoft 代理程式字元是在 Microsoft Windows 的視覺化介面中運作，因此您可以使用視覺元素來提供語音輸入的指示詞提示。</span><span class="sxs-lookup"><span data-stu-id="f5290-162">Because Microsoft Agent characters operate within the visual interface of Microsoft Windows, you can use visual elements to provide directive prompts for speech input.</span></span> <span data-ttu-id="f5290-163">例如，您可以在選項清單中使用字元手勢，並要求使用者選取其中一個，或是在對話方塊或訊息視窗中顯示選擇。</span><span class="sxs-lookup"><span data-stu-id="f5290-163">For example, you can have the character gesture at a list of choices and request that the user select one, or display choices in a dialog box or message window.</span></span> <span data-ttu-id="f5290-164">這有兩個優點：它會明確建議您要讓使用者說出的文字，並提供另一種方法讓使用者回復。</span><span class="sxs-lookup"><span data-stu-id="f5290-164">This has two benefits: it explicitly suggests the words you want the user to speak and it provides an alternate way for the user to reply.</span></span>

<span data-ttu-id="f5290-165">您也可以使用其他互動模式，以稍微建議使用者適當的語音文法，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="f5290-165">You can also use other modes of interaction to subtly suggest to users the appropriate speech grammar, as shown in the following example:</span></span>



|            |                                                     |
|------------|-----------------------------------------------------|
| <span data-ttu-id="f5290-166">使用者：</span><span class="sxs-lookup"><span data-stu-id="f5290-166">User:</span></span>      | <span data-ttu-id="f5290-167"> (按下滑鼠) 來按一下夏威夷樣式的比薩選項</span><span class="sxs-lookup"><span data-stu-id="f5290-167">(Clicks Hawaiian-style pizza option with the mouse)</span></span> |
| <span data-ttu-id="f5290-168">字元：</span><span class="sxs-lookup"><span data-stu-id="f5290-168">Character:</span></span> | <span data-ttu-id="f5290-169">夏威夷樣式的比薩。</span><span class="sxs-lookup"><span data-stu-id="f5290-169">Hawaiian-style pizza.</span></span>                               |
| <span data-ttu-id="f5290-170">使用者：</span><span class="sxs-lookup"><span data-stu-id="f5290-170">User:</span></span>      | <span data-ttu-id="f5290-171"> (按一下滑鼠) 的額外乳酪選項</span><span class="sxs-lookup"><span data-stu-id="f5290-171">(Clicks Extra Cheese option with the mouse)</span></span>         |
| <span data-ttu-id="f5290-172">字元：</span><span class="sxs-lookup"><span data-stu-id="f5290-172">Character:</span></span> | <span data-ttu-id="f5290-173">新增「額外乳酪」。</span><span class="sxs-lookup"><span data-stu-id="f5290-173">Add "Extra Cheese."</span></span>                                 |



 

<span data-ttu-id="f5290-174">成功語音輸入的另一個重要因素是在引擎準備好進行輸入時，提示使用者，因為許多語音引擎一次只允許一個語句。</span><span class="sxs-lookup"><span data-stu-id="f5290-174">Another important factor in successful speech input is cueing the user when the engine is ready for input, because many speech engines allow only a single utterance at a time.</span></span> <span data-ttu-id="f5290-175">Microsoft Agent 提供這兩種方式的支援。</span><span class="sxs-lookup"><span data-stu-id="f5290-175">Microsoft Agent provides support for this in two ways.</span></span> <span data-ttu-id="f5290-176">首先，如果音效卡支援 MIDI，當語音輸入頻道可用時，Microsoft 代理程式會產生簡短的聲音來發出通知。</span><span class="sxs-lookup"><span data-stu-id="f5290-176">First, if the sound card supports MIDI, Microsoft Agent generates a brief tone to signal when the speech-input channel is available.</span></span> <span data-ttu-id="f5290-177">其次，當 (語音引擎的字元) 正在接聽輸入時，接聽提示視窗會顯示適當的文字提示。</span><span class="sxs-lookup"><span data-stu-id="f5290-177">Second, the Listening Tip window displays an appropriate text prompt when the character (speech engine) is listening for input.</span></span> <span data-ttu-id="f5290-178">此外，此秘訣會顯示引擎的聲音。</span><span class="sxs-lookup"><span data-stu-id="f5290-178">In addition, this tip displays what the engine heard.</span></span>

 

 




