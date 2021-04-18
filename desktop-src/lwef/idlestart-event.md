---
title: IdleStart 事件
description: IdleStart 事件
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965795"
---
# <a name="idlestart-event"></a><span data-ttu-id="0c7ae-103">IdleStart 事件</span><span class="sxs-lookup"><span data-stu-id="0c7ae-103">IdleStart Event</span></span>

<span data-ttu-id="0c7ae-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0c7ae-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c7ae-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="0c7ae-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c7ae-106">當伺服器將字元設定為 **閒置** 狀態時發生。</span><span class="sxs-lookup"><span data-stu-id="0c7ae-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="0c7ae-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="0c7ae-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c7ae-108">**子\*\*\*代理程式 \* \* \* \_ IdleStart* \*  **(ByVal** *CharacterID \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="0c7ae-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="0c7ae-109">部分</span><span class="sxs-lookup"><span data-stu-id="0c7ae-109">Part</span></span>          | <span data-ttu-id="0c7ae-110">描述</span><span class="sxs-lookup"><span data-stu-id="0c7ae-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="0c7ae-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="0c7ae-111">*CharacterID*</span></span> | <span data-ttu-id="0c7ae-112">以字串形式傳回閒置字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c7ae-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="0c7ae-113">備註</span><span class="sxs-lookup"><span data-stu-id="0c7ae-113">Remarks</span></span>

<span data-ttu-id="0c7ae-114">伺服器會將此事件傳送給該字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="0c7ae-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="0c7ae-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c7ae-115">See Also</span></span>

[<span data-ttu-id="0c7ae-116">**IdleComplete 事件**</span><span class="sxs-lookup"><span data-stu-id="0c7ae-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




