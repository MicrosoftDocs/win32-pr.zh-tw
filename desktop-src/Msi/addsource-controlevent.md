---
description: 此事件會通知安裝程式，同時讓目前的對話保持執行狀態，以從來源執行功能或所有功能。
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: AddSource ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998284"
---
# <a name="addsource-controlevent"></a><span data-ttu-id="ae71f-103">AddSource ControlEvent</span><span class="sxs-lookup"><span data-stu-id="ae71f-103">AddSource ControlEvent</span></span>

<span data-ttu-id="ae71f-104">此事件會通知安裝程式，同時讓目前的對話保持執行狀態，以從來源執行功能或所有功能。</span><span class="sxs-lookup"><span data-stu-id="ae71f-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run from source.</span></span> <span data-ttu-id="ae71f-105">這個事件可以透過 [按鈕控制項](pushbutton-control.md)、 [Checkbox 控制項](checkbox-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="ae71f-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="ae71f-106">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="ae71f-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="ae71f-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="ae71f-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ae71f-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="ae71f-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ae71f-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="ae71f-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ae71f-110">發佈者</span><span class="sxs-lookup"><span data-stu-id="ae71f-110">Published By</span></span>

<span data-ttu-id="ae71f-111">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="ae71f-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="ae71f-112">引數</span><span class="sxs-lookup"><span data-stu-id="ae71f-112">Argument</span></span>

<span data-ttu-id="ae71f-113">字串，也就是功能的名稱或 "ALL"。</span><span class="sxs-lookup"><span data-stu-id="ae71f-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ae71f-114">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="ae71f-114">Action on Subscribers</span></span>

<span data-ttu-id="ae71f-115">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="ae71f-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ae71f-116">一般用法</span><span class="sxs-lookup"><span data-stu-id="ae71f-116">Typical Use</span></span>

<span data-ttu-id="ae71f-117">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項系結至此事件，用來通知安裝程式，而不需停止對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ae71f-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



