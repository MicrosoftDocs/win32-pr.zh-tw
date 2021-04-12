---
title: BalloonShow 事件
description: BalloonShow 事件
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372454"
---
# <a name="balloonshow-event"></a><span data-ttu-id="5d45e-103">BalloonShow 事件</span><span class="sxs-lookup"><span data-stu-id="5d45e-103">BalloonShow Event</span></span>

<span data-ttu-id="5d45e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5d45e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5d45e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="5d45e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5d45e-106">發生于顯示字元的文字批註時。</span><span class="sxs-lookup"><span data-stu-id="5d45e-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="5d45e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="5d45e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5d45e-108">**Sub** *agent* \_ **BalloonShow** **(ByVal** *CharacterID \* \* \* )*\*</span><span class="sxs-lookup"><span data-stu-id="5d45e-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="5d45e-109">部分</span><span class="sxs-lookup"><span data-stu-id="5d45e-109">Part</span></span>          | <span data-ttu-id="5d45e-110">描述</span><span class="sxs-lookup"><span data-stu-id="5d45e-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="5d45e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5d45e-111">*CharacterID*</span></span> | <span data-ttu-id="5d45e-112">傳回與文字提示字元相關聯之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d45e-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5d45e-113">備註</span><span class="sxs-lookup"><span data-stu-id="5d45e-113">Remarks</span></span>

<span data-ttu-id="5d45e-114">伺服器只會將此事件傳送給 (應用程式的用戶端，而這些應用程式已載入使用文字球的字元) 。</span><span class="sxs-lookup"><span data-stu-id="5d45e-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="5d45e-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d45e-115">See Also</span></span>

[<span data-ttu-id="5d45e-116">**BalloonHide 事件**</span><span class="sxs-lookup"><span data-stu-id="5d45e-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




