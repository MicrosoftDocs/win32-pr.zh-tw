---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120822"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="91ea9-103">IAgentNotifySink：:D ragStart</span><span class="sxs-lookup"><span data-stu-id="91ea9-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="91ea9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="91ea9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="91ea9-105">當使用者開始拖曳字元時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="91ea9-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="91ea9-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="91ea9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="91ea9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="91ea9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-108">拖曳字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91ea9-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="91ea9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="91ea9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-110">指出滑鼠按鍵和輔助按鍵狀態的參數。</span><span class="sxs-lookup"><span data-stu-id="91ea9-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="91ea9-111">參數可以傳回下列任何組合：</span><span class="sxs-lookup"><span data-stu-id="91ea9-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="91ea9-112">值</span><span class="sxs-lookup"><span data-stu-id="91ea9-112">Value</span></span>  | <span data-ttu-id="91ea9-113">描述</span><span class="sxs-lookup"><span data-stu-id="91ea9-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="91ea9-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="91ea9-114">0x0001</span></span> | <span data-ttu-id="91ea9-115">左方按鈕</span><span class="sxs-lookup"><span data-stu-id="91ea9-115">Left Button</span></span>      |
| <span data-ttu-id="91ea9-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="91ea9-116">0x0010</span></span> | <span data-ttu-id="91ea9-117">中間按鈕</span><span class="sxs-lookup"><span data-stu-id="91ea9-117">Middle Button</span></span>    |
| <span data-ttu-id="91ea9-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="91ea9-118">0x0002</span></span> | <span data-ttu-id="91ea9-119">右鍵按鈕</span><span class="sxs-lookup"><span data-stu-id="91ea9-119">Right Button</span></span>     |
| <span data-ttu-id="91ea9-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="91ea9-120">0x0004</span></span> | <span data-ttu-id="91ea9-121">向下 Shift 鍵</span><span class="sxs-lookup"><span data-stu-id="91ea9-121">Shift Key Down</span></span>   |
| <span data-ttu-id="91ea9-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="91ea9-122">0x0008</span></span> | <span data-ttu-id="91ea9-123">控制索引鍵關閉</span><span class="sxs-lookup"><span data-stu-id="91ea9-123">Control Key Down</span></span> |
| <span data-ttu-id="91ea9-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="91ea9-124">0x0020</span></span> | <span data-ttu-id="91ea9-125">ALT 鍵向下鍵</span><span class="sxs-lookup"><span data-stu-id="91ea9-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="91ea9-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="91ea9-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-127">滑鼠指標的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="91ea9-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="91ea9-128"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="91ea9-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-129">滑鼠指標的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="91ea9-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




