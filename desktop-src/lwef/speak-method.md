---
title: 說話方法
description: 說話方法
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463048"
---
# <a name="speak-method"></a><span data-ttu-id="993d5-103">說話方法</span><span class="sxs-lookup"><span data-stu-id="993d5-103">Speak Method</span></span>

<span data-ttu-id="993d5-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="993d5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="993d5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="993d5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="993d5-106">為指定的字元說出指定的文字或音效檔。</span><span class="sxs-lookup"><span data-stu-id="993d5-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="993d5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="993d5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="993d5-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。說* 出 \*  \[ *文字* \] ， \[ *Url*\]</span><span class="sxs-lookup"><span data-stu-id="993d5-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="993d5-109">部分</span><span class="sxs-lookup"><span data-stu-id="993d5-109">Part</span></span>   | <span data-ttu-id="993d5-110">描述</span><span class="sxs-lookup"><span data-stu-id="993d5-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="993d5-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="993d5-111">*Text*</span></span> | <span data-ttu-id="993d5-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="993d5-112">Optional.</span></span> <span data-ttu-id="993d5-113">字串，指定字元所顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="993d5-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="993d5-114">*Url*</span><span class="sxs-lookup"><span data-stu-id="993d5-114">*Url*</span></span>  | <span data-ttu-id="993d5-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="993d5-115">Optional.</span></span> <span data-ttu-id="993d5-116">字串運算式，指定音訊檔 ( 的位置。WAV 或。) 的 LWV 格式。</span><span class="sxs-lookup"><span data-stu-id="993d5-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="993d5-117">您可以將位置指定為檔案 (包括 UNC 路徑規格) 或 URL (當字元動畫資料也透過 HTTP 通訊協定) 進行抓取時。</span><span class="sxs-lookup"><span data-stu-id="993d5-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="993d5-118">備註</span><span class="sxs-lookup"><span data-stu-id="993d5-118">Remarks</span></span>

<span data-ttu-id="993d5-119">雖然 *Text* 和 *Url* 參數是選擇性的，但必須提供其中一個。</span><span class="sxs-lookup"><span data-stu-id="993d5-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="993d5-120">若要使用這個方法，並將字元設定為只在其文字提示字元中說話，或使用文字轉換語音 (TTS) 引擎，只要提供 *text* 參數即可。</span><span class="sxs-lookup"><span data-stu-id="993d5-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="993d5-121">請在單字之間加上空格，以在文字氣球中定義適當的斷字元號，即使通常不包含空格的語言也是如此。</span><span class="sxs-lookup"><span data-stu-id="993d5-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="993d5-122">您也可以 \| 在 *Text* 參數中包含分隔號字元 () 來指定替代字串，讓伺服器在每次處理方法時隨機播放不同的字串。</span><span class="sxs-lookup"><span data-stu-id="993d5-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="993d5-123">使用 Microsoft Agent 字元編輯器編譯字元時，會定義 TTS 輸出的字元支援。</span><span class="sxs-lookup"><span data-stu-id="993d5-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="993d5-124">若要產生 TTS 輸出，必須先安裝相容的 TTS 引擎，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="993d5-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="993d5-125">如需詳細資訊，請參閱 [存取語音服務](accessing-speech-services.md)。</span><span class="sxs-lookup"><span data-stu-id="993d5-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="993d5-126">如果您使用錄製的音效檔 (。WAV 或。LWV 格式：只) 字元的輸出，請在 *Url* 參數中指定檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="993d5-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="993d5-127">此檔案規格可以包含本機 (絕對或相對) 或通用命名慣例 (UNC) 路徑。</span><span class="sxs-lookup"><span data-stu-id="993d5-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="993d5-128">檔案名不能包含美國字碼頁1252中未包含的任何字元。</span><span class="sxs-lookup"><span data-stu-id="993d5-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="993d5-129">但是，如果您使用 HTTP 通訊協定來存取字元動畫資料，請使用 [**Get**](get-method.md) 方法來載入動畫，然後再呼叫 **說話** 方法。</span><span class="sxs-lookup"><span data-stu-id="993d5-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="993d5-130">如需創意的詳細資訊，請參閱 [使用 Microsoft 語言資訊音效編輯工具](using-the-microsoft-linguistic-information-sound-editing-tool.md) 。LWV 檔案。</span><span class="sxs-lookup"><span data-stu-id="993d5-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="993d5-131">當您使用錄製的音效檔案輸出時，仍然可以使用 *Text* 參數來指定出現在字元之文字批註中的單字。</span><span class="sxs-lookup"><span data-stu-id="993d5-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="993d5-132">但是，如果您指定語言增強的音效檔 (。LWV *Url* 參數的) ，而不指定文字給文字提示，則 *text* 參數會使用儲存在檔案中的文字。</span><span class="sxs-lookup"><span data-stu-id="993d5-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="993d5-133">您也可以使用包含在 *文字* 參數中的特殊標籤，來改變語音輸出的參數。</span><span class="sxs-lookup"><span data-stu-id="993d5-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="993d5-134">如需詳細資訊，請參閱 [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md)。</span><span class="sxs-lookup"><span data-stu-id="993d5-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="993d5-135">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="993d5-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="993d5-136">您可以使用這個來同步處理常式代碼的其他部分與字元的語音輸出，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="993d5-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


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



