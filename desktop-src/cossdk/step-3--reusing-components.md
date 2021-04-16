---
description: 步驟3：重複使用元件
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 步驟3：重複使用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566724"
---
# <a name="step-3-reusing-components"></a><span data-ttu-id="82a59-103">步驟3：重複使用元件</span><span class="sxs-lookup"><span data-stu-id="82a59-103">Step 3: Reusing Components</span></span>

## <a name="objectives"></a><span data-ttu-id="82a59-104">目標</span><span class="sxs-lookup"><span data-stu-id="82a59-104">Objectives</span></span>

<span data-ttu-id="82a59-105">在此步驟中，您將瞭解下列各項：</span><span class="sxs-lookup"><span data-stu-id="82a59-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="82a59-106">可重複使用的元件。</span><span class="sxs-lookup"><span data-stu-id="82a59-106">Reusable components.</span></span>
-   <span data-ttu-id="82a59-107">如何規劃重複可重複的方案。</span><span class="sxs-lookup"><span data-stu-id="82a59-107">How to plan for reusability.</span></span>

## <a name="description"></a><span data-ttu-id="82a59-108">Description</span><span class="sxs-lookup"><span data-stu-id="82a59-108">Description</span></span>

<span data-ttu-id="82a59-109">這個 COM + 服務入門的前兩個部分， [步驟1：建立](step-1--creating-a-transactional-component.md) 交易式元件和 [步驟2：跨多個元件延伸交易](step-2--extending-a-transaction-across-multiple-components.md) 示範如何撰寫一個元件來呼叫第二個元件，以協助完成一些工作、更新 Microsoft SQL Server Pubs 資料庫中的作者資訊;所有工作都是由單一交易保護。</span><span class="sxs-lookup"><span data-stu-id="82a59-109">Two previous parts of this COM+ services primer, [Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) and [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md) show how to write one component that calls a second component to assist in completing some work, updating author information in the Microsoft SQL Server Pubs database; all work is protected by a single transaction.</span></span> <span data-ttu-id="82a59-110">範例元件著重于更新作者的資料以及驗證作者的位址，以及 COM + 提供的交易處理、 [JIT 啟用](com--just-in-time-activation.md)和 [並行保護](com--synchronization.md)的工作。</span><span class="sxs-lookup"><span data-stu-id="82a59-110">The sample components focused on the work of updating an author's data and verifying the author's address, and COM+ provided transaction processing, [JIT activation](com--just-in-time-activation.md), and [concurrency protection](com--synchronization.md).</span></span>

<span data-ttu-id="82a59-111">此步驟示範如何重複使用步驟1和2中建立的元件，並查看這對這些元件的設計有何意義。</span><span class="sxs-lookup"><span data-stu-id="82a59-111">This step demonstrates how to reuse the components created in steps 1 and 2 and looks at what this means to the design of those components.</span></span> <span data-ttu-id="82a59-112">如下圖所示，這表示建立新的元件，藉 `AddNewAuthor` 由呼叫將新作者新增至資料庫 `UpdateAuthorAddress` 。</span><span class="sxs-lookup"><span data-stu-id="82a59-112">As shown in the following illustration, this means creating a new component, `AddNewAuthor`, that adds new authors to the database by calling `UpdateAuthorAddress`.</span></span>

