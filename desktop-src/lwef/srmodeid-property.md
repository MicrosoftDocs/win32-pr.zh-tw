---
title: SRModeID 屬性
description: SRModeID 屬性
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976328"
---
# <a name="srmodeid-property"></a><span data-ttu-id="abfa1-103">SRModeID 屬性</span><span class="sxs-lookup"><span data-stu-id="abfa1-103">SRModeID Property</span></span>

<span data-ttu-id="abfa1-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="abfa1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="abfa1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="abfa1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="abfa1-106">傳回或設定字元使用的語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="abfa1-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="abfa1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="abfa1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="abfa1-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。SRModeID* \*  \[  =  *ModeID*\]</span><span class="sxs-lookup"><span data-stu-id="abfa1-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="abfa1-109">部分</span><span class="sxs-lookup"><span data-stu-id="abfa1-109">Part</span></span>     | <span data-ttu-id="abfa1-110">描述</span><span class="sxs-lookup"><span data-stu-id="abfa1-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="abfa1-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="abfa1-111">*ModeID*</span></span> | <span data-ttu-id="abfa1-112">對應至語音引擎之模式識別碼的字串運算式。</span><span class="sxs-lookup"><span data-stu-id="abfa1-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abfa1-113">備註</span><span class="sxs-lookup"><span data-stu-id="abfa1-113">Remarks</span></span>

<span data-ttu-id="abfa1-114">屬性會決定語音輸入的字元所使用的語音辨識引擎。</span><span class="sxs-lookup"><span data-stu-id="abfa1-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="abfa1-115">語音辨識引擎的模式識別碼是由語音供應商定義的格式化字串，可唯一識別引擎。</span><span class="sxs-lookup"><span data-stu-id="abfa1-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="abfa1-116">如需詳細資訊，請參閱 [在程式碼中存取語音引擎](accessing-a-speech-engine-in-your-code.md)。</span><span class="sxs-lookup"><span data-stu-id="abfa1-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="abfa1-117">如果您針對未安裝的語音引擎指定模式識別碼，則如果使用者已停用 [Microsoft 代理程式] 屬性工作表中的 [語音辨識] () ，或是指定之語音引擎的語言不符合字元的 [**LanguageID**](languageid-property.md) 設定，則伺服器會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="abfa1-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="abfa1-118">如果您查詢此屬性，但尚未成功 () 設定語音辨識引擎，則伺服器會根據字元的 [**LanguageID**](languageid-property.md) 設定，傳回由 SAPI 傳回的引擎模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="abfa1-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="abfa1-119">如果您尚未設定此字元的 **LanguageID**，則 Agent 會根據使用者的預設語言識別項設定，傳回由 SAPI 傳回的引擎模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="abfa1-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="abfa1-120">如果沒有相符的引擎，伺服器會傳回空字串 ( "" ) 。</span><span class="sxs-lookup"><span data-stu-id="abfa1-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="abfa1-121">查詢此屬性不需要該 [**SpeechInput。 Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) 必須設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="abfa1-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="abfa1-122">但是，如果您在停用語音輸入時查詢屬性，伺服器就會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="abfa1-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="abfa1-123">啟用語音輸入時 (在 [先進字元選項] 視窗中) ，查詢或設定這個屬性會載入關聯的引擎 (如果尚未載入) ，然後啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="abfa1-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="abfa1-124">亦即，接聽鍵可供使用，而且可以顯示接聽提示。</span><span class="sxs-lookup"><span data-stu-id="abfa1-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="abfa1-125"> (接聽鍵和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="abfa1-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="abfa1-126">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="abfa1-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="abfa1-127">Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。</span><span class="sxs-lookup"><span data-stu-id="abfa1-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="abfa1-128">支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。</span><span class="sxs-lookup"><span data-stu-id="abfa1-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="abfa1-129">如果您的系統上未安裝相容的音效支援，這個屬性也會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="abfa1-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="abfa1-130">查詢此屬性通常不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="abfa1-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="abfa1-131">但是，如果語音引擎的載入異常時間很長，您可能會收到錯誤，指出查詢已超時。</span><span class="sxs-lookup"><span data-stu-id="abfa1-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="abfa1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abfa1-132">See Also</span></span>

[<span data-ttu-id="abfa1-133">**LanguageID 屬性**</span><span class="sxs-lookup"><span data-stu-id="abfa1-133">**LanguageID property**</span></span>](languageid-property.md)


 

 




