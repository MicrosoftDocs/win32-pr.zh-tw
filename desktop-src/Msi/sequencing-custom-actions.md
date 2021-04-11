---
description: 自訂動作會以與標準動作相同的方式，在順序資料表中排程。
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: 排序自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7c24fb91247a36880cb808c9b8e10437312cf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195261"
---
# <a name="sequencing-custom-actions"></a><span data-ttu-id="01c3e-103">排序自訂動作</span><span class="sxs-lookup"><span data-stu-id="01c3e-103">Sequencing Custom Actions</span></span>

<span data-ttu-id="01c3e-104">自訂動作會以與標準動作相同的方式，在順序資料表中排程。</span><span class="sxs-lookup"><span data-stu-id="01c3e-104">Custom actions are scheduled in sequence tables in the same way as standard actions.</span></span>

<span data-ttu-id="01c3e-105">**若要排程順序資料表中的自訂動作**</span><span class="sxs-lookup"><span data-stu-id="01c3e-105">**To schedule a custom action in a sequence table**</span></span>

1.  <span data-ttu-id="01c3e-106">在 [[順序](sequence-table-detailed-example.md)] 資料表的 [動作] 資料行中，輸入自訂動作名稱 (，這是[CustomAction](customaction-table.md)) 資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="01c3e-106">Enter the custom action name (which is the primary key of the [CustomAction](customaction-table.md)) table into the Action column of the [Sequence](sequence-table-detailed-example.md) table.</span></span>
2.  <span data-ttu-id="01c3e-107">將自訂動作的順序，輸入至 [ [順序](sequence-table-detailed-example.md) ] 資料表的 [順序] 資料行中，相對於資料表中的其他動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-107">Enter the custom action's sequence relative to the other actions in the table into the Sequence column of the [Sequence](sequence-table-detailed-example.md) table.</span></span> <span data-ttu-id="01c3e-108">如需順序資料表的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="01c3e-108">For more information about sequence tables, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>
3.  <span data-ttu-id="01c3e-109">若要有條件地略過該動作，請在 [ [順序](sequence-table-detailed-example.md) ] 資料表的 [條件] 資料行中輸入條件運算式。</span><span class="sxs-lookup"><span data-stu-id="01c3e-109">To conditionally skip the action, enter a conditional expression into the Condition column of the [Sequence](sequence-table-detailed-example.md) table.</span></span> <span data-ttu-id="01c3e-110">如果運算式評估為 FALSE，則安裝程式會略過這個動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-110">The installer skips this action if the expression evaluates to FALSE.</span></span>

<span data-ttu-id="01c3e-111">就像標準動作一樣，只有在內部使用者介面設定為完整層級時，才會執行 [InstallUISequence](installuisequence-table.md) 或 [AdminUISequence](adminuisequence-table.md) 中排程的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-111">As in the case of standard actions, custom actions that are scheduled in the [InstallUISequence](installuisequence-table.md) or [AdminUISequence](adminuisequence-table.md) run only if the internal user interface is set to the full level.</span></span> <span data-ttu-id="01c3e-112">UI 層級是使用 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 函數來設定。</span><span class="sxs-lookup"><span data-stu-id="01c3e-112">The UI level is set by using the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

<span data-ttu-id="01c3e-113">排程在 [InstallExecuteSequence](installexecutesequence-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)或 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表中的標準和自訂動作不會進行系統變更。</span><span class="sxs-lookup"><span data-stu-id="01c3e-113">Standard and custom actions scheduled in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables do not make system changes.</span></span> <span data-ttu-id="01c3e-114">相反地，安裝程式會將腳本中的執行記錄排入佇列中，以便在安裝服務期間進行後續的執行。</span><span class="sxs-lookup"><span data-stu-id="01c3e-114">Instead the installer queues up execution records in a script for subsequent execution during the install service.</span></span> <span data-ttu-id="01c3e-115">如果沒有安裝服務，則在這些資料表中排程的動作會在與 UI 順序相同的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="01c3e-115">If there is no install service, then the actions scheduled in these tables are run in the same context as the UI sequence.</span></span>

<span data-ttu-id="01c3e-116">如果安裝程式伺服器未註冊，則會在用戶端上執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-116">If the installer server is not registered, the custom actions are executed on the client side.</span></span> <span data-ttu-id="01c3e-117">如果伺服器已註冊且使用完整的 UI 模式，則會在伺服器端執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-117">If the server is registered and using the full UI mode, then the custom actions are run on the server side.</span></span>

