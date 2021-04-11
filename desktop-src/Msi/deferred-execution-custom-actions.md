---
description: 延後執行自訂動作的目的是延遲系統變更執行安裝腳本的時間。
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: 延後執行自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09b91793f5d5bbc7be7099c92f8d8f212012d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944559"
---
# <a name="deferred-execution-custom-actions"></a><span data-ttu-id="adaf8-103">延後執行自訂動作</span><span class="sxs-lookup"><span data-stu-id="adaf8-103">Deferred Execution Custom Actions</span></span>

<span data-ttu-id="adaf8-104">延後執行自訂動作的目的是延遲系統變更執行安裝腳本的時間。</span><span class="sxs-lookup"><span data-stu-id="adaf8-104">The purpose of a deferred execution custom action is to delay the execution of a system change to the time when the installation script is executed.</span></span> <span data-ttu-id="adaf8-105">這不同于一般自訂動作或標準動作，在此動作中，安裝程式會在序列資料表或 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)的呼叫中，立即執行動作。</span><span class="sxs-lookup"><span data-stu-id="adaf8-105">This differs from a regular custom action, or a standard action, in which the installer executes the action immediately upon encountering it in a sequence table or in a call to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> <span data-ttu-id="adaf8-106">延後執行自訂動作可讓封裝作者指定執行安裝腳本內特定點的系統作業。</span><span class="sxs-lookup"><span data-stu-id="adaf8-106">A deferred execution custom action enables a package author to specify system operations at a particular point within the execution of the installation script.</span></span>

<span data-ttu-id="adaf8-107">安裝程式在處理安裝順序時，不會執行順延強制自訂動作。</span><span class="sxs-lookup"><span data-stu-id="adaf8-107">The installer does not execute a deferred execution custom action at the time the installation sequence is processed.</span></span> <span data-ttu-id="adaf8-108">相反地，安裝程式會將自訂動作寫入安裝腳本中。</span><span class="sxs-lookup"><span data-stu-id="adaf8-108">Instead the installer writes the custom action into the installation script.</span></span> <span data-ttu-id="adaf8-109">唯一的模式參數是在此案例中，安裝程式所設定的 MSIRUNMODE \_ 排程。</span><span class="sxs-lookup"><span data-stu-id="adaf8-109">The only mode parameter the installer sets in this case is MSIRUNMODE\_SCHEDULED.</span></span> <span data-ttu-id="adaf8-110">如需執行模式參數的說明，請參閱 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 。</span><span class="sxs-lookup"><span data-stu-id="adaf8-110">See [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) for a description of the run mode parameters.</span></span>

<span data-ttu-id="adaf8-111">延後執行自訂動作必須在執行腳本產生之區段內的執行順序資料表中排程。</span><span class="sxs-lookup"><span data-stu-id="adaf8-111">A deferred execution custom action must be scheduled in the execute sequence table within the section that performs script generation.</span></span> <span data-ttu-id="adaf8-112">延後執行自訂動作必須在 [InstallInitialize](installinitialize-action.md) 之後，並且在動作順序中 [InstallFinalize](installfinalize-action.md) 之前。</span><span class="sxs-lookup"><span data-stu-id="adaf8-112">Deferred execution custom actions must come after [InstallInitialize](installinitialize-action.md) and come before [InstallFinalize](installfinalize-action.md) in the action sequence.</span></span>

<span data-ttu-id="adaf8-113">設定屬性、功能狀態、元件狀態或目標目錄的自訂動作，或藉由將資料列插入至順序資料表來排程系統作業，在許多情況下都可以安全地使用立即執行。</span><span class="sxs-lookup"><span data-stu-id="adaf8-113">Custom actions that set properties, feature states, component states, or target directories, or that schedule system operations by inserting rows into sequence tables, can in many cases use immediate execution safely.</span></span> <span data-ttu-id="adaf8-114">不過，直接變更系統或呼叫另一個系統服務的自訂動作，必須延後至執行安裝腳本的時間。</span><span class="sxs-lookup"><span data-stu-id="adaf8-114">However, custom actions that change the system directly, or call another system service, must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="adaf8-115">如需其自訂動作和主要安裝執行緒之間可能發生衝突的詳細資訊，請參閱 [同步和非同步自訂動作](synchronous-and-asynchronous-custom-actions.md) 。</span><span class="sxs-lookup"><span data-stu-id="adaf8-115">See [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md) for more information about potential clashes between their custom actions and the main installation thread.</span></span>

<span data-ttu-id="adaf8-116">因為安裝腳本可以在寫入的安裝會話之外執行，所以在安裝腳本執行期間，會話可能不會再存在。</span><span class="sxs-lookup"><span data-stu-id="adaf8-116">Because the installation script can be executed outside of the installation session in which it was written, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="adaf8-117">這表示，順延強制自訂動作無法使用安裝順序期間的原始會話控制碼和屬性資料集。</span><span class="sxs-lookup"><span data-stu-id="adaf8-117">This means that the original session handle and property data set during the installation sequence is not available to a deferred execution custom action.</span></span> <span data-ttu-id="adaf8-118">延遲的自訂動作會呼叫動態連結程式庫 (Dll) 傳遞控制碼，該控制碼只能用來取得非常有限的資訊，如 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="adaf8-118">Deferred custom actions that call dynamic-link libraries (DLLs) pass a handle which can only be used to obtain a very limited amount of information, as described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="adaf8-119">請注意，延遲的自訂動作（包括 [復原自訂動作](rollback-custom-actions.md) 和 [認可自訂動作](commit-custom-actions.md)）是唯一可在使用者安全性內容外部執行的動作類型。</span><span class="sxs-lookup"><span data-stu-id="adaf8-119">Note that deferred custom actions, including [rollback custom actions](rollback-custom-actions.md) and [commit custom actions](commit-custom-actions.md), are the only types of actions that can run outside the users security context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adaf8-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="adaf8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adaf8-121">自訂動作 In-Script 執行選項</span><span class="sxs-lookup"><span data-stu-id="adaf8-121">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="adaf8-122">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="adaf8-122">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> </dl>

 

 



