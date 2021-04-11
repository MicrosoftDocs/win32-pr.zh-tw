---
description: 安裝程式會使用此事件來發佈目前動作的名稱。 訂閱此 ControlEvent 的文字控制項可以在對話方塊上顯示名稱。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944047"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="c339b-105">ActionText ControlEvent</span><span class="sxs-lookup"><span data-stu-id="c339b-105">ActionText ControlEvent</span></span>

<span data-ttu-id="c339b-106">安裝程式會使用此事件來發佈目前動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="c339b-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="c339b-107">訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊上顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c339b-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="c339b-108">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="c339b-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c339b-109">此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="c339b-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="c339b-110">如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="c339b-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c339b-111">發佈者</span><span class="sxs-lookup"><span data-stu-id="c339b-111">Published By</span></span>

<span data-ttu-id="c339b-112">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="c339b-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="c339b-113">引數</span><span class="sxs-lookup"><span data-stu-id="c339b-113">Argument</span></span>

<span data-ttu-id="c339b-114">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="c339b-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c339b-115">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="c339b-115">Action on Subscribers</span></span>

<span data-ttu-id="c339b-116">當新的進度資料從安裝程式抵達時，會顯示訂閱者。</span><span class="sxs-lookup"><span data-stu-id="c339b-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c339b-117">一般用法</span><span class="sxs-lookup"><span data-stu-id="c339b-117">Typical Use</span></span>

<span data-ttu-id="c339b-118">非強制回應對話方塊上的 [文字控制項](text-control.md) 會透過 [EventMapping 資料表](eventmapping-table.md)訂閱此事件。</span><span class="sxs-lookup"><span data-stu-id="c339b-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="c339b-119">[文字控制項屬性](text-control-attribute.md)應該列在此資料表的 [屬性] 欄位中，以接收目前動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="c339b-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



