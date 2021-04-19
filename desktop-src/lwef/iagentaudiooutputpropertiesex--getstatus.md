---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380742"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="92972-103">IAgentAudioOutputPropertiesEx：： GetStatus</span><span class="sxs-lookup"><span data-stu-id="92972-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="92972-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="92972-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="92972-105">捕獲音訊通道的狀態。</span><span class="sxs-lookup"><span data-stu-id="92972-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="92972-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="92972-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="92972-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="92972-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="92972-108">音訊輸出通道的狀態，它可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="92972-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="92972-109">值</span><span class="sxs-lookup"><span data-stu-id="92972-109">Value</span></span>                                                                         | <span data-ttu-id="92972-110">描述</span><span class="sxs-lookup"><span data-stu-id="92972-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92972-111">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ 可用 = 0;**</span><span class="sxs-lookup"><span data-stu-id="92972-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="92972-112">音訊輸出通道可用 () 不會忙碌。</span><span class="sxs-lookup"><span data-stu-id="92972-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="92972-113">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ NOAUDIO = 1;**</span><span class="sxs-lookup"><span data-stu-id="92972-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="92972-114">不支援音訊輸出;例如，因為沒有音效卡。</span><span class="sxs-lookup"><span data-stu-id="92972-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="92972-115">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ CANTOPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="92972-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="92972-116">無法開啟音訊輸出通道 (忙碌中) ;例如，因為另一個應用程式現正播放音訊。</span><span class="sxs-lookup"><span data-stu-id="92972-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="92972-117">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ USERSPEAKING = 3;**</span><span class="sxs-lookup"><span data-stu-id="92972-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="92972-118">音訊輸出通道忙碌中，因為伺服器正在處理使用者語音輸入</span><span class="sxs-lookup"><span data-stu-id="92972-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="92972-119">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="92972-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="92972-120">音訊輸出通道正在忙碌中，因為字元目前正在說話中。</span><span class="sxs-lookup"><span data-stu-id="92972-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="92972-121">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="92972-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="92972-122">音訊輸出通道不在忙碌中，但正在等候使用者語音輸入。</span><span class="sxs-lookup"><span data-stu-id="92972-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="92972-123">**const 不帶正負號的短\*\*\*\*音訊 \_ 狀態 \_ 錯誤 = 6;**</span><span class="sxs-lookup"><span data-stu-id="92972-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="92972-124">嘗試存取音訊輸出通道時發生一些其他 (未知的) 問題。</span><span class="sxs-lookup"><span data-stu-id="92972-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="92972-125">這項設定可讓您的用戶端應用程式查詢音訊輸出通道的狀態。</span><span class="sxs-lookup"><span data-stu-id="92972-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="92972-126">您可以使用此資訊來判斷是否要使用 **IAgentCharacterEx：：接聽**) 來說出要使用的字元，或嘗試開啟接聽模式 (。</span><span class="sxs-lookup"><span data-stu-id="92972-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using **IAgentCharacterEx::Listen**).</span></span>

 

 





