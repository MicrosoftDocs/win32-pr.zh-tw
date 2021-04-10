---
title: AgentPropertyChange 事件
description: AgentPropertyChange 事件
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021230"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="918b2-103">AgentPropertyChange 事件</span><span class="sxs-lookup"><span data-stu-id="918b2-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="918b2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="918b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="918b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="918b2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="918b2-106">發生于使用者變更 [先進字元選項] 視窗中的屬性時。</span><span class="sxs-lookup"><span data-stu-id="918b2-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="918b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="918b2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="918b2-108">**子\*\*\*代理程式。 \* \* \* AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="918b2-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="918b2-109">備註</span><span class="sxs-lookup"><span data-stu-id="918b2-109">Remarks</span></span>

<span data-ttu-id="918b2-110">此事件表示使用者已變更並套用 [Advanced Character] 選項視窗中包含的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="918b2-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="918b2-111">在處理此事件的程式碼中，您可以查詢 [AudioOutput](the-audiooutput-object.md) 或 [SpeechInput](the-speechinput-object.md) 物件的特定屬性設定。</span><span class="sxs-lookup"><span data-stu-id="918b2-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="918b2-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="918b2-112">See Also</span></span>

[<span data-ttu-id="918b2-113">**DefaultCharacterChange 事件**</span><span class="sxs-lookup"><span data-stu-id="918b2-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




