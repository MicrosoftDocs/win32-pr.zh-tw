---
description: 此事件會通知 DirectoryList 控制項必須建立新資料夾;它會建立新的資料夾，並選取資料夾的 [名稱] 欄位以進行編輯。
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980101"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="59d9b-103">DirectoryListNew ControlEvent</span><span class="sxs-lookup"><span data-stu-id="59d9b-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="59d9b-104">此事件會通知 [DirectoryList 控制項](directorylist-control.md) 必須建立新資料夾;它會建立新的資料夾，並選取資料夾的 [名稱] 欄位以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="59d9b-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="59d9b-105">新資料夾的預設名稱可能會在 [UIText 資料表](uitext-table.md)中撰寫。</span><span class="sxs-lookup"><span data-stu-id="59d9b-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="59d9b-106">在索引鍵資料行中輸入 "NewFolder"。</span><span class="sxs-lookup"><span data-stu-id="59d9b-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="59d9b-107">在 [文字] 資料行中，輸入新資料夾的預設名稱值。</span><span class="sxs-lookup"><span data-stu-id="59d9b-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="59d9b-108">這個值必須是 [Filename](filename.md) 資料行資料類型的格式，並使用 SFN \| LFN 語法。</span><span class="sxs-lookup"><span data-stu-id="59d9b-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="59d9b-109">如果此值不存在於 UIText 資料表中或為無效值，則安裝程式會使用預設值 "Fldr \| New Folder"。</span><span class="sxs-lookup"><span data-stu-id="59d9b-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="59d9b-110">如需相關資訊，請參閱 [流覽對話方塊](browse-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="59d9b-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="59d9b-111">這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。</span><span class="sxs-lookup"><span data-stu-id="59d9b-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="59d9b-112">此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。</span><span class="sxs-lookup"><span data-stu-id="59d9b-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="59d9b-113">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="59d9b-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="59d9b-114">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="59d9b-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="59d9b-115">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="59d9b-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="59d9b-116">請注意，如果在新資料夾已存在時再次呼叫這個 ControlEvent，則不會建立第二個新的資料夾。</span><span class="sxs-lookup"><span data-stu-id="59d9b-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="59d9b-117">在此情況下，呼叫 DirectoryListNew 會選取現有的新資料夾名稱進行編輯。</span><span class="sxs-lookup"><span data-stu-id="59d9b-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="59d9b-118">發佈者</span><span class="sxs-lookup"><span data-stu-id="59d9b-118">Published By</span></span>

[<span data-ttu-id="59d9b-119">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="59d9b-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="59d9b-120">引數</span><span class="sxs-lookup"><span data-stu-id="59d9b-120">Argument</span></span>

<span data-ttu-id="59d9b-121">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="59d9b-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="59d9b-122">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="59d9b-122">Action on Subscribers</span></span>

<span data-ttu-id="59d9b-123">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="59d9b-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="59d9b-124">一般用法</span><span class="sxs-lookup"><span data-stu-id="59d9b-124">Typical Use</span></span>

<span data-ttu-id="59d9b-125">與 DirectoryList 相同的強制回應對話方塊中的 [按鈕](pushbutton-control.md) 控制項，可用來觸發新資料夾的建立。</span><span class="sxs-lookup"><span data-stu-id="59d9b-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



