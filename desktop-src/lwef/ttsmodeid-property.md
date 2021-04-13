---
title: TTSModeID 屬性
description: TTSModeID 屬性
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183968"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="13fff-103">TTSModeID 屬性</span><span class="sxs-lookup"><span data-stu-id="13fff-103">TTSModeID Property</span></span>

<span data-ttu-id="13fff-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="13fff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="13fff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="13fff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="13fff-106">傳回或設定用於字元的 TTS 引擎模式。</span><span class="sxs-lookup"><span data-stu-id="13fff-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="13fff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="13fff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="13fff-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。TTSModeID* \*  \[  =  *ModeID*\]</span><span class="sxs-lookup"><span data-stu-id="13fff-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="13fff-109">部分</span><span class="sxs-lookup"><span data-stu-id="13fff-109">Part</span></span>     | <span data-ttu-id="13fff-110">描述</span><span class="sxs-lookup"><span data-stu-id="13fff-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="13fff-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="13fff-111">*ModeID*</span></span> | <span data-ttu-id="13fff-112">對應至語音引擎之模式識別碼的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="13fff-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13fff-113">備註</span><span class="sxs-lookup"><span data-stu-id="13fff-113">Remarks</span></span>

<span data-ttu-id="13fff-114">這個屬性會針對字元的讀出輸出，判斷 (文字轉換語音) 引擎模式識別碼的 TTS。</span><span class="sxs-lookup"><span data-stu-id="13fff-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="13fff-115">TTS 引擎的模式識別碼是由語音供應商定義的格式化字串，可唯一識別引擎的模式。</span><span class="sxs-lookup"><span data-stu-id="13fff-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="13fff-116">如需詳細資訊，請參閱 [在程式碼中存取語音引擎](accessing-a-speech-engine-in-your-code.md)。</span><span class="sxs-lookup"><span data-stu-id="13fff-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="13fff-117">設定這個屬性會覆寫伺服器嘗試載入以該字元編譯之 TTS 設定為基礎的引擎，以及字元目前的 [**LanguageID**](languageid-property.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="13fff-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="13fff-118">但是，如果您針對未安裝的引擎指定模式識別碼，或使用者已在 Microsoft Agent 屬性工作表中停用語音輸出 (**AudioOutput。 Enabled = False**) ，伺服器會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="13fff-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="13fff-119">如果您未 (或未成功) 為字元設定 TTS 模式識別碼，伺服器會檢查字元的已編譯 TTS 模式設定是否符合字元的 [**LanguageID**](languageid-property.md) 設定，以及是否已安裝相關聯的 tts 引擎。</span><span class="sxs-lookup"><span data-stu-id="13fff-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="13fff-120">如果是，則為讀出字元輸出的字元所使用的 TTS 模式，而這個屬性會傳回該模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="13fff-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="13fff-121">如果不是，伺服器會要求相容的 SAPI 語音引擎，該引擎會符合字元的 **LanguageID** ，以及字元的已編譯模式識別碼的性別和年齡組。</span><span class="sxs-lookup"><span data-stu-id="13fff-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="13fff-122">如果您未設定字元的 **LanguageID**，則其 **LanguageID** 為目前的使用者語言。</span><span class="sxs-lookup"><span data-stu-id="13fff-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="13fff-123">如果找不到相符的引擎，則查詢此屬性會傳回引擎模式識別碼的空字串。</span><span class="sxs-lookup"><span data-stu-id="13fff-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="13fff-124">同樣地，如果您在使用者已停用 Microsoft Agent 屬性工作表中的語音輸出時查詢此屬性 (**AudioOutput。 Enabled = False**) ，此值將會是空字串。</span><span class="sxs-lookup"><span data-stu-id="13fff-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="13fff-125">如果尚未載入關聯的引擎，則查詢或設定這個屬性會將其載入 (（如果尚未載入）) 。</span><span class="sxs-lookup"><span data-stu-id="13fff-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="13fff-126">但是，如果已安裝字元編譯的 TTS 設定中指定的引擎，並且符合字元的語言識別項設定，則會在載入字元時載入引擎。</span><span class="sxs-lookup"><span data-stu-id="13fff-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="13fff-127">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="13fff-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="13fff-128">Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。</span><span class="sxs-lookup"><span data-stu-id="13fff-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="13fff-129">支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。</span><span class="sxs-lookup"><span data-stu-id="13fff-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="13fff-130">如果您的系統上未安裝相容的音效支援，這個屬性也會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="13fff-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="13fff-131">如果未安裝 Speech.dll，且您指定的引擎不符合字元的編譯 TTS 模式設定，則設定 **TTSModeID** 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="13fff-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="13fff-132">查詢此屬性通常不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="13fff-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="13fff-133">但是，如果語音引擎的載入異常時間很長，您可能會收到錯誤，指出查詢已超時。</span><span class="sxs-lookup"><span data-stu-id="13fff-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="13fff-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13fff-134">See Also</span></span>

[<span data-ttu-id="13fff-135">**LanguageID 屬性**</span><span class="sxs-lookup"><span data-stu-id="13fff-135">**LanguageID property**</span></span>](languageid-property.md)


 

 




