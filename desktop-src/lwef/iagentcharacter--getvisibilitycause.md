---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372690"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="7e2f9-103">IAgentCharacter::GetVisibilityCause</span><span class="sxs-lookup"><span data-stu-id="7e2f9-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="7e2f9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7e2f9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="7e2f9-105">捕獲字元可見狀態的原因。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="7e2f9-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7e2f9-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="7e2f9-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="7e2f9-108">接收字元上一次可見度狀態變更之原因的變數位址，將會是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="7e2f9-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="7e2f9-109">值</span><span class="sxs-lookup"><span data-stu-id="7e2f9-109">Value</span></span>                                                                   | <span data-ttu-id="7e2f9-110">描述</span><span class="sxs-lookup"><span data-stu-id="7e2f9-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2f9-111">**const 不帶正負號短** **NeverShown = 0;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="7e2f9-112">未顯示字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="7e2f9-113">**const 不帶正負號短** **UserHid = 1;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="7e2f9-114">使用者以字元的工作列圖示快顯功能表或使用語音輸入來隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="7e2f9-115">**const 不帶正負號短** **UserShowed = 2;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="7e2f9-116">使用者顯示字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="7e2f9-117">**const 不帶正負號短** **ProgramHid = 3;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="7e2f9-118">您的應用程式會隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="7e2f9-119">**const 不帶正負號短** **ProgramShowed = 4;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="7e2f9-120">您的應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="7e2f9-121">**const 不帶正負號短** **OtherProgramHid = 5;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="7e2f9-122">另一個應用程式會將字元隱藏。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="7e2f9-123">**const 不帶正負號短** **OtherProgramShowed = 6;**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="7e2f9-124">另一個應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="7e2f9-125">**const 不帶正負號短** **UserHidViaCharacterMenu = 7**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="7e2f9-126">使用者會在字元的快顯功能表中隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="7e2f9-127">**const 不帶正負號的短** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="7e2f9-128">使用者以字元的工作列圖示快顯功能表或使用語音輸入來隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="7e2f9-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7e2f9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e2f9-129">See Also</span></span>

[<span data-ttu-id="7e2f9-130">**IAgentNotifySink::VisibleState**</span><span class="sxs-lookup"><span data-stu-id="7e2f9-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 





