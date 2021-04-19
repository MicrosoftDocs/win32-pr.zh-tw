---
description: 藉由呼叫 MsiDoAction 函數或在順序資料表中包含動作，在 Windows Installer 中執行動作。
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: 使用標準動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975016"
---
# <a name="using-standard-actions"></a><span data-ttu-id="519dd-103">使用標準動作</span><span class="sxs-lookup"><span data-stu-id="519dd-103">Using Standard Actions</span></span>

<span data-ttu-id="519dd-104">藉由呼叫 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函數或在順序資料表中包含動作，在 Windows Installer 中執行動作。</span><span class="sxs-lookup"><span data-stu-id="519dd-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="519dd-105">因為大部分的動作都會封裝單一用途，所以使用動作最常見的方式就是將一連串的動作排序成一個序列，以完成較大的工作。</span><span class="sxs-lookup"><span data-stu-id="519dd-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="519dd-106">安裝程式有三個標準的最上層動作，這些動作會呼叫一組相關聯的順序資料表。</span><span class="sxs-lookup"><span data-stu-id="519dd-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="519dd-107">這些相關聯的順序資料表可能包含標準動作、自訂動作和使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="519dd-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="519dd-108">順序資料表中的每個動作都有相關聯的序號，而且也可以有相關聯的條件運算式。</span><span class="sxs-lookup"><span data-stu-id="519dd-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="519dd-109">順序資料表中的所有動作都會依序流覽，而且只有在條件運算式評估為 True 時才會執行。</span><span class="sxs-lookup"><span data-stu-id="519dd-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="519dd-110">雖然標準動作可以有與其相關聯的任何序號，但是有許多順序限制必須遵循，才能讓動作正常運作。</span><span class="sxs-lookup"><span data-stu-id="519dd-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="519dd-111">例如，您必須在[CostInitialize 動作](costinitialize-action.md)之後呼叫[FileCost 動作](filecost-action.md)。</span><span class="sxs-lookup"><span data-stu-id="519dd-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="519dd-112">如需標準動作順序限制的詳細資訊，請參閱 [具有排序限制的動作](actions-with-sequencing-restrictions.md)、 [沒有排序限制的動作](actions-without-sequencing-restrictions.md)，或 [標準動作參考](standard-actions-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="519dd-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="519dd-113">下列主題提供有關使用標準動作的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="519dd-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="519dd-114">發佈產品、功能和元件</span><span class="sxs-lookup"><span data-stu-id="519dd-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="519dd-115">檔案搜尋</span><span class="sxs-lookup"><span data-stu-id="519dd-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="519dd-116">檔案成本</span><span class="sxs-lookup"><span data-stu-id="519dd-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="519dd-117">檔案安裝</span><span class="sxs-lookup"><span data-stu-id="519dd-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="519dd-118">修改登錄</span><span class="sxs-lookup"><span data-stu-id="519dd-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="519dd-119">執行動作</span><span class="sxs-lookup"><span data-stu-id="519dd-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="519dd-120">另請參閱 [標準動作](about-standard-actions.md) 或 [標準動作參考](standard-actions-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="519dd-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



