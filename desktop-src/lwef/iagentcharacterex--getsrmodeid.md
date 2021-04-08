---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103681487"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="6c6cc-103">IAgentCharacterEx::GetSRModeID</span><span class="sxs-lookup"><span data-stu-id="6c6cc-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="6c6cc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6c6cc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="6c6cc-105">抓取為字元設定的語音辨識引擎的模式識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="6c6cc-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6c6cc-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="6c6cc-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="6c6cc-108">接收字元的語音辨識引擎模式識別碼設定之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="6c6cc-109">此設定會傳回針對字元的語音輸入所設定的引擎。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="6c6cc-110">語音辨識引擎的模式識別碼是 GUID (格式的字串表示，並以大括弧和連字號) ，由語音供應商唯一識別引擎。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="6c6cc-111">如需詳細資訊，請參閱 [Microsoft 語音 SDK 檔](https://msdn.microsoft.com/library/ee705648.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="6c6cc-112">如果您未設定字元的語音辨識引擎模式識別碼，伺服器會傳回符合字元語言設定的引擎， (使用 Microsoft 語音 API 介面) 。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="6c6cc-113">如果字元沒有相符的語音辨識引擎可供使用，則伺服器會傳回 null (空白的) 字串。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="6c6cc-114">啟用語音輸入時 (在 [先進字元選項] 視窗中) ，查詢或設定這個屬性會載入關聯的引擎 (如果尚未載入) ，然後啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="6c6cc-115">亦即，接聽鍵可供使用，而且可以顯示接聽提示。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="6c6cc-116"> (接聽金鑰和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務，且會傳回 null 字串 (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="6c6cc-117">此函數只會傳回用戶端應用程式使用字元的設定;此設定不會反映用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="6c6cc-118">如果 [**IAgentSpeechInputProperties：： GetEnabled**](iagentspeechinputproperties--getenabled.md) 傳回 **False**，則此函數不會失敗。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="6c6cc-119">Microsoft 代理程式的語音引擎需求是以 Microsoft 語音 API 為基礎。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="6c6cc-120">支援 Microsoft 代理程式的 SAPI 需求的引擎可與代理程式一起安裝和使用。</span><span class="sxs-lookup"><span data-stu-id="6c6cc-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c6cc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c6cc-121">See Also</span></span>

[<span data-ttu-id="6c6cc-122">**IAgentCharacterEx::SetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="6c6cc-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




