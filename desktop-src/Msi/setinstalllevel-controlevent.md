---
description: SetInstallLevel 事件會將安裝層級變更為引數所指定的值。
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191603"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="65f15-103">SetInstallLevel ControlEvent</span><span class="sxs-lookup"><span data-stu-id="65f15-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="65f15-104">SetInstallLevel 事件會將安裝層級變更為引數所指定的值。</span><span class="sxs-lookup"><span data-stu-id="65f15-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="65f15-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="65f15-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="65f15-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="65f15-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="65f15-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="65f15-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="65f15-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="65f15-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="65f15-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="65f15-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="65f15-110">發佈者</span><span class="sxs-lookup"><span data-stu-id="65f15-110">Published By</span></span>

<span data-ttu-id="65f15-111">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="65f15-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="65f15-112">引數</span><span class="sxs-lookup"><span data-stu-id="65f15-112">Argument</span></span>

<span data-ttu-id="65f15-113">整數，這是安裝層級的新值。</span><span class="sxs-lookup"><span data-stu-id="65f15-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="65f15-114">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="65f15-114">Action on Subscribers</span></span>

<span data-ttu-id="65f15-115">無。</span><span class="sxs-lookup"><span data-stu-id="65f15-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="65f15-116">一般用法</span><span class="sxs-lookup"><span data-stu-id="65f15-116">Typical Use</span></span>

<span data-ttu-id="65f15-117">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以變更安裝層級。</span><span class="sxs-lookup"><span data-stu-id="65f15-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



