---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021966"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="a2b91-103">IAgentNotifySink：:D ragComplete</span><span class="sxs-lookup"><span data-stu-id="a2b91-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="a2b91-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a2b91-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="a2b91-105">當使用者停止拖曳字元時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="a2b91-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="a2b91-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a2b91-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a2b91-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="a2b91-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a2b91-108">拖曳字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2b91-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="a2b91-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="a2b91-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a2b91-110">指出滑鼠按鍵和輔助按鍵狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="a2b91-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a2b91-111">參數可以傳回下列任何組合：</span><span class="sxs-lookup"><span data-stu-id="a2b91-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="a2b91-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="a2b91-112">0x0001</span></span> | <span data-ttu-id="a2b91-113">左方按鈕</span><span class="sxs-lookup"><span data-stu-id="a2b91-113">Left Button</span></span>      |
| <span data-ttu-id="a2b91-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="a2b91-114">0x0010</span></span> | <span data-ttu-id="a2b91-115">中間按鈕</span><span class="sxs-lookup"><span data-stu-id="a2b91-115">Middle Button</span></span>    |
| <span data-ttu-id="a2b91-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="a2b91-116">0x0002</span></span> | <span data-ttu-id="a2b91-117">右鍵按鈕</span><span class="sxs-lookup"><span data-stu-id="a2b91-117">Right Button</span></span>     |
| <span data-ttu-id="a2b91-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="a2b91-118">0x0004</span></span> | <span data-ttu-id="a2b91-119">向下 Shift 鍵</span><span class="sxs-lookup"><span data-stu-id="a2b91-119">Shift Key Down</span></span>   |
| <span data-ttu-id="a2b91-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="a2b91-120">0x0008</span></span> | <span data-ttu-id="a2b91-121">控制索引鍵關閉</span><span class="sxs-lookup"><span data-stu-id="a2b91-121">Control Key Down</span></span> |
| <span data-ttu-id="a2b91-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="a2b91-122">0x0020</span></span> | <span data-ttu-id="a2b91-123">ALT 鍵向下鍵</span><span class="sxs-lookup"><span data-stu-id="a2b91-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a2b91-124"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="a2b91-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a2b91-125">滑鼠指標的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="a2b91-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a2b91-126"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="a2b91-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a2b91-127">滑鼠指標的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="a2b91-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




