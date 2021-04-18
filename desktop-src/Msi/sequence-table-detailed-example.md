---
description: 以下是 sequence 資料表的範例。
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: 順序資料表詳細範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978179"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="f1e2a-103">順序資料表詳細範例</span><span class="sxs-lookup"><span data-stu-id="f1e2a-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="f1e2a-104">以下是 sequence 資料表的範例。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="f1e2a-105">動作</span><span class="sxs-lookup"><span data-stu-id="f1e2a-105">Action</span></span>                                          | <span data-ttu-id="f1e2a-106">條件</span><span class="sxs-lookup"><span data-stu-id="f1e2a-106">Condition</span></span>                                                       | <span data-ttu-id="f1e2a-107">順序</span><span class="sxs-lookup"><span data-stu-id="f1e2a-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="f1e2a-108">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="f1e2a-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="f1e2a-109">AppSearch</span><span class="sxs-lookup"><span data-stu-id="f1e2a-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="f1e2a-110">200</span><span class="sxs-lookup"><span data-stu-id="f1e2a-110">200</span></span>      |
| [<span data-ttu-id="f1e2a-111">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="f1e2a-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="f1e2a-112">CCP \_ 測試</span><span class="sxs-lookup"><span data-stu-id="f1e2a-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="f1e2a-113">300</span><span class="sxs-lookup"><span data-stu-id="f1e2a-113">300</span></span>      |
| <span data-ttu-id="f1e2a-114">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-114">CCPDialog</span></span>                                       | <span data-ttu-id="f1e2a-115">不是 \_ CCP \_ 成功</span><span class="sxs-lookup"><span data-stu-id="f1e2a-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="f1e2a-116">400</span><span class="sxs-lookup"><span data-stu-id="f1e2a-116">400</span></span>      |
| <span data-ttu-id="f1e2a-117">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="f1e2a-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="f1e2a-118">未 [**安裝**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f1e2a-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="f1e2a-119">500</span><span class="sxs-lookup"><span data-stu-id="f1e2a-119">500</span></span>      |
| [<span data-ttu-id="f1e2a-120">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="f1e2a-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="f1e2a-121">600</span><span class="sxs-lookup"><span data-stu-id="f1e2a-121">600</span></span>      |
| [<span data-ttu-id="f1e2a-122">FileCost</span><span class="sxs-lookup"><span data-stu-id="f1e2a-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="f1e2a-123">700</span><span class="sxs-lookup"><span data-stu-id="f1e2a-123">700</span></span>      |
| [<span data-ttu-id="f1e2a-124">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f1e2a-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="f1e2a-125">800</span><span class="sxs-lookup"><span data-stu-id="f1e2a-125">800</span></span>      |
| <span data-ttu-id="f1e2a-126">>installdialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-126">InstallDialog</span></span>                                   | <span data-ttu-id="f1e2a-127">未 [**安裝**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="f1e2a-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="f1e2a-128">900</span><span class="sxs-lookup"><span data-stu-id="f1e2a-128">900</span></span>      |
| <span data-ttu-id="f1e2a-129">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="f1e2a-130">[**已安裝**](installed.md) 而不是 [**繼續**](resume.md)</span><span class="sxs-lookup"><span data-stu-id="f1e2a-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="f1e2a-131">1000</span><span class="sxs-lookup"><span data-stu-id="f1e2a-131">1000</span></span>     |
| <span data-ttu-id="f1e2a-132">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="f1e2a-133">1100</span><span class="sxs-lookup"><span data-stu-id="f1e2a-133">1100</span></span>     |
| [<span data-ttu-id="f1e2a-134">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="f1e2a-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="f1e2a-135">1200</span><span class="sxs-lookup"><span data-stu-id="f1e2a-135">1200</span></span>     |
| [<span data-ttu-id="f1e2a-136">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="f1e2a-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="f1e2a-137">1300</span><span class="sxs-lookup"><span data-stu-id="f1e2a-137">1300</span></span>     |
| [<span data-ttu-id="f1e2a-138">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f1e2a-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="f1e2a-139">1400</span><span class="sxs-lookup"><span data-stu-id="f1e2a-139">1400</span></span>     |
| <span data-ttu-id="f1e2a-140">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="f1e2a-140">MyCustomAction</span></span>                                  | <span data-ttu-id="f1e2a-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="f1e2a-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="f1e2a-142">1500</span><span class="sxs-lookup"><span data-stu-id="f1e2a-142">1500</span></span>     |
| [<span data-ttu-id="f1e2a-143">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="f1e2a-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="f1e2a-144">1600</span><span class="sxs-lookup"><span data-stu-id="f1e2a-144">1600</span></span>     |



 

<span data-ttu-id="f1e2a-145">此順序表中的下列動作是由安裝程式所定義，而且是標準動作的範例：</span><span class="sxs-lookup"><span data-stu-id="f1e2a-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="f1e2a-146">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="f1e2a-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="f1e2a-147">AppSearch</span><span class="sxs-lookup"><span data-stu-id="f1e2a-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="f1e2a-148">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="f1e2a-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="f1e2a-149">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="f1e2a-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="f1e2a-150">FileCost</span><span class="sxs-lookup"><span data-stu-id="f1e2a-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="f1e2a-151">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f1e2a-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="f1e2a-152">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="f1e2a-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="f1e2a-153">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f1e2a-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="f1e2a-154">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f1e2a-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="f1e2a-155">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="f1e2a-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="f1e2a-156">下列動作是由資料表的作者所定義，而且是 [自訂動作](custom-actions.md) 的範例，而且必須列在 [CustomAction 資料表](customaction-table.md)中：</span><span class="sxs-lookup"><span data-stu-id="f1e2a-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="f1e2a-157">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="f1e2a-157">MyCustomConfig</span></span>

 

<span data-ttu-id="f1e2a-158">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="f1e2a-158">MyCustomAction</span></span>

<span data-ttu-id="f1e2a-159">[動作] 欄位中的其餘專案是 [對話方塊資料表](dialog-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="f1e2a-160">如果條件欄位評估為 True，則會指定將顯示之對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="f1e2a-161">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-161">CCPDialog</span></span>

 

<span data-ttu-id="f1e2a-162">>installdialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-162">InstallDialog</span></span>

 

<span data-ttu-id="f1e2a-163">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="f1e2a-164">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="f1e2a-164">ActionDialog</span></span>

<span data-ttu-id="f1e2a-165">如果此欄位中的屬性或運算式為 False，則 [條件] 資料行會讓安裝程式略過該動作。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="f1e2a-166">[**已安裝**](installed.md)的屬性和 [**RESUME**](resume.md)屬性是安裝程式所設定之屬性的範例。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="f1e2a-167">如果已安裝產品，則已 [**安裝**](installed.md) 的屬性會設定為 true，如果繼續已暫停的安裝，則會設定 [**RESUME**](resume.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="f1e2a-168">CCP \_ 測試和 NOT \_ CCP \_ SUCCESS 屬性是可在使用者安裝應用程式時于命令列設定的屬性範例。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="f1e2a-169">所有動作都會依序執行，並具有下列條件式步驟：</span><span class="sxs-lookup"><span data-stu-id="f1e2a-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="f1e2a-170">只有在已設定 CCP 測試時，才會執行 CPPSearch \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="f1e2a-171">只有在未設定 [CCP SUCCESS] 時，才會執行 CCPDialog \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="f1e2a-172">只有在已安裝此產品，且這不是在暫停後繼續執行的安裝時，才會執行 MaintenanceDialog。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="f1e2a-173">只有當 Condition 資料行中的運算式為 True 時，才會執行 MyCustomAction。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="f1e2a-174">運算式 $MyComponent > 2 是指稱為 MyComponent 的元件的動作狀態。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="f1e2a-175">此條件表示 MyCustomAction 只有在 MyComponent 設定為已安裝時才應該執行。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="f1e2a-176">如需動作狀態和選取狀態的詳細資訊，請參閱 [**FeatureRequestState**](session-featurerequeststate.md) 屬性、 [功能資料表](feature-table.md)和 [InstallFiles 動作](installfiles-action.md)。</span><span class="sxs-lookup"><span data-stu-id="f1e2a-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1e2a-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1e2a-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e2a-178">使用屬性</span><span class="sxs-lookup"><span data-stu-id="f1e2a-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="f1e2a-179">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="f1e2a-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



