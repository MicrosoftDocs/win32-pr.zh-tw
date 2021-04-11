---
description: SetTargetPath 事件會通知安裝程式檢查並設定選取的路徑。 如果路徑無效而無法寫入，則安裝程式會封鎖與控制項相關聯的其他工作。
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193677"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="aa7d2-104">SetTargetPath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="aa7d2-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="aa7d2-105">SetTargetPath 事件會通知安裝程式檢查並設定選取的路徑。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="aa7d2-106">如果路徑無效而無法寫入，則安裝程式會封鎖與控制項相關聯的其他工作。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="aa7d2-107">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="aa7d2-108">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="aa7d2-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="aa7d2-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="aa7d2-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="aa7d2-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="aa7d2-112">Published By</span></span>

<span data-ttu-id="aa7d2-113">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="aa7d2-114">引數</span><span class="sxs-lookup"><span data-stu-id="aa7d2-114">Argument</span></span>

<span data-ttu-id="aa7d2-115">包含路徑之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-115">The name of the property containing the path.</span></span> <span data-ttu-id="aa7d2-116">如果屬性是 indirected，則屬性名稱會以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="aa7d2-117">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="aa7d2-117">Action on Subscribers</span></span>

<span data-ttu-id="aa7d2-118">無。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="aa7d2-119">一般用法</span><span class="sxs-lookup"><span data-stu-id="aa7d2-119">Typical Use</span></span>

<span data-ttu-id="aa7d2-120">流覽對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以檢查選取的路徑，然後再返回選取專案對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa7d2-121">備註</span><span class="sxs-lookup"><span data-stu-id="aa7d2-121">Remarks</span></span>

<span data-ttu-id="aa7d2-122">如果已為目前使用者或其他使用者安裝使用這些路徑的元件，請不要嘗試設定目標路徑。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="aa7d2-123">在發佈 SetTargetPath ControlEvent 之前，請先檢查 [**ProductState**](productstate.md) 屬性，以判斷是否已安裝包含該元件的產品。</span><span class="sxs-lookup"><span data-stu-id="aa7d2-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



