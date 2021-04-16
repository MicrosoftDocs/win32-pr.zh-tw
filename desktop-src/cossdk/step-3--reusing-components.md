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
# <a name="step-3-reusing-components"></a>步驟3：重複使用元件

## <a name="objectives"></a>目標

在此步驟中，您將瞭解下列各項：

-   可重複使用的元件。
-   如何規劃重複可重複的方案。

## <a name="description"></a>Description

這個 COM + 服務入門的前兩個部分， [步驟1：建立](step-1--creating-a-transactional-component.md) 交易式元件和 [步驟2：跨多個元件延伸交易](step-2--extending-a-transaction-across-multiple-components.md) 示範如何撰寫一個元件來呼叫第二個元件，以協助完成一些工作、更新 Microsoft SQL Server Pubs 資料庫中的作者資訊;所有工作都是由單一交易保護。 範例元件著重于更新作者的資料以及驗證作者的位址，以及 COM + 提供的交易處理、 [JIT 啟用](com--just-in-time-activation.md)和 [並行保護](com--synchronization.md)的工作。

此步驟示範如何重複使用步驟1和2中建立的元件，並查看這對這些元件的設計有何意義。 如下圖所示，這表示建立新的元件，藉 `AddNewAuthor` 由呼叫將新作者新增至資料庫 `UpdateAuthorAddress` 。

![在重複使用元件時顯示流程的圖表。](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

除了重複使用現有的元件功能之外，還會 `AddNewAuthor` 呼叫另一個稱為的新元件 `ValidateAuthorName` 。 如上圖所示， `ValidateAuthorName` 為非交易式。 此元件的交易屬性值會保留為預設設定 (**不支援**) 將其工作從交易中排除。 如步驟3範例程式碼所示，在 `ValidateAuthorName` 資料庫上執行唯讀查詢，而此次要工作的失敗應該不會有可能中止交易。 不過，元件的交易屬性值 `AddNewAuthor` 會設定為 [ **必要**]。

`AddNewAuthor`、 `UpdateAuthorAddress` 和 `ValidateAuthorAddress` 元件都會在交易中投票。 在此交易中， `AddNewAuthor` 是根物件。 COM + 一律會讓在交易中建立的第一個物件成為根物件。

在此範例中，重複使用 `UpdateAuthorAddress` 元件很簡單— COM + 會自動傳遞預期的服務。 但是，如果元件的交易屬性值 `UpdateAuthorAddress` 最初是設定為 **需要 New** 而非 **必要**，則結果會不同。 在表面上，這兩個設定看起來類似;兩者都保證交易。 但 **需要新** 的，但一律會啟動新的交易，而只有當物件的呼叫端為非交易式時，才 **需要** 開始新的交易。 您可以從這種方式中看出 `UpdateAuthorAddress` ，仔細設定和 thoughtfully 的重要性。 否則，COM + 可能會以不同的方式來解讀服務要求，產生兩個不相關的交易，如下圖所示，而不是一個。

![使用「需要新的」重複使用元件時顯示流程的圖表。](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> 當您重複使用元件時，請確定已將服務設定為可支援您想要的結果。

 

## <a name="sample-code"></a>範例程式碼

AddNewAuthor 元件會藉由允許物件維持作用中，直到用戶端釋出物件的參考，以執行新作者的批次新增。


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



`ValidateAuthorName`元件會先驗證作者名稱，再 `AddNewAuthor` 將名稱加入至資料庫。 如果發生非預期的情況，此元件會將錯誤擲回給呼叫端。


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



## <a name="summary"></a>總結

-   有時您不希望元件在交易中投票。
-   COM + 不會在非交易式元件上強制執行 JIT 啟用或平行存取保護。 您可以另外設定這些服務。
-   呼叫元件的設定會影響 COM + 如何解讀所呼叫元件的服務要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[步驟1：建立交易式元件](step-1--creating-a-transactional-component.md)
</dt> <dt>

[步驟2：跨多個元件擴充交易](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[設定交易](configuring-transactions.md)
</dt> <dt>

[擴充性設計](designing-for-scalability.md)
</dt> </dl>

 

 



