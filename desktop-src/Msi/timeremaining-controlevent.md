---
description: 安裝程式會使用 TimeRemaining 事件來發佈目前進度順序的大約剩餘時間（以秒為單位）。
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027400"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="9d684-103">TimeRemaining ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9d684-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="9d684-104">安裝程式會使用 TimeRemaining 事件來發佈目前進度順序的大約剩餘時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9d684-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="9d684-105">訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊上顯示剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="9d684-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="9d684-106">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="9d684-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="9d684-107">此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="9d684-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="9d684-108">如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="9d684-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="9d684-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="9d684-109">Published By</span></span>

<span data-ttu-id="9d684-110">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="9d684-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="9d684-111">引數</span><span class="sxs-lookup"><span data-stu-id="9d684-111">Argument</span></span>

<span data-ttu-id="9d684-112">無。</span><span class="sxs-lookup"><span data-stu-id="9d684-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9d684-113">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="9d684-113">Action on Subscribers</span></span>

<span data-ttu-id="9d684-114">無。</span><span class="sxs-lookup"><span data-stu-id="9d684-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9d684-115">一般用法</span><span class="sxs-lookup"><span data-stu-id="9d684-115">Typical Use</span></span>

<span data-ttu-id="9d684-116">非強制回應對話方塊上的 [文字控制項](text-control.md) 會透過 [EventMapping 資料表](eventmapping-table.md) 訂閱此事件，並使用 [TimeRemaining 屬性](timeremaining-control-attribute.md) 來顯示剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="9d684-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="9d684-117">訂閱 TimeRemaining ControlEvent 的相同文字控制項也可以訂閱 [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)。</span><span class="sxs-lookup"><span data-stu-id="9d684-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="9d684-118">在此情況下，會以初步的 ScriptInProgress 訊息字串取代，並以「剩餘時間： xx 分鐘」字串取代。</span><span class="sxs-lookup"><span data-stu-id="9d684-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



