---
title: IdleComplete 事件
description: IdleComplete 事件
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020709"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="f1d04-103">IdleComplete 事件</span><span class="sxs-lookup"><span data-stu-id="f1d04-103">IdleComplete Event</span></span>

<span data-ttu-id="f1d04-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f1d04-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f1d04-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="f1d04-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f1d04-106">當伺服器結束字元的 **閒置** 狀態時發生。</span><span class="sxs-lookup"><span data-stu-id="f1d04-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="f1d04-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="f1d04-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f1d04-108">**子\*\*\*代理程式 \* \* \* \_ IdleComplete* \*  **(ByVal** *CharacterID \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="f1d04-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="f1d04-109">部分</span><span class="sxs-lookup"><span data-stu-id="f1d04-109">Part</span></span>          | <span data-ttu-id="f1d04-110">描述</span><span class="sxs-lookup"><span data-stu-id="f1d04-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="f1d04-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="f1d04-111">*CharacterID*</span></span> | <span data-ttu-id="f1d04-112">以字串形式傳回閒置字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1d04-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="f1d04-113">備註</span><span class="sxs-lookup"><span data-stu-id="f1d04-113">Remarks</span></span>

<span data-ttu-id="f1d04-114">伺服器會將此事件傳送給該字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="f1d04-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="f1d04-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1d04-115">See Also</span></span>

[<span data-ttu-id="f1d04-116">**IdleStart 事件**</span><span class="sxs-lookup"><span data-stu-id="f1d04-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




