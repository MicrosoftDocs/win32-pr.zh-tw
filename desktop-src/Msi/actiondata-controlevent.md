---
description: 安裝程式會使用此事件來發佈最新動作的資料。 訂閱此 ControlEvent 的文字控制項可以在對話方塊上顯示資料。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999883"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="d18d3-105">ActionData ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d18d3-105">ActionData ControlEvent</span></span>

<span data-ttu-id="d18d3-106">安裝程式會使用此事件來發佈最新動作的資料。</span><span class="sxs-lookup"><span data-stu-id="d18d3-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="d18d3-107">訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊上顯示資料。</span><span class="sxs-lookup"><span data-stu-id="d18d3-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="d18d3-108">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="d18d3-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="d18d3-109">此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="d18d3-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="d18d3-110">如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="d18d3-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d18d3-111">發佈者</span><span class="sxs-lookup"><span data-stu-id="d18d3-111">Published By</span></span>

<span data-ttu-id="d18d3-112">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="d18d3-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d18d3-113">引數</span><span class="sxs-lookup"><span data-stu-id="d18d3-113">Argument</span></span>

<span data-ttu-id="d18d3-114">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="d18d3-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d18d3-115">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="d18d3-115">Action on Subscribers</span></span>

<span data-ttu-id="d18d3-116">當新動作開始時，系統會隱藏訂閱者，並在新的動作資料從安裝程式抵達時顯示。</span><span class="sxs-lookup"><span data-stu-id="d18d3-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d18d3-117">一般用法</span><span class="sxs-lookup"><span data-stu-id="d18d3-117">Typical Use</span></span>

<span data-ttu-id="d18d3-118">非強制回應對話方塊上的 [文字控制項](text-control.md) 會透過 [EventMapping 資料表](eventmapping-table.md)訂閱此事件。</span><span class="sxs-lookup"><span data-stu-id="d18d3-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="d18d3-119">此 [文字控制項屬性](text-control-attribute.md) 會列在此資料表的 [屬性] 欄位中，以接收目前的動作資料。</span><span class="sxs-lookup"><span data-stu-id="d18d3-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="d18d3-120">通常用來顯示檔案複製期間複製的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d18d3-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



