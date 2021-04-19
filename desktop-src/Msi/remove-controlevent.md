---
description: 當選取要移除的功能或所有功能，同時讓目前的對話方塊執行時，安裝程式會收到此事件的通知。
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: 移除 ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977329"
---
# <a name="remove-controlevent"></a><span data-ttu-id="2c158-103">移除 ControlEvent</span><span class="sxs-lookup"><span data-stu-id="2c158-103">Remove ControlEvent</span></span>

<span data-ttu-id="2c158-104">當選取要移除的功能或所有功能，同時讓目前的對話方塊執行時，安裝程式會收到此事件的通知。</span><span class="sxs-lookup"><span data-stu-id="2c158-104">The installer is notified through this event when a feature or all features are selected for removal while keeping the present dialog box running.</span></span>

<span data-ttu-id="2c158-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="2c158-105">This event can be published by a [PushButton control](pushbutton-control.md), [CheckBox control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="2c158-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="2c158-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2c158-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="2c158-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2c158-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="2c158-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2c158-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="2c158-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="2c158-110">發佈者</span><span class="sxs-lookup"><span data-stu-id="2c158-110">Published By</span></span>

<span data-ttu-id="2c158-111">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="2c158-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="2c158-112">引數</span><span class="sxs-lookup"><span data-stu-id="2c158-112">Argument</span></span>

<span data-ttu-id="2c158-113">字串，該字串為功能的名稱或 "ALL"。</span><span class="sxs-lookup"><span data-stu-id="2c158-113">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2c158-114">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="2c158-114">Action on Subscribers</span></span>

<span data-ttu-id="2c158-115">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="2c158-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="action-by-publisher-when-subscriber-activated"></a><span data-ttu-id="2c158-116">訂閱者在訂閱者啟用時的動作</span><span class="sxs-lookup"><span data-stu-id="2c158-116">Action by Publisher When Subscriber Activated</span></span>

<span data-ttu-id="2c158-117">安裝程式會將目前的對話方塊保持在執行狀態，並通知安裝程式。</span><span class="sxs-lookup"><span data-stu-id="2c158-117">The installer keeps the present dialog box running and notifies the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2c158-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="2c158-118">Typical Use</span></span>

<span data-ttu-id="2c158-119">系結至這個事件的強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="2c158-119">A [PushButton](pushbutton-control.md) control on a modal dialog box tied to this event.</span></span>

 

 



