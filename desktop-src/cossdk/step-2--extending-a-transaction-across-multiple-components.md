---
description: 步驟2：跨多個元件擴充交易
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 步驟2：跨多個元件擴充交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321351"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="bb7eb-103">步驟2：跨元件擴充交易</span><span class="sxs-lookup"><span data-stu-id="bb7eb-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="bb7eb-104">目標</span><span class="sxs-lookup"><span data-stu-id="bb7eb-104">Objectives</span></span>

<span data-ttu-id="bb7eb-105">在此步驟中，您將瞭解下列各項：</span><span class="sxs-lookup"><span data-stu-id="bb7eb-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="bb7eb-106">交易流程</span><span class="sxs-lookup"><span data-stu-id="bb7eb-106">Transaction flow</span></span>
-   <span data-ttu-id="bb7eb-107">多個物件在交易中的投票方式</span><span class="sxs-lookup"><span data-stu-id="bb7eb-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="bb7eb-108">Description</span><span class="sxs-lookup"><span data-stu-id="bb7eb-108">Description</span></span>

<span data-ttu-id="bb7eb-109">[步驟1：建立交易元件](step-1--creating-a-transactional-component.md) 示範如何撰寫簡單的交易元件，以更新 Microsoft SQL Server Pubs 資料庫中的作者資訊。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="bb7eb-110">步驟2顯示在多個元件之間擴充交易時所發生的情況。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="bb7eb-111">為了保持 COM + 程式設計模型，在 `UpdateAuthorAddress` 完成其工作的過程中，會呼叫另一個元件。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="bb7eb-112">第二個元件會 `ValidateAuthorAddress` 驗證作者的位址，並將結果傳回給它的呼叫者 `UpdateAuthorAddress` 。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="bb7eb-113">與其呼叫端不同 `ValidateAuthorAddress` 的是，不需要交易，但仍可參與其呼叫端的交易。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="bb7eb-114">在這個步驟中，其交易屬性值會設定為 [ **支援**]，如下圖所示，這會將現有的交易擴充至新的物件。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![顯示將現有交易擴充至新物件的圖表。](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="bb7eb-116">只有當呼叫端為交易式時， **支援** 的屬性值才會) 現有交易中擴充 (或流程。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="bb7eb-117">當 `UpdateAuthorAddress` 呼叫時 `ValidateAuthorAddress` ，com + 會先查看呼叫端的內容，以查看它是否為交易式。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="bb7eb-118">然後 COM + 會查看在上設定的服務屬性 `ValidateAuthorAddress` ，並將指派給呼叫端物件的相同交易識別碼指派給新的物件。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="bb7eb-119">若要進一步瞭解此程式，請參閱 [內容啟用](context-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="bb7eb-120">因為它們共用相同的交易識別碼，所以這兩個物件都必須順利完成其工作，否則 COM + 會中止交易， (復原對 Pubs 資料庫) 所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="bb7eb-121">參與交易的所有物件都會投票至認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="bb7eb-122">當您在程式碼中包含投票指令時，會明確地進行投票，如下列步驟1範例程式碼中所示的解壓縮程式代碼，該程式碼會建立 `UpdateAuthorAddress` 元件：</span><span class="sxs-lookup"><span data-stu-id="bb7eb-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="bb7eb-123">投票也會隱含地發生，如同在元件中所做的一樣 `ValidateAuthorAddress` 。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="bb7eb-124">除非物件另行宣告，否則 COM + 會假設物件已順利完成其工作，但尚未準備好停用。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="bb7eb-125">COM + 會進行下列假設：</span><span class="sxs-lookup"><span data-stu-id="bb7eb-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="bb7eb-126">當 `ValidateAuthorAddress` 回到其呼叫端時，COM + 會以認可的形式讀取其投票。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="bb7eb-127">除非在停用根物件（在此案例中為交易中的第一個物件，即在此案例中為物件），否則 COM + 不會計入投票 `UpdateAuthorAddress` 。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="bb7eb-128">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="bb7eb-128">Sample code</span></span>

<span data-ttu-id="bb7eb-129">`ValidateAuthorAddress`元件會簡單檢查作者的位址。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="bb7eb-130">因為不 `UpdateAuthorAddress` 會明確投票，COM + 會使用預設投票設定。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="bb7eb-131">總結</span><span class="sxs-lookup"><span data-stu-id="bb7eb-131">Summary</span></span>

-   <span data-ttu-id="bb7eb-132">將元件的交易屬性設定為 [ **支援** ] 可能會導致在呼叫物件的交易中建立新的物件。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="bb7eb-133">COM + 會查看呼叫端的內容，以判斷新物件的交易狀態。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="bb7eb-134">如果呼叫端是交易式的，COM + 會將交易流動至新的物件。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="bb7eb-135">參與相同交易的所有物件都會共用一般交易識別碼，而 COM + 會從物件的內容讀取此識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="bb7eb-136">交易中的每個物件都會與其他物件分開投票。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="bb7eb-137">當根物件停用時，COM + 會計算投票。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="bb7eb-138">您可以在認可和中止之間切換物件的交易，直到 COM + 停用物件為止，或直到 COM + 停用根物件並結束交易為止。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="bb7eb-139">只有最後一個投票設定計數。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-139">Only the last vote setting counts.</span></span> <span data-ttu-id="bb7eb-140">[**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)和 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)介面會提供方法，並產生如下表所示的類似投票結果。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="bb7eb-141">您可以使用其中一個介面，在交易中明確地投票。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="bb7eb-142">[**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) 組合方法</span><span class="sxs-lookup"><span data-stu-id="bb7eb-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="bb7eb-143">[**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 對等方法</span><span class="sxs-lookup"><span data-stu-id="bb7eb-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="bb7eb-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="bb7eb-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="bb7eb-146">**SetComplete**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="bb7eb-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="bb7eb-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="bb7eb-149">**EnableCommit**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="bb7eb-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="bb7eb-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="bb7eb-152">**SetAbort**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="bb7eb-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="bb7eb-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="bb7eb-155">**DisableCommit**</span><span class="sxs-lookup"><span data-stu-id="bb7eb-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="bb7eb-156">除非元件有明確的投票，否則 COM + 會將物件的投票設定為對等的 [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) 。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="bb7eb-157">明確投票可以減少交易的整體持續時間，以及釋出昂貴的資源鎖定。</span><span class="sxs-lookup"><span data-stu-id="bb7eb-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb7eb-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb7eb-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb7eb-159">步驟1：建立交易式元件</span><span class="sxs-lookup"><span data-stu-id="bb7eb-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="bb7eb-160">步驟3：重複使用元件</span><span class="sxs-lookup"><span data-stu-id="bb7eb-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="bb7eb-161">內容啟用</span><span class="sxs-lookup"><span data-stu-id="bb7eb-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="bb7eb-162">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="bb7eb-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




