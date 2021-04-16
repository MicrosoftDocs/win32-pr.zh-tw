---
description: 有兩種方式可以撰寫 Windows Installer 安裝資料庫，因此只有在卸載套件時才會呼叫動作。
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: 要在移除期間執行的調節動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e84f21b42f569744af9b8a7a46bb1e3df7a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513092"
---
# <a name="conditioning-actions-to-run-during-removal"></a><span data-ttu-id="4baf6-103">要在移除期間執行的調節動作</span><span class="sxs-lookup"><span data-stu-id="4baf6-103">Conditioning Actions to Run During Removal</span></span>

<span data-ttu-id="4baf6-104">有兩種方式可以撰寫安裝資料庫，因此只會在卸載套件時呼叫動作：</span><span class="sxs-lookup"><span data-stu-id="4baf6-104">There are two ways to author the installation database such that an action is only called when the package is uninstalled:</span></span>

-   <span data-ttu-id="4baf6-105">如果動作是在[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的[InstallValidate 動作](installvalidate-action.md)之後排序，封裝作者可以針對 [條件] 資料行中的動作指定 [移除] = [全部] 條件。</span><span class="sxs-lookup"><span data-stu-id="4baf6-105">If the action is sequenced after the [InstallValidate action](installvalidate-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md), the package author may specify a condition of REMOVE="ALL" for the action in the Condition column.</span></span> <span data-ttu-id="4baf6-106">請注意，在安裝程式執行 InstallValidate 動作之前，不保證會在卸載期間將 [ [**移除**](remove.md) ] 屬性設定為 [全部]。</span><span class="sxs-lookup"><span data-stu-id="4baf6-106">Note that the [**REMOVE**](remove.md) property is not guaranteed to be set to ALL during an uninstall before the installer executes the InstallValidate action.</span></span> <span data-ttu-id="4baf6-107">請注意，在此情況下，引號括住值全部都是必要的。</span><span class="sxs-lookup"><span data-stu-id="4baf6-107">Note that the quote marks around the value ALL are required in this case.</span></span>
-   <span data-ttu-id="4baf6-108">如果動作是在 [CostFinalize 動作](costfinalize-action.md) 之後排序的，以及任何可能變更功能狀態的動作（例如 [MigrateFeatureStates 動作](migratefeaturestates-action.md)），動作就可以是特定功能或元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="4baf6-108">If the action is sequenced after the [CostFinalize action](costfinalize-action.md) and any actions that could change the feature state, such as [MigrateFeatureStates action](migratefeaturestates-action.md), the action can be conditioned on the state of a particular feature or component.</span></span> <span data-ttu-id="4baf6-109">請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="4baf6-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span> <span data-ttu-id="4baf6-110">使用這個選項可在移除特定功能或元件期間呼叫動作，這可能會在應用程式完全移除之外發生。</span><span class="sxs-lookup"><span data-stu-id="4baf6-110">Use this option to call an action during the removal of a particular feature or component, which may occur outside of the complete removal of the application.</span></span>

<span data-ttu-id="4baf6-111">請注意，[ [**已安裝**](installed.md) ] 屬性可用於條件運算式中，以判斷是否已針對每部電腦或目前使用者安裝產品。</span><span class="sxs-lookup"><span data-stu-id="4baf6-111">Note that the [**Installed**](installed.md) property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="4baf6-112">若要判斷是否已針對不同的使用者安裝產品，請檢查 [**ProductState**](productstate.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4baf6-112">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="4baf6-113">請注意， [RemoveExistingProducts 動作](removeexistingproducts-action.md)在升級期間可能會移除較舊版本的產品。</span><span class="sxs-lookup"><span data-stu-id="4baf6-113">Note that older versions of a product may be removed during an upgrade by the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="4baf6-114">在此情況下， [升級資料表](upgrade-table.md) 也可以將 [ [**移除**](remove.md) ] 屬性設定為 [全部]。</span><span class="sxs-lookup"><span data-stu-id="4baf6-114">The [Upgrade table](upgrade-table.md) may also set the [**REMOVE**](remove.md) property to ALL in this case.</span></span> <span data-ttu-id="4baf6-115">若要判斷升級是否正在移除產品，請檢查 [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4baf6-115">To determine whether a product is being removed by an upgrade, check the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) property.</span></span> <span data-ttu-id="4baf6-116">當 RemoveExistingProducts 移除產品時，安裝程式只會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="4baf6-116">The installer only sets this property when RemoveExistingProducts removes the product.</span></span> <span data-ttu-id="4baf6-117">安裝程式不會在一般卸載期間設定屬性，例如，使用 [新增/移除程式] 移除。</span><span class="sxs-lookup"><span data-stu-id="4baf6-117">The installer does not set the property during a normal uninstall, such as removal with Add/Remove programs.</span></span>

 

 



