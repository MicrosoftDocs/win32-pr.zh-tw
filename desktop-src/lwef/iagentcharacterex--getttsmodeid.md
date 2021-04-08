---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023119"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="1a3df-103">IAgentCharacterEx::GetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="1a3df-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="1a3df-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1a3df-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="1a3df-105">抓取為字元設定的 TTS 引擎的模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a3df-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="1a3df-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1a3df-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1a3df-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="1a3df-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="1a3df-108">接收字元之 TTS 引擎的模式識別碼設定之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="1a3df-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="1a3df-109">此設定會針對字元的語音輸出，傳回 (文字轉換語音) 引擎模式識別碼的 TTS。</span><span class="sxs-lookup"><span data-stu-id="1a3df-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="1a3df-110">TTS 引擎的模式識別碼是 GUID 的字串表示， (以大括弧和連字號來格式化，) 由語音廠商所定義，以唯一識別引擎。</span><span class="sxs-lookup"><span data-stu-id="1a3df-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="1a3df-111">如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1a3df-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="1a3df-112">如果尚未載入相關聯的引擎，則查詢此屬性會載入相關聯的引擎。</span><span class="sxs-lookup"><span data-stu-id="1a3df-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="1a3df-113">如果您沒有為字元設定 TTS 引擎模式識別碼，伺服器會嘗試傳回符合 (使用 Microsoft 語音 API 介面的引擎，) 字元的編譯的 TTS 設定和字元的目前語言設定。</span><span class="sxs-lookup"><span data-stu-id="1a3df-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="1a3df-114">如果這些不同，則字元的語言設定會覆寫其撰寫的模式設定。</span><span class="sxs-lookup"><span data-stu-id="1a3df-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="1a3df-115">如果您未設定字元的語言設定，則字元的語言會是使用者預設語言識別項，而伺服器會根據該語言識別項來嘗試相符。</span><span class="sxs-lookup"><span data-stu-id="1a3df-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="1a3df-116">如果 [**IAgentAudioObjectProperties：： GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) 傳回 **False**，則此函數不會失敗。</span><span class="sxs-lookup"><span data-stu-id="1a3df-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="1a3df-117">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="1a3df-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="1a3df-118">Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。</span><span class="sxs-lookup"><span data-stu-id="1a3df-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="1a3df-119">支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。</span><span class="sxs-lookup"><span data-stu-id="1a3df-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a3df-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a3df-120">See Also</span></span>

[<span data-ttu-id="1a3df-121">**IAgentCharacterEx::SetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="1a3df-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




