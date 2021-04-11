---
description: '下表描述 InkEdit 控制項事件可以引發的執行緒。EventThreadsChangeFires 在應用程式的使用者)  (介面上，在應用程式 ui threadKeyDownFires 上的應用程式 ui threadGestureFires 上的應用程式 ui (上的應用程式 ui threadKeyPressFires 上的應用程式 ui threadKeyUpFires 上的應用程式 ui threadMouseDownFires 上的應用程式 ui threadMouseMoveFires 上的應用程式 ui threadMouseUpFires threadClickFires 應用程式 ui threadRecognition 上應用程式 ui 上應用程式 ui 上的應用程式 ui （僅) 限在應用程式 ui 執行緒上應用程式 ui threadSelChangeFires 的應用程式 ui threadRecognitionResultFires 上，于應用程式的 ui 執行緒上引發 '
ms.assetid: 8554a1ab-3288-4bdd-866b-dd2c25842b1f
title: InkEdit 控制項事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1547df05b438e6ade49663f5095dfd6674dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945000"
---
# <a name="inkedit-control-events"></a><span data-ttu-id="1a5ea-103">InkEdit 控制項事件</span><span class="sxs-lookup"><span data-stu-id="1a5ea-103">InkEdit Control Events</span></span>

<span data-ttu-id="1a5ea-104">下表描述 [InkEdit](inkedit-control-reference.md) 控制項事件可以引發的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1a5ea-104">The following table describes which threads the [InkEdit](inkedit-control-reference.md) control events can fire on.</span></span>



| <span data-ttu-id="1a5ea-105">事件</span><span class="sxs-lookup"><span data-stu-id="1a5ea-105">Event</span></span>                                                                          | <span data-ttu-id="1a5ea-106">執行緒</span><span class="sxs-lookup"><span data-stu-id="1a5ea-106">Threads</span></span>                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1a5ea-107">**變更**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-107">**Change**</span></span>](inkedit-change.md)                                               | <span data-ttu-id="1a5ea-108">在應用程式的使用者介面上引發 (UI) 執行緒</span><span class="sxs-lookup"><span data-stu-id="1a5ea-108">Fires on the application's user interface (UI) thread</span></span><br/> |
| [<span data-ttu-id="1a5ea-109">**按一下**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-109">**Click**</span></span>](inkedit-click.md)                                                 | <span data-ttu-id="1a5ea-110">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-110">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-111">**DblClick**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-111">**DblClick**</span></span>](inkedit-dblclick.md)                                           | <span data-ttu-id="1a5ea-112">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-112">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-113">**手勢**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-113">**Gesture**</span></span>](inkedit-gesture.md)                                             | <span data-ttu-id="1a5ea-114">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-114">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-115">**KeyDown**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-115">**KeyDown**</span></span>](inkedit-keydown.md)                                             | <span data-ttu-id="1a5ea-116">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-116">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-117">**KeyPress**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-117">**KeyPress**</span></span>](inkedit-keypress.md)                                           | <span data-ttu-id="1a5ea-118">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-118">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-119">**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-119">**KeyUp**</span></span>](inkedit-keyup.md)                                                 | <span data-ttu-id="1a5ea-120">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-120">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-121">**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-121">**MouseDown**</span></span>](inkedit-mousedown.md)                                         | <span data-ttu-id="1a5ea-122">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-122">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-123">**MouseMove**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-123">**MouseMove**</span></span>](inkedit-mousemove.md)                                         | <span data-ttu-id="1a5ea-124">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-124">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-125">**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-125">**MouseUp**</span></span>](inkedit-mouseup.md)                                             | <span data-ttu-id="1a5ea-126">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-126">Fires on the application's UI thread</span></span><br/>                  |
| <span data-ttu-id="1a5ea-127">僅 [**)  (受控**](/previous-versions/ms567627(v=vs.100))程式庫的辨識。</span><span class="sxs-lookup"><span data-stu-id="1a5ea-127">[**Recognition**](/previous-versions/ms567627(v=vs.100)) (Managed Library only).</span></span> | <span data-ttu-id="1a5ea-128">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-128">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-129">**RecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-129">**RecognitionResult**</span></span>](inkedit-recognitionresult.md)                         | <span data-ttu-id="1a5ea-130">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-130">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-131">**SelChange**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-131">**SelChange**</span></span>](inkedit-selchange.md)                                         | <span data-ttu-id="1a5ea-132">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-132">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="1a5ea-133">**中風**</span><span class="sxs-lookup"><span data-stu-id="1a5ea-133">**Stroke**</span></span>](inkedit-stroke.md)                                               | <span data-ttu-id="1a5ea-134">在應用程式的 UI 執行緒上引發</span><span class="sxs-lookup"><span data-stu-id="1a5ea-134">Fires on the application's UI thread</span></span><br/>                  |



 

 

