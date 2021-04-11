---
description: 此事件會通知 DirectoryList 控制項，表示使用者想要選取目前目錄的父系。 如需相關資訊，請參閱流覽對話方塊。
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945501"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="6a0fa-104">DirectoryListUp ControlEvent</span><span class="sxs-lookup"><span data-stu-id="6a0fa-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="6a0fa-105">此事件會通知 [DirectoryList 控制項](directorylist-control.md) ，表示使用者想要選取目前目錄的父系。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="6a0fa-106">如需相關資訊，請參閱 [流覽對話方塊](browse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="6a0fa-107">這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="6a0fa-108">此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="6a0fa-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="6a0fa-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="6a0fa-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="6a0fa-112">如果目前的目錄是磁片磁碟機的根目錄，DirectoryListUp 事件會停用任何其他發行 DirectoryListUp 事件的控制項。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="6a0fa-113">發佈者</span><span class="sxs-lookup"><span data-stu-id="6a0fa-113">Published By</span></span>

[<span data-ttu-id="6a0fa-114">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="6a0fa-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="6a0fa-115">引數</span><span class="sxs-lookup"><span data-stu-id="6a0fa-115">Argument</span></span>

<span data-ttu-id="6a0fa-116">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="6a0fa-117">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="6a0fa-117">Action on Subscribers</span></span>

<span data-ttu-id="6a0fa-118">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6a0fa-119">一般用法</span><span class="sxs-lookup"><span data-stu-id="6a0fa-119">Typical Use</span></span>

<span data-ttu-id="6a0fa-120">在與 DirectoryList 相同的強制回應對話方塊上，使用 [ [按鈕](pushbutton-control.md) ] 控制項來觸發路徑中的逐步執行。</span><span class="sxs-lookup"><span data-stu-id="6a0fa-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