<span data-ttu-id="993d5-137">您也可以使用 [**要求**](/windows/desktop/lwef/the-request-object) 物件來檢查特定的錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="993d5-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="993d5-138">例如，如果您使用「 **說話** 」方法來說出但未安裝相容的 TTS 引擎，則伺服器會將 **要求** 物件的 [**Status**](status-property.md) 屬性設為「失敗」，並將其 [**Description**](description-property.md) 屬性設定為「類別未註冊」或「未知或物件傳回的錯誤」。</span><span class="sxs-lookup"><span data-stu-id="993d5-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="993d5-139">若要判斷是否已安裝 TTS 引擎，請使用 [**TTSModeID**](ttsmodeid-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="993d5-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="993d5-140">同樣地，如果您有嘗試說出音效檔的字元，而且檔案尚未載入或音訊裝置有問題，則伺服器也會將 [**要求**](/windows/desktop/lwef/the-request-object) 物件的 [**Status**](status-property.md) 屬性設為「失敗」，並提供適當的錯誤碼號碼。</span><span class="sxs-lookup"><span data-stu-id="993d5-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="993d5-141">您也可以在說出的文字中包含書簽聲控標籤，以同步處理您的程式碼：</span><span class="sxs-lookup"><span data-stu-id="993d5-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


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



<span data-ttu-id="993d5-142">如需書簽聲控標籤的詳細資訊，請參閱 [語音輸出標記](mrk-tag.md)。</span><span class="sxs-lookup"><span data-stu-id="993d5-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="993d5-143">**說話** 方法會使用最後播放的動作來判斷要播放的說話動畫。</span><span class="sxs-lookup"><span data-stu-id="993d5-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="993d5-144">例如，如果您在「**說話**」命令前面加上「**GestureRight**」，伺服器將會播放 **GestureRight** ，然後 [**再播放**](play-method.md) **GestureRight** 說話動畫。</span><span class="sxs-lookup"><span data-stu-id="993d5-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="993d5-145">如果播放的最後一個動畫沒有說話動畫，則代理程式會播放指派給字元 **說話** 狀態的動畫。</span><span class="sxs-lookup"><span data-stu-id="993d5-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="993d5-146">如果您呼叫 **說話** 且音訊頻道忙碌中，則不會聽到字元的音訊輸出，但文字會顯示在文字提示字元中。</span><span class="sxs-lookup"><span data-stu-id="993d5-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="993d5-147">代理程式自動斷詞字提示字元會中斷使用空白字元的單字 (例如，空格鍵或 Tab) 。</span><span class="sxs-lookup"><span data-stu-id="993d5-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="993d5-148">但是，如果無法使用，它可能會中斷文字以符合氣球。</span><span class="sxs-lookup"><span data-stu-id="993d5-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="993d5-149">在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。</span><span class="sxs-lookup"><span data-stu-id="993d5-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="993d5-150">文字氣球的 [**Enabled**](enabled-property.md) 屬性也必須為 **True** ，才能顯示文字。</span><span class="sxs-lookup"><span data-stu-id="993d5-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="993d5-151">設定字元的語言識別項 (，方法是在使用 [**朗讀**] 方法之前，先設定字元的 **LanguageID** ，以確保文字氣球內適當的文字顯示。</span><span class="sxs-lookup"><span data-stu-id="993d5-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="993d5-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="993d5-152">See Also</span></span>

<span data-ttu-id="993d5-153">[**Bookmark 事件**](bookmark-event.md)、 [**RequestStart 事件**](requeststart-event.md)、 [**RequestComplete 事件**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="993d5-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 