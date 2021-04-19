---
description: CostInitialize 動作會起始安裝成本處理常式。
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: CostInitialize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971872"
---
# <a name="costinitialize-action"></a><span data-ttu-id="e97de-103">CostInitialize 動作</span><span class="sxs-lookup"><span data-stu-id="e97de-103">CostInitialize Action</span></span>

<span data-ttu-id="e97de-104">CostInitialize 動作會起始安裝 [*成本*](c-gly.md) 處理常式。</span><span class="sxs-lookup"><span data-stu-id="e97de-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e97de-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="e97de-105">Sequence Restrictions</span></span>

<span data-ttu-id="e97de-106">任何會影響成本的標準或 [自訂](custom-actions.md) 動作，都應該在 CostInitialize 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="e97de-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="e97de-107">在 CostInitialize 動作之後立即呼叫 [FileCost](filecost-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="e97de-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="e97de-108">然後，在 CostInitialize 動作動作之後呼叫 [CostFinalize](costfinalize-action.md) 動作，以透過 [元件](component-table.md) 資料表將所有最終成本計算提供給安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e97de-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e97de-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="e97de-109">ActionData Messages</span></span>

<span data-ttu-id="e97de-110">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="e97de-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e97de-111">備註</span><span class="sxs-lookup"><span data-stu-id="e97de-111">Remarks</span></span>

<span data-ttu-id="e97de-112">CostInitialize 動作會將元件資料表和 [功能](feature-table.md) 資料表載入記憶體中。</span><span class="sxs-lookup"><span data-stu-id="e97de-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="e97de-113">如需安裝程式中 [*成本*](c-gly.md) 處理常式的詳細資訊，請參閱檔案 [成本](file-costing.md)。</span><span class="sxs-lookup"><span data-stu-id="e97de-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e97de-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e97de-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97de-115">檔案成本</span><span class="sxs-lookup"><span data-stu-id="e97de-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



