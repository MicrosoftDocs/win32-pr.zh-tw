---
description: 安裝程式會使用 SetProgress 事件來發佈有關安裝進度的資訊。
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944648"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="ddb64-103">SetProgress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="ddb64-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="ddb64-104">安裝程式會使用 SetProgress 事件來發佈有關安裝進度的資訊。</span><span class="sxs-lookup"><span data-stu-id="ddb64-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="ddb64-105">[ProgressBar 控制項](progressbar-control.md)或[佈告欄控制項](billboard-control.md)應藉由命名其進度指出的動作，來透過[EventMapping 資料表](eventmapping-table.md)訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="ddb64-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="ddb64-106">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="ddb64-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ddb64-107">此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="ddb64-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="ddb64-108">如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="ddb64-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ddb64-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="ddb64-109">Published By</span></span>

<span data-ttu-id="ddb64-110">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="ddb64-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="ddb64-111">引數</span><span class="sxs-lookup"><span data-stu-id="ddb64-111">Argument</span></span>

<span data-ttu-id="ddb64-112">無。</span><span class="sxs-lookup"><span data-stu-id="ddb64-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ddb64-113">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="ddb64-113">Action on Subscribers</span></span>

<span data-ttu-id="ddb64-114">無。</span><span class="sxs-lookup"><span data-stu-id="ddb64-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ddb64-115">一般用法</span><span class="sxs-lookup"><span data-stu-id="ddb64-115">Typical Use</span></span>

<span data-ttu-id="ddb64-116">非強制回應對話方塊上的 [ProgressBar](progressbar-control.md) 控制項會使用 [進度](progress-control-attribute.md) 屬性來接收進度資訊，以訂閱此事件。</span><span class="sxs-lookup"><span data-stu-id="ddb64-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



