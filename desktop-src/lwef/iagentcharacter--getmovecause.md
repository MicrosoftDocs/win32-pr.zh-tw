---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119681"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="12e49-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="12e49-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="12e49-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="12e49-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="12e49-105">抓取字元上一次移動的原因。</span><span class="sxs-lookup"><span data-stu-id="12e49-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="12e49-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="12e49-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="12e49-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="12e49-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="12e49-108">接收字元最後一個移動原因的變數位址，將會是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="12e49-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="12e49-109">值</span><span class="sxs-lookup"><span data-stu-id="12e49-109">Value</span></span>                                                               | <span data-ttu-id="12e49-110">描述</span><span class="sxs-lookup"><span data-stu-id="12e49-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12e49-111">**const 不帶正負號短** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="12e49-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="12e49-112">尚未移動字元。</span><span class="sxs-lookup"><span data-stu-id="12e49-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="12e49-113">**const 不帶正負號短** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="12e49-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="12e49-114">使用者拖曳字元。</span><span class="sxs-lookup"><span data-stu-id="12e49-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="12e49-115">**const 不帶正負號短** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="12e49-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="12e49-116">您的應用程式移動了該字元。</span><span class="sxs-lookup"><span data-stu-id="12e49-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="12e49-117">**const 不帶正負號短** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="12e49-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="12e49-118">另一個應用程式移動字元。</span><span class="sxs-lookup"><span data-stu-id="12e49-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="12e49-119">**const 不帶正負號短** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="12e49-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="12e49-120">伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。</span><span class="sxs-lookup"><span data-stu-id="12e49-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="12e49-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e49-121">See Also</span></span>

[<span data-ttu-id="12e49-122">**IAgentNotifySink：： Move**</span><span class="sxs-lookup"><span data-stu-id="12e49-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





