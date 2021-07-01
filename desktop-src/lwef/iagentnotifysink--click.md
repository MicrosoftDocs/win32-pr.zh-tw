---
title: IAgentNotifySink 按一下
description: IAgentNotifySink 按一下
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120901"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="a645e-103">IAgentNotifySink：： Click</span><span class="sxs-lookup"><span data-stu-id="a645e-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="a645e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a645e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="a645e-105">當使用者按一下字元或字元的工作列圖示時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="a645e-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="a645e-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a645e-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a645e-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="a645e-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a645e-108">已按下字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a645e-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="a645e-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="a645e-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a645e-110">指出滑鼠按鍵和輔助按鍵狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="a645e-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a645e-111">參數可以傳回下列任何組合：</span><span class="sxs-lookup"><span data-stu-id="a645e-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="a645e-112">值</span><span class="sxs-lookup"><span data-stu-id="a645e-112">Value</span></span>  | <span data-ttu-id="a645e-113">描述</span><span class="sxs-lookup"><span data-stu-id="a645e-113">Description</span></span>                                    |
|--------|------------------------------------------------|
| <span data-ttu-id="a645e-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="a645e-114">0x0001</span></span> | <span data-ttu-id="a645e-115">左方按鈕</span><span class="sxs-lookup"><span data-stu-id="a645e-115">Left Button</span></span>                                    |
| <span data-ttu-id="a645e-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="a645e-116">0x0010</span></span> | <span data-ttu-id="a645e-117">中間按鈕</span><span class="sxs-lookup"><span data-stu-id="a645e-117">Middle Button</span></span>                                  |
| <span data-ttu-id="a645e-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="a645e-118">0x0002</span></span> | <span data-ttu-id="a645e-119">右鍵按鈕</span><span class="sxs-lookup"><span data-stu-id="a645e-119">Right Button</span></span>                                   |
| <span data-ttu-id="a645e-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="a645e-120">0x0004</span></span> | <span data-ttu-id="a645e-121">向下 Shift 鍵</span><span class="sxs-lookup"><span data-stu-id="a645e-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="a645e-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="a645e-122">0x0008</span></span> | <span data-ttu-id="a645e-123">控制索引鍵關閉</span><span class="sxs-lookup"><span data-stu-id="a645e-123">Control Key Down</span></span>                               |
| <span data-ttu-id="a645e-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="a645e-124">0x0020</span></span> | <span data-ttu-id="a645e-125">ALT 鍵向下鍵</span><span class="sxs-lookup"><span data-stu-id="a645e-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="a645e-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="a645e-126">0x1000</span></span> | <span data-ttu-id="a645e-127">在字元的工作列圖示上發生事件</span><span class="sxs-lookup"><span data-stu-id="a645e-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="a645e-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="a645e-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a645e-129">滑鼠指標的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="a645e-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a645e-130"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="a645e-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a645e-131">滑鼠指標的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="a645e-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="a645e-132">此事件會傳送到字元的輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="a645e-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="a645e-133">如果沒有任何字元的用戶端為輸入-主動，伺服器會通知該字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="a645e-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="a645e-134">如果顯示此字元，伺服器也會讓該用戶端輸入為主動，並傳送 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md)。</span><span class="sxs-lookup"><span data-stu-id="a645e-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="a645e-135">如果隱藏字元，則也會自動顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="a645e-135">If the character hidden, the character is also automatically shown.</span></span>

 

 




