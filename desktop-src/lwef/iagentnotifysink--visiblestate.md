---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968659"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="1cbb9-103">IAgentNotifySink::VisibleState</span><span class="sxs-lookup"><span data-stu-id="1cbb9-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="1cbb9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1cbb9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="1cbb9-105">當字元的可見度狀態變更時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="1cbb9-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="1cbb9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="1cbb9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="1cbb9-108">變更其可見度狀態之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb9-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="1cbb9-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="1cbb9-110">可見度旗標。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-110">Visibility flag.</span></span> <span data-ttu-id="1cbb9-111">當字元變成可見時，此布林值為 **True** ，當字元變成隱藏時為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb9-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="1cbb9-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="1cbb9-113">上次變更字元可見度狀態的原因。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="1cbb9-114">參數可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="1cbb9-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="1cbb9-115">值</span><span class="sxs-lookup"><span data-stu-id="1cbb9-115">Value</span></span>                                                                   | <span data-ttu-id="1cbb9-116">描述</span><span class="sxs-lookup"><span data-stu-id="1cbb9-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbb9-117">**const 不帶正負號短** **NeverShown = 0;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="1cbb9-118">未顯示字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="1cbb9-119">**const 不帶正負號短** **UserHid = 1;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="1cbb9-120">使用者以字元的工作列圖示快顯功能表或語音輸入來隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="1cbb9-121">**const 不帶正負號短** **UserShowed = 2;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="1cbb9-122">使用者顯示字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="1cbb9-123">**const 不帶正負號短** **ProgramHid = 3;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="1cbb9-124">您的應用程式會隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="1cbb9-125">**const 不帶正負號短** **ProgramShowed = 4;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="1cbb9-126">您的應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="1cbb9-127">**const 不帶正負號短** **OtherProgramHid = 5;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="1cbb9-128">另一個應用程式會將字元隱藏。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="1cbb9-129">**const 不帶正負號短** **OtherProgramShowed = 6;**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="1cbb9-130">另一個應用程式會顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="1cbb9-131">**const 不帶正負號短** **UserHidViaCharacterMenu = 7**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="1cbb9-132">使用者會在字元的快顯功能表中隱藏該字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="1cbb9-133">**const 不帶正負號的短** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="1cbb9-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="1cbb9-134">使用者以字元的工作列圖示快顯功能表或使用語音輸入來隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="1cbb9-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1cbb9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cbb9-135">See Also</span></span>

<span data-ttu-id="1cbb9-136">[**IAgentCharacter：： GetVisible**](iagentcharacter--getvisible.md)、 [ **IAgentCharacter：： GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb9-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 





