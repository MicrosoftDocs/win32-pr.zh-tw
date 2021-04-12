---
description: 步驟1：建立交易式元件
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 步驟1：建立交易式元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104321348"
---
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="8efcb-103">步驟1：建立交易式元件</span><span class="sxs-lookup"><span data-stu-id="8efcb-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="8efcb-104">目標</span><span class="sxs-lookup"><span data-stu-id="8efcb-104">Objectives</span></span>

<span data-ttu-id="8efcb-105">在此步驟中，您將會瞭解下列各項：</span><span class="sxs-lookup"><span data-stu-id="8efcb-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="8efcb-106">如何在 Microsoft Visual Basic 中撰寫交易元件</span><span class="sxs-lookup"><span data-stu-id="8efcb-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="8efcb-107">COM + 服務的預設設定是什麼</span><span class="sxs-lookup"><span data-stu-id="8efcb-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="8efcb-108">如何設定 COM + 服務</span><span class="sxs-lookup"><span data-stu-id="8efcb-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="8efcb-109">Description</span><span class="sxs-lookup"><span data-stu-id="8efcb-109">Description</span></span>

<span data-ttu-id="8efcb-110">UpdateAuthorAddress 元件是在此區段中建立的元件，會更新 Pubs 資料庫中現有作者的位址。</span><span class="sxs-lookup"><span data-stu-id="8efcb-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="8efcb-111">Pubs 資料庫是 Microsoft SQL Server 隨附的範例資料庫。</span><span class="sxs-lookup"><span data-stu-id="8efcb-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="8efcb-112">它包含作者姓名、位址和書籍標題等發行資訊。</span><span class="sxs-lookup"><span data-stu-id="8efcb-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="8efcb-113">Pubs 是此入門中所使用的資料存放區。</span><span class="sxs-lookup"><span data-stu-id="8efcb-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="8efcb-114">因為 UpdateAuthorAddress 會更新資料存放區，建議您在交易中包含工作，如下圖所示，如此一來，當用戶端呼叫元件時，COM + 會自動啟動交易，並在該交易 (resource manager) 登錄資料庫。</span><span class="sxs-lookup"><span data-stu-id="8efcb-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="8efcb-115"> (如需有關 COM + 中交易的詳細資訊，請參閱 [Com + 交易](com--transactions.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="8efcb-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![此圖顯示具有 UpdateAuthorAddress 的 COM + 交易。](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="8efcb-117">若要使 UpdateAuthorAddress 成為交易元件，必須執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8efcb-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="8efcb-118">必須寫入元件。</span><span class="sxs-lookup"><span data-stu-id="8efcb-118">The component must be written.</span></span> <span data-ttu-id="8efcb-119">為了額外保護，會新增副程式，確認 COM + 已在交易中建立物件。</span><span class="sxs-lookup"><span data-stu-id="8efcb-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="8efcb-120">此外，元件中包含基本的錯誤處理，以簡化錯誤復原。</span><span class="sxs-lookup"><span data-stu-id="8efcb-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="8efcb-121">交易驗證和錯誤處理會增強元件的可靠性。</span><span class="sxs-lookup"><span data-stu-id="8efcb-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="8efcb-122"> (如需完整的 UpdateAuthorAddress 元件清單，請參閱步驟1的範例程式碼。 ) </span><span class="sxs-lookup"><span data-stu-id="8efcb-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="8efcb-123">將元件加入至 COM + 應用程式並安裝應用程式之後，交易屬性必須設定為 [ **必要**]，以確保 com + 在交易中建立每個 UpdateAuthorAddress 物件。</span><span class="sxs-lookup"><span data-stu-id="8efcb-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="8efcb-124">如需有關如何設定元件之交易屬性的指示，請參閱 [設定交易屬性](setting-the-transaction-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="8efcb-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="8efcb-125">在元件上設定交易屬性，會定義 COM + 如何建立每個與交易有關的物件。</span><span class="sxs-lookup"><span data-stu-id="8efcb-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="8efcb-126">交易屬性值會被 **忽略**、 **不支援**、 **支援**、 **必要**，且 **需要新** 的。</span><span class="sxs-lookup"><span data-stu-id="8efcb-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="8efcb-127">**必要** 值不是元件的預設屬性值之一。</span><span class="sxs-lookup"><span data-stu-id="8efcb-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="8efcb-128">COM + 會將交易服務系結至即時 (JIT) 啟用和平行存取。</span><span class="sxs-lookup"><span data-stu-id="8efcb-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="8efcb-129">當您將元件宣告為交易式時，COM + 也會強制執行 JIT 啟用和並行保護 (同步處理) 。</span><span class="sxs-lookup"><span data-stu-id="8efcb-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="8efcb-130">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="8efcb-130">Sample code</span></span>

<span data-ttu-id="8efcb-131">UpdateAuthorAddress 元件會開啟與 Pubs 資料庫的連接，讓使用者可以修改作者的名稱、位址或合約狀態。</span><span class="sxs-lookup"><span data-stu-id="8efcb-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="8efcb-132">它也會呼叫第二個元件，這會在 [步驟2：跨多個元件延伸交易](step-2--extending-a-transaction-across-multiple-components.md)時討論。</span><span class="sxs-lookup"><span data-stu-id="8efcb-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="8efcb-133">若要在 Microsoft Visual Basic 專案中使用下列程式碼，請開啟新的 ActiveX.dll 專案，並將參考新增至 Microsoft ActiveX Data Objects 程式庫和 COM + 服務型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="8efcb-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="8efcb-134">本入門中的範例程式碼是為了說明的目的，對於實際的預備和生產來說可能不是最有效率的。</span><span class="sxs-lookup"><span data-stu-id="8efcb-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a><span data-ttu-id="8efcb-135">總結</span><span class="sxs-lookup"><span data-stu-id="8efcb-135">Summary</span></span>

-   <span data-ttu-id="8efcb-136">COM + 會指派預設屬性值。</span><span class="sxs-lookup"><span data-stu-id="8efcb-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="8efcb-137">您可以重新設定大部分的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="8efcb-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="8efcb-138">將元件的交易屬性設定為 [ **必要** ] 可保證 com + 必須在交易中建立該元件的每個實例，但不一定會啟動新的交易。</span><span class="sxs-lookup"><span data-stu-id="8efcb-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="8efcb-139">確認交易是否存在，會確認元件的交易屬性值不會不慎重設為非交易值，例如「 **略** 過」或「 **不支援**」。</span><span class="sxs-lookup"><span data-stu-id="8efcb-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="8efcb-140">處理錯誤可讓您的元件更可靠且更容易進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="8efcb-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="8efcb-141">COM + 會針對交易元件強制執行 [JIT 啟用](com--just-in-time-activation.md) 和 [並行保護](com--synchronization.md) 服務。</span><span class="sxs-lookup"><span data-stu-id="8efcb-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="8efcb-142">當您完成資料庫連接時，請將其關閉，以允許相同交易中的另一個元件重複使用連接集區中的連接。</span><span class="sxs-lookup"><span data-stu-id="8efcb-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="8efcb-143"> (連接共用不應與 [物件](com--object-pooling.md)共用混淆。 ) </span><span class="sxs-lookup"><span data-stu-id="8efcb-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="8efcb-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="8efcb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8efcb-145">步驟2：跨多個元件擴充交易</span><span class="sxs-lookup"><span data-stu-id="8efcb-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="8efcb-146">步驟3：重複使用元件</span><span class="sxs-lookup"><span data-stu-id="8efcb-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="8efcb-147">COM + 即時啟用</span><span class="sxs-lookup"><span data-stu-id="8efcb-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="8efcb-148">COM + 同步處理</span><span class="sxs-lookup"><span data-stu-id="8efcb-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="8efcb-149">設定交易</span><span class="sxs-lookup"><span data-stu-id="8efcb-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="8efcb-150">建立 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="8efcb-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="8efcb-151">設定交易屬性</span><span class="sxs-lookup"><span data-stu-id="8efcb-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



