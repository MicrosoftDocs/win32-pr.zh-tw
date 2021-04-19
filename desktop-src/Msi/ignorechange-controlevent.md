---
description: 當選取的資料夾從某個目錄變更為控制項中的另一個目錄時，DirectoryList 控制項就會發佈 IgnoreChange ControlEvent。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000273"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="b991b-104">IgnoreChange ControlEvent</span><span class="sxs-lookup"><span data-stu-id="b991b-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="b991b-105">當選取的資料夾從某個目錄變更為控制項中的另一個目錄時， [DirectoryList 控制項](directorylist-control.md) 就會發佈 IgnoreChange ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="b991b-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="b991b-106">此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="b991b-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b991b-107">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="b991b-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b991b-108">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b991b-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b991b-109">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="b991b-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="b991b-110">發佈者</span><span class="sxs-lookup"><span data-stu-id="b991b-110">Published By</span></span>

[<span data-ttu-id="b991b-111">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="b991b-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="b991b-112">引數</span><span class="sxs-lookup"><span data-stu-id="b991b-112">Argument</span></span>

<span data-ttu-id="b991b-113">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="b991b-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b991b-114">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="b991b-114">Action on Subscribers</span></span>

<span data-ttu-id="b991b-115">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="b991b-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b991b-116">一般用法</span><span class="sxs-lookup"><span data-stu-id="b991b-116">Typical Use</span></span>

<span data-ttu-id="b991b-117">[DirectoryCombo 控制項](directorycombo-control.md)通常會採用 IgnoreChange ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="b991b-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



