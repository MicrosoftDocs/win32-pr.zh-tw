---
description: 當編譯安裝的執行腳本時，安裝程式會使用此事件來顯示資訊字串。
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986944"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="150a0-103">ScriptInProgress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="150a0-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="150a0-104">當編譯安裝的執行腳本時，安裝程式會使用此事件來顯示資訊字串。</span><span class="sxs-lookup"><span data-stu-id="150a0-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="150a0-105">訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊中顯示資訊字串。</span><span class="sxs-lookup"><span data-stu-id="150a0-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="150a0-106">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="150a0-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="150a0-107">此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="150a0-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="150a0-108">如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="150a0-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="150a0-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="150a0-109">Published By</span></span>

<span data-ttu-id="150a0-110">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="150a0-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="150a0-111">引數</span><span class="sxs-lookup"><span data-stu-id="150a0-111">Argument</span></span>

<span data-ttu-id="150a0-112">無。</span><span class="sxs-lookup"><span data-stu-id="150a0-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="150a0-113">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="150a0-113">Action on Subscribers</span></span>

<span data-ttu-id="150a0-114">訂閱 ScriptInProgress 的 [文字控制項](text-control.md) 將會顯示 [UIText 資料表](uitext-table.md)中指定的文字字串。</span><span class="sxs-lookup"><span data-stu-id="150a0-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="150a0-115">一般用法</span><span class="sxs-lookup"><span data-stu-id="150a0-115">Typical Use</span></span>

<span data-ttu-id="150a0-116">在編譯執行腳本時，安裝程式會顯示 ProgressBar，指出腳本執行開始之前的剩餘時間。</span><span class="sxs-lookup"><span data-stu-id="150a0-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="150a0-117">封裝作者在這段時間可以顯示初步訊息來說明 ProgressBar。</span><span class="sxs-lookup"><span data-stu-id="150a0-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="150a0-118">若要顯示初步訊息，請在與 ProgressBar 相同的非強制回應對話方塊中包含 [文字控制項](text-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="150a0-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="150a0-119">指定此文字控制項透過 [EventMapping 資料表](eventmapping-table.md)訂閱 ScriptInProgress ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="150a0-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="150a0-120">在 [UIText 資料表](uitext-table.md) 中包含索引鍵欄位中指定 ScriptInProgress 的專案。</span><span class="sxs-lookup"><span data-stu-id="150a0-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="150a0-121">在 UIText 資料表的文字欄位中，將初稿訊息指定為文字字串。</span><span class="sxs-lookup"><span data-stu-id="150a0-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="150a0-122">然後，在腳本編譯期間，安裝程式會在文字控制項中顯示此字串。</span><span class="sxs-lookup"><span data-stu-id="150a0-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="150a0-123">腳本編譯完成時，顯示的文字就會消失。</span><span class="sxs-lookup"><span data-stu-id="150a0-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="150a0-124">訂閱 ScriptInProgress ControlEvent 的相同文字控制項也可以訂閱 [TimeRemaining ControlEvent](timeremaining-controlevent.md)。</span><span class="sxs-lookup"><span data-stu-id="150a0-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="150a0-125">在此情況下，當初稿 ScriptInProgress 字串的文字消失時，就會以「剩餘時間： xx 分鐘」字串取代。</span><span class="sxs-lookup"><span data-stu-id="150a0-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



