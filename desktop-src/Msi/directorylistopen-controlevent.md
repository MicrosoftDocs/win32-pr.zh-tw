---
description: 此事件會選取並反白顯示 DirectoryList 控制項中使用者已選擇要開啟的目錄。 如需相關資訊，請參閱流覽對話方塊。
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195594"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="9eaa4-104">DirectoryListOpen ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9eaa4-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="9eaa4-105">此事件會選取並反白顯示 [DirectoryList 控制項](directorylist-control.md) 中使用者已選擇要開啟的目錄。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="9eaa4-106">如需相關資訊，請參閱 [流覽對話方塊](browse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="9eaa4-107">這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="9eaa4-108">此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="9eaa4-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="9eaa4-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="9eaa4-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="9eaa4-112">如果未在 [DirectoryList 控制項](directorylist-control.md)中選取任何目錄，DirectoryListOpen 事件就會停用任何其他發行 DirectoryListOpen 事件的控制項。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="9eaa4-113">發佈者</span><span class="sxs-lookup"><span data-stu-id="9eaa4-113">Published By</span></span>

[<span data-ttu-id="9eaa4-114">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="9eaa4-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="9eaa4-115">引數</span><span class="sxs-lookup"><span data-stu-id="9eaa4-115">Argument</span></span>

<span data-ttu-id="9eaa4-116">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9eaa4-117">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="9eaa4-117">Action on Subscribers</span></span>

<span data-ttu-id="9eaa4-118">此 ControlEvent 不會對訂閱者執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9eaa4-119">一般用法</span><span class="sxs-lookup"><span data-stu-id="9eaa4-119">Typical Use</span></span>

<span data-ttu-id="9eaa4-120">在相同的強制回應對話方塊上，使用 DirectoryList 的 [按鈕](pushbutton-control.md) 控制項，可用來觸發路徑中的逐步執行。</span><span class="sxs-lookup"><span data-stu-id="9eaa4-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



