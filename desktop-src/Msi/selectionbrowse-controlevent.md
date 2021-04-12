---
description: SelectionTree 控制項會使用 SelectionBrowse 事件來產生流覽對話方塊，讓您可以修改反白專案的路徑。
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321067"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="2851d-103">SelectionBrowse ControlEvent</span><span class="sxs-lookup"><span data-stu-id="2851d-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="2851d-104">[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionBrowse 事件來產生 **流覽** 對話方塊，讓您可以修改反白專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2851d-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="2851d-105">這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。</span><span class="sxs-lookup"><span data-stu-id="2851d-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="2851d-106">此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。</span><span class="sxs-lookup"><span data-stu-id="2851d-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2851d-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="2851d-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2851d-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="2851d-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2851d-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="2851d-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="2851d-110">如果已選取已安裝、無法設定或未選取要進行本機安裝的功能，則任何發佈 SelectionBrowse 事件的控制項都會變成停用狀態。</span><span class="sxs-lookup"><span data-stu-id="2851d-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="2851d-111">若要設定，此功能必須在功能資料表的 [目錄] 欄位中輸入[公用屬性](public-properties.md) \_ 。 [](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="2851d-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="2851d-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="2851d-112">Published By</span></span>

[<span data-ttu-id="2851d-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="2851d-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="2851d-114">引數</span><span class="sxs-lookup"><span data-stu-id="2851d-114">Argument</span></span>

<span data-ttu-id="2851d-115">要產生之對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="2851d-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2851d-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="2851d-116">Action on Subscribers</span></span>

<span data-ttu-id="2851d-117">無。</span><span class="sxs-lookup"><span data-stu-id="2851d-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2851d-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="2851d-118">Typical Use</span></span>

<span data-ttu-id="2851d-119">與 SelectionTree 相同的強制回應對話方塊中的 [按鈕](pushbutton-control.md) 控制項，會使用此事件來觸發 [ **流覽** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2851d-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



