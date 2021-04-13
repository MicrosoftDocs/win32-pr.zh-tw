---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374658"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="3b33a-103">IAgentCharacterEx::SetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="3b33a-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="3b33a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3b33a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="3b33a-105">設定為字元設定的 TTS 引擎的模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b33a-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="3b33a-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="3b33a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3b33a-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span><span class="sxs-lookup"><span data-stu-id="3b33a-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="3b33a-108">此字元之 TTS 引擎的模式識別碼設定。</span><span class="sxs-lookup"><span data-stu-id="3b33a-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="3b33a-109">**IAgentCharacterEx：** 如果未安裝 Speech.dll，且您指定的引擎不符合字元的編譯 TTS 模式設定，SetTTSModeID 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b33a-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="3b33a-110">此設定會決定字元的朗讀 TTS 輸出的慣用引擎模式。</span><span class="sxs-lookup"><span data-stu-id="3b33a-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="3b33a-111">TTS (文字轉換語音) 引擎的模式識別碼是語音供應商定義的 GUID，可唯一識別引擎的模式 (以大括弧和連字號) 格式化。</span><span class="sxs-lookup"><span data-stu-id="3b33a-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="3b33a-112">如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3b33a-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="3b33a-113">如果您設定了 TTS 模式識別碼，它會根據字元編譯的 TTS 模式識別碼、目前的系統語言識別項和字元目前的語言識別項，覆寫伺服器嘗試比對語音引擎。</span><span class="sxs-lookup"><span data-stu-id="3b33a-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="3b33a-114">但是，如果您嘗試在使用者停用 Microsoft Agent 屬性工作表中的語音輸出或未安裝相關聯的引擎時，設定模式識別碼，此呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b33a-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="3b33a-115">如果您沒有為字元設定 TTS 引擎模式識別碼，則伺服器會設定符合字元語言設定的引擎， (使用 Microsoft 語音 API 介面) 。</span><span class="sxs-lookup"><span data-stu-id="3b33a-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="3b33a-116">如果尚未載入相關聯的引擎，則設定這個屬性會載入相關聯的引擎。</span><span class="sxs-lookup"><span data-stu-id="3b33a-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="3b33a-117">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3b33a-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="3b33a-118">Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。</span><span class="sxs-lookup"><span data-stu-id="3b33a-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="3b33a-119">支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。</span><span class="sxs-lookup"><span data-stu-id="3b33a-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b33a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b33a-120">See Also</span></span>

[<span data-ttu-id="3b33a-121">**IAgentCharacterEx:GetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="3b33a-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




