---
title: ListenComplete 事件
description: ListenComplete 事件
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372548"
---
# <a name="listencomplete-event"></a><span data-ttu-id="43fd8-103">ListenComplete 事件</span><span class="sxs-lookup"><span data-stu-id="43fd8-103">ListenComplete Event</span></span>

<span data-ttu-id="43fd8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="43fd8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="43fd8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="43fd8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="43fd8-106">當接聽模式 (語音辨識) 結束時發生。</span><span class="sxs-lookup"><span data-stu-id="43fd8-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="43fd8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="43fd8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="43fd8-108">**子\*\*\*代理程式。 \* \* \* ListenComplete (byval* \*  *CharacterID*， **byval** *原因 \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="43fd8-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="43fd8-109">部分</span><span class="sxs-lookup"><span data-stu-id="43fd8-109">Part</span></span>          | <span data-ttu-id="43fd8-110">描述</span><span class="sxs-lookup"><span data-stu-id="43fd8-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43fd8-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="43fd8-111">*CharacterID*</span></span> | <span data-ttu-id="43fd8-112">以字串形式傳回接聽字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43fd8-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="43fd8-113">*原因*</span><span class="sxs-lookup"><span data-stu-id="43fd8-113">*Cause*</span></span>       | <span data-ttu-id="43fd8-114">以整數形式傳回完整事件的原因，可能是下列其中一項：已由程式碼關閉1個接聽模式。</span><span class="sxs-lookup"><span data-stu-id="43fd8-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="43fd8-115">程式碼) 超時， (開啟了2個接聽模式。</span><span class="sxs-lookup"><span data-stu-id="43fd8-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="43fd8-116"> (由接聽鍵開啟3個接聽模式) 超時。</span><span class="sxs-lookup"><span data-stu-id="43fd8-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="43fd8-117">因為使用者已釋放接聽金鑰，所以已關閉4個接聽模式。</span><span class="sxs-lookup"><span data-stu-id="43fd8-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="43fd8-118">5個接聽模式已結束，因為使用者已完成說話。</span><span class="sxs-lookup"><span data-stu-id="43fd8-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="43fd8-119">6個接聽模式已結束，因為輸入-主動用戶端已停用。</span><span class="sxs-lookup"><span data-stu-id="43fd8-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="43fd8-120">7接聽模式已結束，因為預設字元已變更。</span><span class="sxs-lookup"><span data-stu-id="43fd8-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="43fd8-121">8接聽模式已結束，因為使用者已停用語音輸入。</span><span class="sxs-lookup"><span data-stu-id="43fd8-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="43fd8-122">備註</span><span class="sxs-lookup"><span data-stu-id="43fd8-122">Remarks</span></span>

<span data-ttu-id="43fd8-123">此事件會在接聽模式超時結束、使用者放開接聽金鑰之後、輸入作用中用戶端以 **False** 呼叫 [**接聽**](listen-method.md)方法，或使用者已完成說話時，傳送至所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="43fd8-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="43fd8-124">您可以使用此事件來判斷何時繼續 (音訊) 輸出的字元。</span><span class="sxs-lookup"><span data-stu-id="43fd8-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="43fd8-125">如果您使用 [**接聽**](listen-method.md) 方法開啟接聽模式，然後使用者按下接聽鍵，則接聽模式會重設並繼續進行，直到接聽的金鑰超時時間完成、接聽的金鑰已釋出，或使用者已完成說話（以較晚者為准）。</span><span class="sxs-lookup"><span data-stu-id="43fd8-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="43fd8-126">在此情況下，您將不會收到 **ListenComplete** 事件，直到接聽鍵的模式完成為止。</span><span class="sxs-lookup"><span data-stu-id="43fd8-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="43fd8-127">此事件會將字元傳回給目前已載入此字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="43fd8-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="43fd8-128">所有其他用戶端都會收到 null 字元， (空的字串) 。</span><span class="sxs-lookup"><span data-stu-id="43fd8-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="43fd8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43fd8-129">See Also</span></span>

<span data-ttu-id="43fd8-130">[**ListenStart 事件**](listenstart-event.md)， [**接聽方法**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="43fd8-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





