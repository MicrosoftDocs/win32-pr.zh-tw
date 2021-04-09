---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021262"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="3076d-103">IAgentCharacterEx::GetSRStatus</span><span class="sxs-lookup"><span data-stu-id="3076d-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="3076d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3076d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="3076d-105">抓取支援語音輸入所需的條件狀態。</span><span class="sxs-lookup"><span data-stu-id="3076d-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="3076d-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="3076d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3076d-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="3076d-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="3076d-108">變數的位址，此變數會接收狀態設定的下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3076d-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="3076d-109">值</span><span class="sxs-lookup"><span data-stu-id="3076d-109">Value</span></span>                                                                               | <span data-ttu-id="3076d-110">描述</span><span class="sxs-lookup"><span data-stu-id="3076d-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3076d-111">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ CANLISTEN = 0;**</span><span class="sxs-lookup"><span data-stu-id="3076d-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="3076d-112">條件支援語音輸入。</span><span class="sxs-lookup"><span data-stu-id="3076d-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="3076d-113">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ NOAUDIO = 1;**</span><span class="sxs-lookup"><span data-stu-id="3076d-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="3076d-114">此系統上沒有可用的音訊輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="3076d-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="3076d-115"> (請注意，這不會偵測是否已安裝麥克風;它只能偵測使用者是否已安裝具有正常運作驅動程式的已啟用輸入的音效卡。 ) </span><span class="sxs-lookup"><span data-stu-id="3076d-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="3076d-116">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ NOTTOPMOST = 2;**</span><span class="sxs-lookup"><span data-stu-id="3076d-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="3076d-117">另一個用戶端是此字元的作用中用戶端，或目前的字元不是最上層。</span><span class="sxs-lookup"><span data-stu-id="3076d-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="3076d-118">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ CANTOPENAUDIO = 3;**</span><span class="sxs-lookup"><span data-stu-id="3076d-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="3076d-119">音訊輸入或輸出通道目前忙碌中，其他應用程式正在使用音訊。</span><span class="sxs-lookup"><span data-stu-id="3076d-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="3076d-120">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ COULDNTINITIALIZESPEECH = 4;**</span><span class="sxs-lookup"><span data-stu-id="3076d-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="3076d-121">初始化語音辨識子系統的過程中發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3076d-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="3076d-122">這包括沒有任何語音引擎可符合字元語言設定的可能性。</span><span class="sxs-lookup"><span data-stu-id="3076d-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="3076d-123">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ SPEECHDISABLED = 5;**</span><span class="sxs-lookup"><span data-stu-id="3076d-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="3076d-124">使用者已在 [先進字元選項] 視窗中停用語音輸入。</span><span class="sxs-lookup"><span data-stu-id="3076d-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="3076d-125">**const 不帶正負號的 long** **接聽 \_ 狀態 \_ 錯誤 = 6;**</span><span class="sxs-lookup"><span data-stu-id="3076d-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="3076d-126">檢查音訊狀態時發生錯誤，但系統不會傳回錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="3076d-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="3076d-127">此函數可讓您查詢目前的條件是否支援語音辨識輸入，包括音訊裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="3076d-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="3076d-128">如果您的應用程式使用 [**IAgentCharacterEx：：接聽**](iagentcharacterex--listen.md) 方法，您可以使用此函式，以確保呼叫會成功。</span><span class="sxs-lookup"><span data-stu-id="3076d-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="3076d-129">呼叫這個方法也會載入語音引擎（如果尚未載入）。</span><span class="sxs-lookup"><span data-stu-id="3076d-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="3076d-130">但是，它不會開啟接聽模式。</span><span class="sxs-lookup"><span data-stu-id="3076d-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="3076d-131">在 [代理程式] 屬性工作表中啟用語音輸入時 ([Advanced Character Options]) ，查詢狀態將會載入相關聯的引擎 (如果尚未載入) ，然後啟動 [語音服務]。</span><span class="sxs-lookup"><span data-stu-id="3076d-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="3076d-132">亦即，接聽鍵可供使用，而且可以顯示接聽提示。</span><span class="sxs-lookup"><span data-stu-id="3076d-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="3076d-133"> (接聽鍵和接聽提示只會在先進的字元選項中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="3076d-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="3076d-134">此函數只會傳回用戶端應用程式使用字元的設定;此設定不會反映用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3076d-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





