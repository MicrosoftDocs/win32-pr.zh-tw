---
description: '下表描述 InkCollector 物件事件可以引發的執行緒。筆墨線程上的 EventThreadsCursorButtonDownFires。筆墨線程上的 CursorButtonUpFires。筆墨線程上的 CursorDownFires。筆墨線程上的 CursorInRangeFires。筆墨線程上的 CursorOutOfRangeFires。DoubleClick 事件 (Automation 僅) 。在應用程式的使用者介面上引發 (UI) 執行緒。DoubleClick (Managed 程式庫只能在應用程式的 UI 執行緒上引發) 。筆墨線程上的 GestureFires。在應用程式的 UI 執行緒上 MouseDownFires。在應用程式的 UI 執行緒上 MouseMoveFires。在應用程式的 UI 執行緒上 MouseUpFires。在應用程式的 UI 執行緒上 MouseWheelFires。筆墨線程上的 NewInAirPacketsFires。筆墨線程上的 NewPacketsFires。StrokeFires 筆墨線程上的筆墨 thread.SystemGestureFires。筆墨線程上的 TabletAddedFires。筆墨線程上的 TabletRemovedFires。 '
ms.assetid: 39a1c868-eb7e-4139-806d-27d86175cbcf
title: InkCollector 物件事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b5d0031c6a471f3958efa5a8a1f95a5150e8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511293"
---
# <a name="inkcollector-object-events"></a><span data-ttu-id="51797-103">InkCollector 物件事件</span><span class="sxs-lookup"><span data-stu-id="51797-103">InkCollector Object Events</span></span>

<span data-ttu-id="51797-104">下表描述 [**InkCollector**](inkcollector-class.md) 物件事件可以引發的執行緒。</span><span class="sxs-lookup"><span data-stu-id="51797-104">The following table describes which threads the [**InkCollector**](inkcollector-class.md) object events can fire on.</span></span>



| <span data-ttu-id="51797-105">事件</span><span class="sxs-lookup"><span data-stu-id="51797-105">Event</span></span>                                                                              | <span data-ttu-id="51797-106">執行緒</span><span class="sxs-lookup"><span data-stu-id="51797-106">Threads</span></span>                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="51797-107">**CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="51797-107">**CursorButtonDown**</span></span>](inkcollector-cursorbuttondown.md)                          | <span data-ttu-id="51797-108">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-108">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-109">**CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="51797-109">**CursorButtonUp**</span></span>](inkcollector-cursorbuttonup.md)                              | <span data-ttu-id="51797-110">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-110">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-111">**CursorDown**</span><span class="sxs-lookup"><span data-stu-id="51797-111">**CursorDown**</span></span>](inkcollector-cursordown.md)                                      | <span data-ttu-id="51797-112">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-112">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-113">**CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="51797-113">**CursorInRange**</span></span>](inkcollector-cursorinrange.md)                                | <span data-ttu-id="51797-114">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-114">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-115">**CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="51797-115">**CursorOutOfRange**</span></span>](inkcollector-cursoroutofrange.md)                          | <span data-ttu-id="51797-116">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-116">Fires on the ink thread.</span></span><br/>                               |
| <span data-ttu-id="51797-117">[**DoubleClick 事件**](inkcollector-doubleclick.md) (Automation 僅) 。</span><span class="sxs-lookup"><span data-stu-id="51797-117">[**DoubleClick Event**](inkcollector-doubleclick.md) (Automation only).</span></span>           | <span data-ttu-id="51797-118">在應用程式的使用者介面上引發 (UI) 執行緒。</span><span class="sxs-lookup"><span data-stu-id="51797-118">Fires on the application's user interface (UI) thread.</span></span><br/> |
| <span data-ttu-id="51797-119">僅限 [**DoubleClick**](/previous-versions/ms567614(v=vs.100)) (Managed 程式庫) </span><span class="sxs-lookup"><span data-stu-id="51797-119">[**DoubleClick**](/previous-versions/ms567614(v=vs.100)) (Managed Library only)</span></span> | <span data-ttu-id="51797-120">在應用程式的 UI 執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-120">Fires on the application's UI thread.</span></span><br/>                  |
| [<span data-ttu-id="51797-121">**手勢**</span><span class="sxs-lookup"><span data-stu-id="51797-121">**Gesture**</span></span>](inkcollector-gesture.md)                                            | <span data-ttu-id="51797-122">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-122">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-123">**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="51797-123">**MouseDown**</span></span>](inkcollector-mousedown.md)                                        | <span data-ttu-id="51797-124">在應用程式的 UI 執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-124">Fires on the application's UI thread.</span></span><br/>                  |
| [<span data-ttu-id="51797-125">**MouseMove**</span><span class="sxs-lookup"><span data-stu-id="51797-125">**MouseMove**</span></span>](inkcollector-mousemove.md)                                        | <span data-ttu-id="51797-126">在應用程式的 UI 執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-126">Fires on the application's UI thread.</span></span><br/>                  |
| [<span data-ttu-id="51797-127">**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="51797-127">**MouseUp**</span></span>](inkcollector-mouseup.md)                                            | <span data-ttu-id="51797-128">在應用程式的 UI 執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-128">Fires on the application's UI thread.</span></span><br/>                  |
| [<span data-ttu-id="51797-129">**滑鼠滾輪**</span><span class="sxs-lookup"><span data-stu-id="51797-129">**MouseWheel**</span></span>](inkcollector-mousewheel.md)                                      | <span data-ttu-id="51797-130">在應用程式的 UI 執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-130">Fires on the application's UI thread.</span></span><br/>                  |
| [<span data-ttu-id="51797-131">**NewInAirPackets**</span><span class="sxs-lookup"><span data-stu-id="51797-131">**NewInAirPackets**</span></span>](inkcollector-newinairpackets.md)                            | <span data-ttu-id="51797-132">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-132">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-133">**NewPackets**</span><span class="sxs-lookup"><span data-stu-id="51797-133">**NewPackets**</span></span>](inkcollector-newpackets.md)                                      | <span data-ttu-id="51797-134">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-134">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-135">**中風**</span><span class="sxs-lookup"><span data-stu-id="51797-135">**Stroke**</span></span>](inkcollector-stroke.md)                                              | <span data-ttu-id="51797-136">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-136">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-137">**SystemGesture**</span><span class="sxs-lookup"><span data-stu-id="51797-137">**SystemGesture**</span></span>](inkcollector-systemgesture.md)                                | <span data-ttu-id="51797-138">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-138">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-139">**TabletAdded**</span><span class="sxs-lookup"><span data-stu-id="51797-139">**TabletAdded**</span></span>](inkcollector-tabletadded.md)                                    | <span data-ttu-id="51797-140">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-140">Fires on the ink thread.</span></span><br/>                               |
| [<span data-ttu-id="51797-141">**TabletRemoved**</span><span class="sxs-lookup"><span data-stu-id="51797-141">**TabletRemoved**</span></span>](inkcollector-tabletremoved.md)                                | <span data-ttu-id="51797-142">在筆跡執行緒上引發。</span><span class="sxs-lookup"><span data-stu-id="51797-142">Fires on the ink thread.</span></span><br/>                               |



 

 

