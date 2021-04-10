---
title: ActiveClientChange 事件
description: ActiveClientChange 事件
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183500"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="b21bd-103">ActiveClientChange 事件</span><span class="sxs-lookup"><span data-stu-id="b21bd-103">ActiveClientChange Event</span></span>

<span data-ttu-id="b21bd-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b21bd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b21bd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="b21bd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b21bd-106">當字元的作用中用戶端變更時發生。</span><span class="sxs-lookup"><span data-stu-id="b21bd-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="b21bd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="b21bd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b21bd-108">\**子\*\*\*代理程式。* ActiveClientChange (ByVal *CharacterID*，byval *主動* **)**</span><span class="sxs-lookup"><span data-stu-id="b21bd-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="b21bd-109">部分</span><span class="sxs-lookup"><span data-stu-id="b21bd-109">Part</span></span>          | <span data-ttu-id="b21bd-110">描述</span><span class="sxs-lookup"><span data-stu-id="b21bd-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b21bd-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="b21bd-111">*CharacterID*</span></span> | <span data-ttu-id="b21bd-112">傳回發生事件之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b21bd-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="b21bd-113">*使用中*</span><span class="sxs-lookup"><span data-stu-id="b21bd-113">*Active*</span></span>      | <span data-ttu-id="b21bd-114">指出用戶端是否為作用中或非作用中的布林值。</span><span class="sxs-lookup"><span data-stu-id="b21bd-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="b21bd-115">**True** 用戶端應用程式成為字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="b21bd-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="b21bd-116">**False** 用戶端應用程式不再是字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="b21bd-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="b21bd-117">備註</span><span class="sxs-lookup"><span data-stu-id="b21bd-117">Remarks</span></span>

<span data-ttu-id="b21bd-118">當多個用戶端應用程式共用相同的字元時，字元的作用中用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。</span><span class="sxs-lookup"><span data-stu-id="b21bd-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="b21bd-119">同樣地，當顯示多個字元時，最上層字元的作用中用戶端 (也稱為輸入-主動用戶端) 接收 [命令](command-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="b21bd-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="b21bd-120">當使用中用戶端的字元變更時，此事件會傳回該字元的識別碼，如果您的應用程式已成為字元的作用中用戶端， **則為 True** ; 如果不再是字元的作用中用戶端，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="b21bd-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="b21bd-121">當使用者在字元的快顯功能表中選取用戶端應用程式的專案時，或在用戶端應用程式變更其作用中狀態，或當其他用戶端應用程式結束其代理程式的連接時，用戶端應用程式可能會收到此事件。</span><span class="sxs-lookup"><span data-stu-id="b21bd-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="b21bd-122">代理程式只會將此事件傳送給直接受影響的用戶端應用程式;這會成為作用中的用戶端，或停止成為作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="b21bd-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="b21bd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b21bd-123">See Also</span></span>

<span data-ttu-id="b21bd-124">[\* \* \* \* ActivateInput \* \* event \* \*](activateinput-event.md)、\* \* \* \* [Active \* \* property \* \*](active-property.md)、 [\* \* \* \* DeactivateInput \* \* event \* \*](deactivateinput-event.md)、 [\* \* \* \* Activate \* \* 方法 \*](activate-method.md) \*</span><span class="sxs-lookup"><span data-stu-id="b21bd-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





