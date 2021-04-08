---
title: 顯示事件
description: 顯示事件
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839655"
---
# <a name="show-event"></a><span data-ttu-id="2b214-103">顯示事件</span><span class="sxs-lookup"><span data-stu-id="2b214-103">Show Event</span></span>

<span data-ttu-id="2b214-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2b214-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2b214-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="2b214-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2b214-106">發生于顯示字元時。</span><span class="sxs-lookup"><span data-stu-id="2b214-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="2b214-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="2b214-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2b214-108">**子\*\*\*代理程式 \* \* \* \_ 顯示 (byval* \*  *CharacterID*， **byval** *原因 \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="2b214-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="2b214-109">部分</span><span class="sxs-lookup"><span data-stu-id="2b214-109">Part</span></span>          | <span data-ttu-id="2b214-110">描述</span><span class="sxs-lookup"><span data-stu-id="2b214-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b214-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="2b214-111">*CharacterID*</span></span> | <span data-ttu-id="2b214-112">傳回顯示為字串之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b214-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="2b214-113">*原因*</span><span class="sxs-lookup"><span data-stu-id="2b214-113">*Cause*</span></span>       | <span data-ttu-id="2b214-114">傳回值，這個值會指出造成字元顯示的原因。</span><span class="sxs-lookup"><span data-stu-id="2b214-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="2b214-115">2使用者使用功能表或語音命令) 顯示字元 (。</span><span class="sxs-lookup"><span data-stu-id="2b214-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="2b214-116">4您的用戶端應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="2b214-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="2b214-117">6另一個用戶端應用程式顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="2b214-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="2b214-118">備註</span><span class="sxs-lookup"><span data-stu-id="2b214-118">Remarks</span></span>

<span data-ttu-id="2b214-119">伺服器會將此事件傳送給該字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="2b214-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="2b214-120">若要查詢字元的目前狀態，請使用 [**Visible**](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2b214-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="2b214-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b214-121">See Also</span></span>

<span data-ttu-id="2b214-122">[**隱藏事件**](hide-event.md)， [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="2b214-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





