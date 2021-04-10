---
title: BalloonHide 事件
description: BalloonHide 事件
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184030"
---
# <a name="balloonhide-event"></a><span data-ttu-id="46085-103">BalloonHide 事件</span><span class="sxs-lookup"><span data-stu-id="46085-103">BalloonHide Event</span></span>

<span data-ttu-id="46085-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="46085-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="46085-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="46085-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="46085-106">發生于隱藏字元的文字批註時。</span><span class="sxs-lookup"><span data-stu-id="46085-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="46085-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="46085-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="46085-108">**Sub** *agent* \_ **BalloonHide** **(ByVal** *CharacterID \* \* \* )*\*</span><span class="sxs-lookup"><span data-stu-id="46085-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="46085-109">部分</span><span class="sxs-lookup"><span data-stu-id="46085-109">Part</span></span>          | <span data-ttu-id="46085-110">描述</span><span class="sxs-lookup"><span data-stu-id="46085-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="46085-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="46085-111">*CharacterID*</span></span> | <span data-ttu-id="46085-112">傳回與文字提示字元相關聯之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="46085-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="46085-113">備註</span><span class="sxs-lookup"><span data-stu-id="46085-113">Remarks</span></span>

<span data-ttu-id="46085-114">伺服器只會將此事件傳送給 (應用程式的用戶端，而這些應用程式已載入使用文字球的字元) 。</span><span class="sxs-lookup"><span data-stu-id="46085-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="46085-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46085-115">See Also</span></span>

[<span data-ttu-id="46085-116">**BalloonShow 事件**</span><span class="sxs-lookup"><span data-stu-id="46085-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




