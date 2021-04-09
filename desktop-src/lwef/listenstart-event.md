---
title: ListenStart 事件
description: ListenStart 事件
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840672"
---
# <a name="listenstart-event"></a><span data-ttu-id="8cdaa-103">ListenStart 事件</span><span class="sxs-lookup"><span data-stu-id="8cdaa-103">ListenStart Event</span></span>

<span data-ttu-id="8cdaa-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8cdaa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8cdaa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="8cdaa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8cdaa-106">當接聽模式 (語音辨識) 開始時發生。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="8cdaa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="8cdaa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8cdaa-108">**子\*\*\*代理程式。 \* \* \* ListenStart (ByVal* \*  *CharacterID \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="8cdaa-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="8cdaa-109">部分</span><span class="sxs-lookup"><span data-stu-id="8cdaa-109">Part</span></span>          | <span data-ttu-id="8cdaa-110">描述</span><span class="sxs-lookup"><span data-stu-id="8cdaa-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="8cdaa-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="8cdaa-111">*CharacterID*</span></span> | <span data-ttu-id="8cdaa-112">以字串形式傳回接聽字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8cdaa-113">備註</span><span class="sxs-lookup"><span data-stu-id="8cdaa-113">Remarks</span></span>

<span data-ttu-id="8cdaa-114">此事件會在接聽模式開始時傳送至所有用戶端，因為使用者按下接聽鍵或輸入主動用戶端，並以 **True** 呼叫 [**接聽**](listen-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="8cdaa-115">您可以使用此事件來避免在接聽模式開啟時，讓您的字元說話。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="8cdaa-116">如果您使用 [**接聽**](listen-method.md) 方法開啟接聽模式，然後使用者按下接聽鍵，則接聽模式會重設並繼續進行，直到接聽的金鑰超時時間完成、接聽的金鑰已釋出或使用者已完成說話（以稍後的何者為准）。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="8cdaa-117">在此情況下，當接聽模式已開啟時，當使用者按下接聽鍵時，您將不會收到額外的 **ListenStart** 事件。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="8cdaa-118">此事件會將字元傳回給目前已載入此字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="8cdaa-119">所有其他用戶端都會收到 null 字元， (空的字串) 。</span><span class="sxs-lookup"><span data-stu-id="8cdaa-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="8cdaa-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cdaa-120">See Also</span></span>

<span data-ttu-id="8cdaa-121">[**ListenComplete 事件**](listencomplete-event.md)， [**接聽方法**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="8cdaa-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




