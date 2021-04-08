---
title: SRStatus 屬性
description: SRStatus 屬性
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022116"
---
# <a name="srstatus-property"></a><span data-ttu-id="2d7a2-103">SRStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="2d7a2-103">SRStatus Property</span></span>

<span data-ttu-id="2d7a2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2d7a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2d7a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="2d7a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2d7a2-106">傳回是否可針對字元啟動語音輸入。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="2d7a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="2d7a2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2d7a2-108">*代理。\*\*\*字元 (*\*\* 」CharacterID \* \* \* ) 。SRStatus\*\*</span><span class="sxs-lookup"><span data-stu-id="2d7a2-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="2d7a2-109">值</span><span class="sxs-lookup"><span data-stu-id="2d7a2-109">Value</span></span> | <span data-ttu-id="2d7a2-110">描述</span><span class="sxs-lookup"><span data-stu-id="2d7a2-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7a2-111">0</span><span class="sxs-lookup"><span data-stu-id="2d7a2-111">0</span></span>     | <span data-ttu-id="2d7a2-112">條件支援語音輸入。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="2d7a2-113">1</span><span class="sxs-lookup"><span data-stu-id="2d7a2-113">1</span></span>     | <span data-ttu-id="2d7a2-114">此系統上沒有可用的音訊輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="2d7a2-115"> (請注意，這不會偵測是否已安裝麥克風;它只能偵測使用者是否已安裝具有正常運作驅動程式的已啟用輸入的音效卡。 ) </span><span class="sxs-lookup"><span data-stu-id="2d7a2-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="2d7a2-116">2</span><span class="sxs-lookup"><span data-stu-id="2d7a2-116">2</span></span>     | <span data-ttu-id="2d7a2-117">另一個用戶端是此字元的作用中用戶端，或目前的字元不是最上層。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="2d7a2-118">3</span><span class="sxs-lookup"><span data-stu-id="2d7a2-118">3</span></span>     | <span data-ttu-id="2d7a2-119">音訊輸入或輸出通道目前忙碌中，應用程式正在使用音訊。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="2d7a2-120">4</span><span class="sxs-lookup"><span data-stu-id="2d7a2-120">4</span></span>     | <span data-ttu-id="2d7a2-121">初始化語音辨識子系統的過程中發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="2d7a2-122">這包括沒有任何語音引擎可符合字元語言設定的可能性。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="2d7a2-123">5</span><span class="sxs-lookup"><span data-stu-id="2d7a2-123">5</span></span>     | <span data-ttu-id="2d7a2-124">使用者已停用 Advanced Character 選項中的語音輸入。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="2d7a2-125">6</span><span class="sxs-lookup"><span data-stu-id="2d7a2-125">6</span></span>     | <span data-ttu-id="2d7a2-126">檢查音訊狀態時發生錯誤，但系統不會傳回錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d7a2-127">備註</span><span class="sxs-lookup"><span data-stu-id="2d7a2-127">Remarks</span></span>

<span data-ttu-id="2d7a2-128">這個屬性會傳回支援語音輸入所需的條件，包括音訊裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="2d7a2-129">您可以先檢查這個屬性，然後再呼叫 [**接聽**](listen-method.md) 方法，以更妥善地確保其成功。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="2d7a2-130">在 [代理程式] 屬性工作表中啟用語音輸入時 ([Advanced Character Options]) ，查詢此屬性將會載入相關聯的引擎（如果尚未載入），並啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="2d7a2-131">亦即，接聽鍵可供使用，而且接聽提示會自動顯示。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="2d7a2-132"> (接聽金鑰和接聽提示只會在 [高階字元選項] 中啟用時才會啟用 ) 。不過，如果您在停用語音時查詢屬性，伺服器就不會啟動語音服務。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="2d7a2-133">這個屬性只適用于用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d7a2-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d7a2-134">See Also</span></span>

[<span data-ttu-id="2d7a2-135">**接聽方法**</span><span class="sxs-lookup"><span data-stu-id="2d7a2-135">**Listen method**</span></span>](listen-method.md)


 

 




