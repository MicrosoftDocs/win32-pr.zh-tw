---
description: ValidateProductID 事件會將 ProductID 屬性設定為完整的產品識別碼。 如果驗證失敗，則此事件會針對產品識別碼的使用者專案顯示錯誤訊息和強制回應對話方塊。
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971038"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="6f25a-104">ValidateProductID ControlEvent</span><span class="sxs-lookup"><span data-stu-id="6f25a-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="6f25a-105">ValidateProductID 事件會將 [**ProductID**](productid.md) 屬性設定為完整的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f25a-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="6f25a-106">如果驗證失敗，則此事件會針對產品識別碼的使用者專案顯示錯誤訊息和強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6f25a-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="6f25a-107">這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。</span><span class="sxs-lookup"><span data-stu-id="6f25a-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="6f25a-108">此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。</span><span class="sxs-lookup"><span data-stu-id="6f25a-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="6f25a-109">此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。</span><span class="sxs-lookup"><span data-stu-id="6f25a-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="6f25a-110">此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6f25a-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="6f25a-111">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="6f25a-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="6f25a-112">發佈者</span><span class="sxs-lookup"><span data-stu-id="6f25a-112">Published By</span></span>

<span data-ttu-id="6f25a-113">此 ControlEvent 是由安裝程式所發佈。</span><span class="sxs-lookup"><span data-stu-id="6f25a-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="6f25a-114">引數</span><span class="sxs-lookup"><span data-stu-id="6f25a-114">Argument</span></span>

<span data-ttu-id="6f25a-115">無。</span><span class="sxs-lookup"><span data-stu-id="6f25a-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="6f25a-116">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="6f25a-116">Action on Subscribers</span></span>

<span data-ttu-id="6f25a-117">無。</span><span class="sxs-lookup"><span data-stu-id="6f25a-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6f25a-118">一般用法</span><span class="sxs-lookup"><span data-stu-id="6f25a-118">Typical Use</span></span>

<span data-ttu-id="6f25a-119">強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項系結至此事件，用來檢查使用者的產品識別碼專案。</span><span class="sxs-lookup"><span data-stu-id="6f25a-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="6f25a-120">如果使用者的輸入有效，則會開啟下一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6f25a-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



