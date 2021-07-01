---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120921"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="c45a9-103">IAgentNotifySink：:D blClick</span><span class="sxs-lookup"><span data-stu-id="c45a9-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="c45a9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c45a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="c45a9-105">當使用者按兩下字元時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="c45a9-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="c45a9-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="c45a9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="c45a9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="c45a9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="c45a9-108">按兩下字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c45a9-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="c45a9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="c45a9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="c45a9-110">指出滑鼠按鍵和輔助按鍵狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="c45a9-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="c45a9-111">參數可以傳回下列任何組合：</span><span class="sxs-lookup"><span data-stu-id="c45a9-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="c45a9-112">值</span><span class="sxs-lookup"><span data-stu-id="c45a9-112">Value</span></span>  | <span data-ttu-id="c45a9-113">描述</span><span class="sxs-lookup"><span data-stu-id="c45a9-113">Description</span></span>                               |
|--------|------------------------------------------------|
| <span data-ttu-id="c45a9-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="c45a9-114">0x0001</span></span> | <span data-ttu-id="c45a9-115">左方按鈕</span><span class="sxs-lookup"><span data-stu-id="c45a9-115">Left Button</span></span>                                    |
| <span data-ttu-id="c45a9-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="c45a9-116">0x0010</span></span> | <span data-ttu-id="c45a9-117">中間按鈕</span><span class="sxs-lookup"><span data-stu-id="c45a9-117">Middle Button</span></span>                                  |
| <span data-ttu-id="c45a9-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="c45a9-118">0x0002</span></span> | <span data-ttu-id="c45a9-119">右鍵按鈕</span><span class="sxs-lookup"><span data-stu-id="c45a9-119">Right Button</span></span>                                   |
| <span data-ttu-id="c45a9-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="c45a9-120">0x0004</span></span> | <span data-ttu-id="c45a9-121">向下 Shift 鍵</span><span class="sxs-lookup"><span data-stu-id="c45a9-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="c45a9-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="c45a9-122">0x0008</span></span> | <span data-ttu-id="c45a9-123">控制索引鍵關閉</span><span class="sxs-lookup"><span data-stu-id="c45a9-123">Control Key Down</span></span>                               |
| <span data-ttu-id="c45a9-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="c45a9-124">0x0020</span></span> | <span data-ttu-id="c45a9-125">ALT 鍵向下鍵</span><span class="sxs-lookup"><span data-stu-id="c45a9-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="c45a9-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="c45a9-126">0x1000</span></span> | <span data-ttu-id="c45a9-127">在字元的工作列圖示上發生事件</span><span class="sxs-lookup"><span data-stu-id="c45a9-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="c45a9-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="c45a9-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="c45a9-129">滑鼠指標的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="c45a9-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="c45a9-130"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="c45a9-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="c45a9-131">滑鼠指標的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="c45a9-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="c45a9-132">此事件會傳送到字元的輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="c45a9-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="c45a9-133">如果沒有任何字元的用戶端為輸入-主動，伺服器會通知該字元的作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="c45a9-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="c45a9-134">如果顯示此字元，伺服器也會讓該用戶端輸入為主動，並傳送 [**IAgentNotifySink：： ActivateInputState**](iagentnotifysink--activateinputstate.md)。</span><span class="sxs-lookup"><span data-stu-id="c45a9-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="c45a9-135">如果隱藏字元，則也會自動顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="c45a9-135">If the character is hidden, the character is also automatically shown.</span></span>

 

 




