---
title: 隱藏事件
description: 隱藏事件
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840112"
---
# <a name="hide-event"></a><span data-ttu-id="bb7e0-103">隱藏事件</span><span class="sxs-lookup"><span data-stu-id="bb7e0-103">Hide Event</span></span>

<span data-ttu-id="bb7e0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bb7e0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bb7e0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="bb7e0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bb7e0-106">發生于隱藏字元時。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-106">Occurs when a character is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="bb7e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="bb7e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bb7e0-108">**子\*\*\*代理程式 \* \* \* \_ 隱藏 (* \*  **byval** *CharacterID*， **byval** *原因 \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="bb7e0-108">**Sub** *agent\*\*\*\_Hide(*\* **ByVal** *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="bb7e0-109">部分</span><span class="sxs-lookup"><span data-stu-id="bb7e0-109">Part</span></span>          | <span data-ttu-id="bb7e0-110">描述</span><span class="sxs-lookup"><span data-stu-id="bb7e0-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7e0-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="bb7e0-111">*CharacterID*</span></span> | <span data-ttu-id="bb7e0-112">以字串形式傳回隱藏字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-112">Returns the ID of the hidden character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="bb7e0-113">*原因*</span><span class="sxs-lookup"><span data-stu-id="bb7e0-113">*Cause*</span></span>       | <span data-ttu-id="bb7e0-114">傳回值，這個值會指出造成字元隱藏的原因。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-114">Returns a value that indicates what caused the character to hide.</span></span> <span data-ttu-id="bb7e0-115">1使用者藉由在字元的工作列圖示快顯功能表上選取命令，或使用語音輸入，來將字元隱藏起來。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-115">1 User hid the character by selecting the command on the character's taskbar icon pop-up menu or using speech input.</span></span><br/> <span data-ttu-id="bb7e0-116">3您的用戶端應用程式會將字元隱藏。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-116">3 Your client application hid the character.</span></span><br/> <span data-ttu-id="bb7e0-117">5另一個用戶端應用程式會將字元隱藏。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-117">5 Another client application hid the character.</span></span><br/> <span data-ttu-id="bb7e0-118">7使用者在字元的快顯功能表上選取命令以隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-118">7 User hid the character by selecting the command on the character's pop-up menu.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="bb7e0-119">備註</span><span class="sxs-lookup"><span data-stu-id="bb7e0-119">Remarks</span></span>

<span data-ttu-id="bb7e0-120">伺服器會將此事件傳送給該字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-120">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="bb7e0-121">若要查詢字元的目前狀態，請使用 [**Visible**](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="bb7e0-121">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="bb7e0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb7e0-122">See Also</span></span>

<span data-ttu-id="bb7e0-123">[**顯示事件**](show-event.md)， [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="bb7e0-123">[**Show event**](show-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





