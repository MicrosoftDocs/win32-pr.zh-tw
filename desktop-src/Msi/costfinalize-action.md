---
description: CostFinalize 動作會結束由 CostInitialize 動作開始的內部安裝成本處理常式。
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: CostFinalize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975475"
---
# <a name="costfinalize-action"></a><span data-ttu-id="4b629-103">CostFinalize 動作</span><span class="sxs-lookup"><span data-stu-id="4b629-103">CostFinalize Action</span></span>

<span data-ttu-id="4b629-104">CostFinalize 動作會結束由 [CostInitialize](costinitialize-action.md)動作開始的內部安裝 [*成本*](c-gly.md)處理常式。</span><span class="sxs-lookup"><span data-stu-id="4b629-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4b629-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="4b629-105">Sequence Restrictions</span></span>

<span data-ttu-id="4b629-106">任何會影響成本的標準或 [自訂動作](custom-actions.md) ，都應該在 [CostInitialize](costinitialize-action.md) 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="4b629-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="4b629-107">在 CostInitialize 動作之後立即呼叫 [FileCost](filecost-action.md) 動作，然後呼叫 CostFinalize 動作，以透過 [元件](component-table.md) 資料表將所有最終成本計算提供給安裝程式。</span><span class="sxs-lookup"><span data-stu-id="4b629-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="4b629-108">CostFinalize 動作必須在啟動任何使用者介面順序之前執行，讓使用者能夠查看或修改 [功能](feature-table.md) 資料表選取專案或目錄。</span><span class="sxs-lookup"><span data-stu-id="4b629-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4b629-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="4b629-109">ActionData Messages</span></span>

<span data-ttu-id="4b629-110">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="4b629-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b629-111">備註</span><span class="sxs-lookup"><span data-stu-id="4b629-111">Remarks</span></span>

<span data-ttu-id="4b629-112">CostFinalize 動作會查詢 [條件](condition-table.md) 資料表，以判斷要安裝的功能。</span><span class="sxs-lookup"><span data-stu-id="4b629-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="4b629-113">[元件](component-table.md)資料表中的每個元件都會進行成本計算。</span><span class="sxs-lookup"><span data-stu-id="4b629-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="4b629-114">CostFinalize 動作也會先確認所有目標目錄都是可寫入的，然後才允許安裝繼續進行。</span><span class="sxs-lookup"><span data-stu-id="4b629-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="4b629-115">在 [系統管理安裝](administrative-installation.md)期間，CostFinalize 會設定所有安裝的功能，但功能 [資料表](feature-table.md)的 [層級] 資料行中有0個撰寫的功能除外。</span><span class="sxs-lookup"><span data-stu-id="4b629-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4b629-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b629-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b629-117">檔案成本</span><span class="sxs-lookup"><span data-stu-id="4b629-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



