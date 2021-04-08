---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023398"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="af842-103">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="af842-103">IAgentNotifySink</span></span>

<span data-ttu-id="af842-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="af842-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="af842-105">IAgentNotifySink 會在發生特定狀態變更時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="af842-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="af842-106">這些函數也可從 [IAgentNotifySinkEx](iagentnotifysinkex.md)取得。</span><span class="sxs-lookup"><span data-stu-id="af842-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="af842-107">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="af842-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="af842-108">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="af842-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="af842-109">Description</span><span class="sxs-lookup"><span data-stu-id="af842-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af842-110">**命令**</span><span class="sxs-lookup"><span data-stu-id="af842-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="af842-111">當伺服器處理用戶端定義的命令時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="af842-112">**ActivateInputState**</span><span class="sxs-lookup"><span data-stu-id="af842-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="af842-113">當字元變成或停止輸入-主動時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="af842-114">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="af842-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="af842-115">當字元的 **可見** 狀態變更時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="af842-116">**點選事件**</span><span class="sxs-lookup"><span data-stu-id="af842-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="af842-117">發生于按一下字元時。</span><span class="sxs-lookup"><span data-stu-id="af842-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="af842-118">**DblClick 事件**</span><span class="sxs-lookup"><span data-stu-id="af842-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="af842-119">發生于按兩下字元時。</span><span class="sxs-lookup"><span data-stu-id="af842-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="af842-120">**DragStart**</span><span class="sxs-lookup"><span data-stu-id="af842-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="af842-121">發生于使用者開始拖曳字元時。</span><span class="sxs-lookup"><span data-stu-id="af842-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="af842-122">**DragComplete**</span><span class="sxs-lookup"><span data-stu-id="af842-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="af842-123">發生于使用者停止拖曳字元時。</span><span class="sxs-lookup"><span data-stu-id="af842-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="af842-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="af842-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="af842-125">當伺服器開始處理 [**要求**](/windows/desktop/lwef/the-request-object) 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="af842-126">**RequestComplete**</span><span class="sxs-lookup"><span data-stu-id="af842-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="af842-127">當伺服器完成處理 [**要求**](/windows/desktop/lwef/the-request-object) 物件時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="af842-128">**書籤**</span><span class="sxs-lookup"><span data-stu-id="af842-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="af842-129">當伺服器處理書簽時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="af842-130">**閒置**</span><span class="sxs-lookup"><span data-stu-id="af842-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="af842-131">當伺服器啟動或結束閒置處理時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="af842-132">**移動**</span><span class="sxs-lookup"><span data-stu-id="af842-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="af842-133">發生于移動字元時。</span><span class="sxs-lookup"><span data-stu-id="af842-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="af842-134">**大小**</span><span class="sxs-lookup"><span data-stu-id="af842-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="af842-135">當字元已調整大小時發生。</span><span class="sxs-lookup"><span data-stu-id="af842-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="af842-136">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="af842-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="af842-137">發生于字元字組氣球的可見度狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="af842-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="af842-138">舊版 Microsoft Agent 支援的 IAgentNotifySink：： Restart 和 IAgentNotifySink：： Shutdown 事件現在已過時。</span><span class="sxs-lookup"><span data-stu-id="af842-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="af842-139">雖然支援回溯相容性，但伺服器不會再傳送這些事件。</span><span class="sxs-lookup"><span data-stu-id="af842-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 