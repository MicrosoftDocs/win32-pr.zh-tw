---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462716"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="892f9-103">IAgentCharacterEx::SetSRModeID</span><span class="sxs-lookup"><span data-stu-id="892f9-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="892f9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="892f9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="892f9-105">設定為字元設定的語音辨識引擎的模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="892f9-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="892f9-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="892f9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="892f9-107">bszModeID</span><span class="sxs-lookup"><span data-stu-id="892f9-107">bszModeID</span></span>

<span data-ttu-id="892f9-108">字元的語音辨識引擎的模式識別碼設定。</span><span class="sxs-lookup"><span data-stu-id="892f9-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="892f9-109">此設定會設定字元語音輸入的引擎。</span><span class="sxs-lookup"><span data-stu-id="892f9-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="892f9-110">語音辨識引擎的模式識別碼是語音供應商定義的 GUID，可唯一識別引擎的模式 (使用大括弧和連字號) 來格式化。</span><span class="sxs-lookup"><span data-stu-id="892f9-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="892f9-111">如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。</span><span class="sxs-lookup"><span data-stu-id="892f9-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="892f9-112">如果您指定的模式識別碼不符合字元的語言設定，則如果使用者已停用 [Microsoft 代理程式] 屬性工作表中的 [語音辨識] () ，或未安裝引擎，此呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="892f9-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="892f9-113">如果您未設定字元的語音辨識引擎模式識別碼，伺服器會將符合字元語言設定的識別碼， (使用 Microsoft 語音 API 介面) 。</span><span class="sxs-lookup"><span data-stu-id="892f9-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="892f9-114">在 [代理程式] 屬性工作表中啟用語音輸入時 ([Advanced Character Options]) ，設定此屬性會載入相關聯的引擎 (如果尚未載入) ，然後啟動 [語音服務]。</span><span class="sxs-lookup"><span data-stu-id="892f9-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="892f9-115">亦即，接聽鍵可供使用，而且可以顯示接聽提示。</span><span class="sxs-lookup"><span data-stu-id="892f9-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="892f9-116"> (接聽鍵和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="892f9-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="892f9-117">這個屬性只適用于字元的用戶端;此設定不會反映其他用戶端的其他字元或用戶端字元的設定。</span><span class="sxs-lookup"><span data-stu-id="892f9-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="892f9-118">Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。</span><span class="sxs-lookup"><span data-stu-id="892f9-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="892f9-119">支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。</span><span class="sxs-lookup"><span data-stu-id="892f9-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="892f9-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="892f9-120">See Also</span></span>

[<span data-ttu-id="892f9-121">**IAgentCharacterEx::GetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="892f9-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




