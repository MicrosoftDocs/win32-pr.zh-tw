---
description: 這個 ControlEvent 可以用來開啟或關閉安裝程式的復原功能。
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978861"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="16681-103">EnableRollback ControlEvent</span><span class="sxs-lookup"><span data-stu-id="16681-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="16681-104">這個 ControlEvent 可以用來開啟或關閉安裝程式的復原功能。</span><span class="sxs-lookup"><span data-stu-id="16681-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="16681-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="16681-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="16681-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="16681-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="16681-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="16681-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="16681-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="16681-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="16681-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="16681-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="16681-110">發佈者</span><span class="sxs-lookup"><span data-stu-id="16681-110">Published By</span></span>

<span data-ttu-id="16681-111">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="16681-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="16681-112">引數</span><span class="sxs-lookup"><span data-stu-id="16681-112">Argument</span></span>

<span data-ttu-id="16681-113">False 關閉安裝程式的復原功能。</span><span class="sxs-lookup"><span data-stu-id="16681-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="16681-114">True 會開啟安裝程式的復原功能。</span><span class="sxs-lookup"><span data-stu-id="16681-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="16681-115">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="16681-115">Action on Subscribers</span></span>

<span data-ttu-id="16681-116">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="16681-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="16681-117">一般用法</span><span class="sxs-lookup"><span data-stu-id="16681-117">Typical Use</span></span>

<span data-ttu-id="16681-118">如果安裝程式偵測到沒有足夠的可用磁碟空間來完成安裝，可以使用來關閉復原功能。</span><span class="sxs-lookup"><span data-stu-id="16681-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="16681-119">在此情況下，ControlEvent 應該與 [**OutOfDiskSpace**](outofdiskspace.md)、 [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)和 [**PROMPTROLLBACKCOST**](promptrollbackcost.md) 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="16681-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