![在重複使用元件時顯示流程的圖表。](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

<span data-ttu-id="82a59-114">除了重複使用現有的元件功能之外，還會 `AddNewAuthor` 呼叫另一個稱為的新元件 `ValidateAuthorName` 。</span><span class="sxs-lookup"><span data-stu-id="82a59-114">In addition to reusing existing component functionality, `AddNewAuthor` calls another new component called `ValidateAuthorName`.</span></span> <span data-ttu-id="82a59-115">如上圖所示， `ValidateAuthorName` 為非交易式。</span><span class="sxs-lookup"><span data-stu-id="82a59-115">As the preceding illustration shows, `ValidateAuthorName` is non-transactional.</span></span> <span data-ttu-id="82a59-116">此元件的交易屬性值會保留為預設設定 (**不支援**) 將其工作從交易中排除。</span><span class="sxs-lookup"><span data-stu-id="82a59-116">The transaction attribute value for this component is left at its default setting (**Not Supported**) to exclude its work from the transaction.</span></span> <span data-ttu-id="82a59-117">如步驟3範例程式碼所示，在 `ValidateAuthorName` 資料庫上執行唯讀查詢，而此次要工作的失敗應該不會有可能中止交易。</span><span class="sxs-lookup"><span data-stu-id="82a59-117">As shown in the step 3 sample code, `ValidateAuthorName` performs read-only queries on the database, and the failure of this minor task should not have the potential to abort the transaction.</span></span> <span data-ttu-id="82a59-118">不過，元件的交易屬性值 `AddNewAuthor` 會設定為 [ **必要**]。</span><span class="sxs-lookup"><span data-stu-id="82a59-118">However, the transaction attribute value of the `AddNewAuthor` component is set to **Required**.</span></span>

<span data-ttu-id="82a59-119">`AddNewAuthor`、 `UpdateAuthorAddress` 和 `ValidateAuthorAddress` 元件都會在交易中投票。</span><span class="sxs-lookup"><span data-stu-id="82a59-119">The `AddNewAuthor`, `UpdateAuthorAddress`, and `ValidateAuthorAddress` components all vote in the transaction.</span></span> <span data-ttu-id="82a59-120">在此交易中， `AddNewAuthor` 是根物件。</span><span class="sxs-lookup"><span data-stu-id="82a59-120">In this transaction, `AddNewAuthor` is the root object.</span></span> <span data-ttu-id="82a59-121">COM + 一律會讓在交易中建立的第一個物件成為根物件。</span><span class="sxs-lookup"><span data-stu-id="82a59-121">COM+ always makes the first object created in the transaction the root object.</span></span>

<span data-ttu-id="82a59-122">在此範例中，重複使用 `UpdateAuthorAddress` 元件很簡單— COM + 會自動傳遞預期的服務。</span><span class="sxs-lookup"><span data-stu-id="82a59-122">In this example, reusing the `UpdateAuthorAddress` component is easy—COM+ automatically delivers the expected services.</span></span> <span data-ttu-id="82a59-123">但是，如果元件的交易屬性值 `UpdateAuthorAddress` 最初是設定為 **需要 New** 而非 **必要**，則結果會不同。</span><span class="sxs-lookup"><span data-stu-id="82a59-123">However, the results would be different if the transaction attribute value of the `UpdateAuthorAddress` component were initially set to **Requires New** instead of **Required**.</span></span> <span data-ttu-id="82a59-124">在表面上，這兩個設定看起來類似;兩者都保證交易。</span><span class="sxs-lookup"><span data-stu-id="82a59-124">On the surface, both settings appear similar; both guarantee a transaction.</span></span> <span data-ttu-id="82a59-125">但 **需要新** 的，但一律會啟動新的交易，而只有當物件的呼叫端為非交易式時，才 **需要** 開始新的交易。</span><span class="sxs-lookup"><span data-stu-id="82a59-125">**Requires New**, however, always starts a new transaction, while **Required** starts a new transaction only when the object's caller is non-transactional.</span></span> <span data-ttu-id="82a59-126">您可以從這種方式中看出 `UpdateAuthorAddress` ，仔細設定和 thoughtfully 的重要性。</span><span class="sxs-lookup"><span data-stu-id="82a59-126">You can see from this how important it was to configure `UpdateAuthorAddress` carefully and thoughtfully.</span></span> <span data-ttu-id="82a59-127">否則，COM + 可能會以不同的方式來解讀服務要求，產生兩個不相關的交易，如下圖所示，而不是一個。</span><span class="sxs-lookup"><span data-stu-id="82a59-127">Otherwise, COM+ might have interpreted the service request differently, generating two unrelated transactions, as shown in the following illustration, instead of one.</span></span>

![使用「需要新的」重複使用元件時顯示流程的圖表。](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> <span data-ttu-id="82a59-129">當您重複使用元件時，請確定已將服務設定為可支援您想要的結果。</span><span class="sxs-lookup"><span data-stu-id="82a59-129">When you reuse components, make sure the services are configured to support your desired outcome.</span></span>

 

## <a name="sample-code"></a><span data-ttu-id="82a59-130">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="82a59-130">Sample code</span></span>

<span data-ttu-id="82a59-131">AddNewAuthor 元件會藉由允許物件維持作用中，直到用戶端釋出物件的參考，以執行新作者的批次新增。</span><span class="sxs-lookup"><span data-stu-id="82a59-131">The AddNewAuthor component performs batch additions of new authors by allowing the object to remain active until the client releases its reference to the object.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



<span data-ttu-id="82a59-132">`ValidateAuthorName`元件會先驗證作者名稱，再 `AddNewAuthor` 將名稱加入至資料庫。</span><span class="sxs-lookup"><span data-stu-id="82a59-132">The `ValidateAuthorName` component validates author names before `AddNewAuthor` adds the name to the database.</span></span> <span data-ttu-id="82a59-133">如果發生非預期的情況，此元件會將錯誤擲回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="82a59-133">This component throws an error back to its caller if something unexpected happens.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a><span data-ttu-id="82a59-134">總結</span><span class="sxs-lookup"><span data-stu-id="82a59-134">Summary</span></span>

-   <span data-ttu-id="82a59-135">有時您不希望元件在交易中投票。</span><span class="sxs-lookup"><span data-stu-id="82a59-135">There are times when you don't want a component to vote in the transaction.</span></span>
-   <span data-ttu-id="82a59-136">COM + 不會在非交易式元件上強制執行 JIT 啟用或平行存取保護。</span><span class="sxs-lookup"><span data-stu-id="82a59-136">COM+ does not enforce JIT activation or concurrency protection on non-transactional components.</span></span> <span data-ttu-id="82a59-137">您可以另外設定這些服務。</span><span class="sxs-lookup"><span data-stu-id="82a59-137">You may configure these services separately.</span></span>
-   <span data-ttu-id="82a59-138">呼叫元件的設定會影響 COM + 如何解讀所呼叫元件的服務要求。</span><span class="sxs-lookup"><span data-stu-id="82a59-138">A calling component's configuration affects how COM+ interprets the service requests of the called component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82a59-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="82a59-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a59-140">步驟1：建立交易式元件</span><span class="sxs-lookup"><span data-stu-id="82a59-140">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="82a59-141">步驟2：跨多個元件擴充交易</span><span class="sxs-lookup"><span data-stu-id="82a59-141">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="82a59-142">設定交易</span><span class="sxs-lookup"><span data-stu-id="82a59-142">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="82a59-143">擴充性設計</span><span class="sxs-lookup"><span data-stu-id="82a59-143">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> </dl>

 

 



