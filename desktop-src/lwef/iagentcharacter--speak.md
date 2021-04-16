---
title: IAgentCharacter 話
description: IAgentCharacter 話
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507903"
---
# <a name="iagentcharacterspeak"></a><span data-ttu-id="f5e9c-103">IAgentCharacter：：說話</span><span class="sxs-lookup"><span data-stu-id="f5e9c-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="f5e9c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f5e9c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="f5e9c-105">說出文字或音效檔。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="f5e9c-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f5e9c-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="f5e9c-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="f5e9c-108">字元要說出的文字。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="f5e9c-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span><span class="sxs-lookup"><span data-stu-id="f5e9c-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="f5e9c-110">要用於語音輸出的音效檔 (或檔案規格) 的 URL。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="f5e9c-111">這可以是標準的音效檔 (。WAV) 或語言增強的音效檔 (。LWV) 。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="f5e9c-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="f5e9c-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="f5e9c-113">接收 [**說話**](/windows/desktop/lwef/iagentcharacter--speak) 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="f5e9c-114">若要使用此方法搭配設定為使用文字轉換語音 (TTS) 引擎的字元;只要提供 *bszText* 參數即可。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="f5e9c-115">您可以 \| 在 *bszText* 參數中包含分隔號字元 () 來指定替代字串，如此一來，每當伺服器處理方法時，就會隨機播放不同的字串。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="f5e9c-116">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義 TTS 輸出的支援。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="f5e9c-117">如果您想要使用音效檔輸出作為字元，請在 *bszURL* 參數中指定檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="f5e9c-118">使用 HTTP 通訊協定下載音效檔時，請使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來確保檔案的可用性，然後再使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="f5e9c-119">您可以使用 *bszText* 參數來指定出現在字元之文字批註中的單字。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="f5e9c-120">如果您指定語言增強的音效檔 (。LWV) 針對 *bszURL* 參數，而且不指定文字， *bszText* 參數會使用儲存在檔案中的文字。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="f5e9c-121">[**說話**](/windows/desktop/lwef/iagentcharacter--speak)方法會使用最後播放的動畫來判斷要播放的說話動畫。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="f5e9c-122">例如，如果您在 **說話** 命令之前加上 [**IAgentCharacter：:P**](iagentcharacter--play.md) 配置 "**GestureRight**"，伺服器將會播放 **GestureRight** ，然後再播放 **GestureRight** 說話動畫。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="f5e9c-123">如果播放的最後一個動畫沒有說話動畫，Microsoft Agent 會播放指派給該字元 **說話** 狀態的動畫。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="f5e9c-124">如果您呼叫 [**說話**](/windows/desktop/lwef/iagentcharacter--speak) 且音訊頻道忙碌中，則不會聽到字元的音訊輸出，但文字會顯示在文字提示字元中。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="f5e9c-125">文字氣球的 [Enabled](enabled-property.md) 屬性也必須為 **True** ，才會顯示文字。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="f5e9c-126">Microsoft Agent 自動斷詞字組，使用空白字元來分隔文字 (例如，空格鍵和 tab) 。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="f5e9c-127">不過，它也可能會中斷文字以容納球。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="f5e9c-128">在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="f5e9c-129">先使用 [**IAgentCharacterEx：： SetLanguageID**](iagentcharacterex--setlanguageid.md) 來設定字元的語言 (識別碼，然後再使用 [ [**朗讀**](/windows/desktop/lwef/iagentcharacter--speak) ] 方法，以確保文字氣球內適當的文字顯示。</span><span class="sxs-lookup"><span data-stu-id="f5e9c-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="f5e9c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5e9c-130">See Also</span></span>

<span data-ttu-id="f5e9c-131">[**IAgentCharacter：:P 的版面**](iagentcharacter--play.md)配置、 [**IAgentBalloon：： GetEnabled**](iagentballoon--getenabled.md)、 [**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)</span><span class="sxs-lookup"><span data-stu-id="f5e9c-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 