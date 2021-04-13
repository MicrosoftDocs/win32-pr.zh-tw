---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372694"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="908d8-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="908d8-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="908d8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="908d8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="908d8-105">抓取字元上一次移動的原因。</span><span class="sxs-lookup"><span data-stu-id="908d8-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="908d8-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="908d8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="908d8-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="908d8-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="908d8-108">接收字元最後一個移動原因的變數位址，將會是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="908d8-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="908d8-109">**const 不帶正負號短** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="908d8-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="908d8-110">尚未移動字元。</span><span class="sxs-lookup"><span data-stu-id="908d8-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="908d8-111">**const 不帶正負號短** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="908d8-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="908d8-112">使用者拖曳字元。</span><span class="sxs-lookup"><span data-stu-id="908d8-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="908d8-113">**const 不帶正負號短** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="908d8-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="908d8-114">您的應用程式移動了該字元。</span><span class="sxs-lookup"><span data-stu-id="908d8-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="908d8-115">**const 不帶正負號短** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="908d8-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="908d8-116">另一個應用程式移動字元。</span><span class="sxs-lookup"><span data-stu-id="908d8-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="908d8-117">**const 不帶正負號短** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="908d8-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="908d8-118">伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。</span><span class="sxs-lookup"><span data-stu-id="908d8-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="908d8-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="908d8-119">See Also</span></span>

[<span data-ttu-id="908d8-120">**IAgentNotifySink：： Move**</span><span class="sxs-lookup"><span data-stu-id="908d8-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





