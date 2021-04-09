---
title: IAgentNotifySink 移動
description: IAgentNotifySink 移動
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932518"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="44ac2-103">IAgentNotifySink：： Move</span><span class="sxs-lookup"><span data-stu-id="44ac2-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="44ac2-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="44ac2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="44ac2-105">移動字元時通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="44ac2-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="44ac2-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="44ac2-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="44ac2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="44ac2-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="44ac2-108">已移動之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="44ac2-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="44ac2-109"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="44ac2-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="44ac2-110">相對於螢幕原點的新位置 x 座標（以圖元為單位）， (左上) 。</span><span class="sxs-lookup"><span data-stu-id="44ac2-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="44ac2-111">字元的位置是根據其動畫框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="44ac2-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="44ac2-112"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="44ac2-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="44ac2-113">新位置的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="44ac2-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="44ac2-114">字元的位置是根據其動畫框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="44ac2-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="44ac2-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="44ac2-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="44ac2-116">字元移動的原因。</span><span class="sxs-lookup"><span data-stu-id="44ac2-116">The cause of the character move.</span></span> <span data-ttu-id="44ac2-117">參數可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="44ac2-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="44ac2-118">值</span><span class="sxs-lookup"><span data-stu-id="44ac2-118">Value</span></span>                                                          | <span data-ttu-id="44ac2-119">描述</span><span class="sxs-lookup"><span data-stu-id="44ac2-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44ac2-120">**const 不帶正負號短** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="44ac2-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="44ac2-121">尚未移動字元。</span><span class="sxs-lookup"><span data-stu-id="44ac2-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="44ac2-122">**const 不帶正負號短** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="44ac2-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="44ac2-123">使用者拖曳字元。</span><span class="sxs-lookup"><span data-stu-id="44ac2-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="44ac2-124">**const 不帶正負號短** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="44ac2-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="44ac2-125">您的應用程式移動了該字元。</span><span class="sxs-lookup"><span data-stu-id="44ac2-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="44ac2-126">**const 不帶正負號短** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="44ac2-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="44ac2-127">另一個應用程式移動字元。</span><span class="sxs-lookup"><span data-stu-id="44ac2-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="44ac2-128">**const 不帶正負號短** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="44ac2-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="44ac2-129">伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。</span><span class="sxs-lookup"><span data-stu-id="44ac2-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="44ac2-130">此事件會傳送到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="44ac2-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="44ac2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44ac2-131">See Also</span></span>

<span data-ttu-id="44ac2-132">[**IAgentCharacter：： GetMoveCause**](iagentcharacter--getmovecause.md)， [ **IAgentCharacter：： MoveTo**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="44ac2-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 