<span data-ttu-id="01c3e-118">如果使用完整的 UI 與伺服器，則在 [InstallValidate](installvalidate-action.md) 動作之前的初始動作會在用戶端上執行，以允許完全互動。</span><span class="sxs-lookup"><span data-stu-id="01c3e-118">If using full UI with the server, the initial actions prior to the [InstallValidate](installvalidate-action.md) action are run on the client to allow full interaction.</span></span> <span data-ttu-id="01c3e-119">然後執行會切換至伺服器，以重複這些動作並執行腳本執行動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-119">Execution is then switched to the server which repeats those actions and runs the script execution actions.</span></span> <span data-ttu-id="01c3e-120">之後會傳回用戶端的最後一個動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-120">This is followed by a return to the client for the final actions.</span></span>

<span data-ttu-id="01c3e-121">請注意，如果產品是藉由將其最上層功能設定為 [不存在] 來移除，則 [ [**移除**](remove.md) ] 屬性在 [InstallValidate](installvalidate-action.md) 動作之後可能不會完全相同。</span><span class="sxs-lookup"><span data-stu-id="01c3e-121">Note that if a product is removed by setting its top feature to absent, the [**REMOVE**](remove.md) property may not equal ALL until after the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="01c3e-122">這表示任何相依于 REMOVE = ALL 的自訂動作都必須在 InstallValidate 動作之後排序。</span><span class="sxs-lookup"><span data-stu-id="01c3e-122">This means that any custom action that depends on REMOVE=ALL must be sequenced after the InstallValidate action.</span></span> <span data-ttu-id="01c3e-123">自訂動作可能會勾選 [移除]，以判斷產品是否已設定為完全卸載。</span><span class="sxs-lookup"><span data-stu-id="01c3e-123">A custom action may check REMOVE to determine whether a product has been set to be completely uninstalled.</span></span>

<span data-ttu-id="01c3e-124">參考已安裝檔案作為其來源的自訂動作，例如自訂動作類型 17 (DLL) 、自訂動作類型 18 (EXE) 、自訂動作類型 21 (JScript) 和自訂動作類型 22 (VBScript) ，必須遵守下列排序限制。</span><span class="sxs-lookup"><span data-stu-id="01c3e-124">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), Custom Action Type 18 (EXE), Custom Action Type 21 (JScript), and Custom Action Type 22 (VBScript), must adhere to the following sequencing restrictions.</span></span>

-   <span data-ttu-id="01c3e-125">自訂動作必須在 [CostFinalize](costfinalize-action.md) 動作之後排序，才能解析參考檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="01c3e-125">The custom action must be sequenced after the [CostFinalize](costfinalize-action.md) action so that the path to the referenced file can be resolved.</span></span>
-   <span data-ttu-id="01c3e-126">如果來源檔案尚未安裝在電腦上，延遲的 (腳本內) 自訂動作必須在 [InstallFiles](installfiles-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="01c3e-126">If the source file is not already installed on the computer, deferred (in-script) custom actions must be sequenced after the [InstallFiles](installfiles-action.md).</span></span>
-   <span data-ttu-id="01c3e-127">如果來源檔案尚未安裝在電腦上，則必須在 [InstallInitialize](installinitialize-action.md) 動作之後排序 nondeferred 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-127">If the source file is not already installed on the computer, nondeferred custom actions must be sequenced after the [InstallInitialize](installinitialize-action.md) action.</span></span>

<span data-ttu-id="01c3e-128">下列排序限制適用于變更或更新 Windows Installer 封裝的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-128">The following sequencing restrictions apply to custom actions that change or update a Windows Installer package.</span></span>

-   <span data-ttu-id="01c3e-129">如果自訂動作變更了封裝（例如將資料列加入資料表中），則必須在 [InstallInitialize](installinitialize-action.md) 動作之前排序動作。</span><span class="sxs-lookup"><span data-stu-id="01c3e-129">If the custom action changes the package, such as by adding rows to a table, the action must be sequenced before the [InstallInitialize](installinitialize-action.md) action.</span></span>
-   <span data-ttu-id="01c3e-130">如果自訂動作會產生會影響成本的變更，則應該在 [CostInitialize](costfinalize-action.md) 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="01c3e-130">If the custom action makes changes that would affect costing, then it should be sequenced before the [CostInitialize](costfinalize-action.md) action.</span></span>
-   <span data-ttu-id="01c3e-131">如果自訂動作變更了功能或元件的安裝狀態，則必須在 [InstallValidate](installvalidate-action.md) 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="01c3e-131">If the custom action changes the installation state of features or components, it must be sequenced before the [InstallValidate](installvalidate-action.md) action.</span></span>

 

 



