---
description: 步驟1：建立交易式元件
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 步驟1：建立交易式元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f5c87fb5c5f615ee04a3233f1a563d5ae5230e4dd18908c78e94092ff0f5c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305405"
---
# <a name="step-1-creating-a-transactional-component"></a>步驟1：建立交易式元件

## <a name="objectives"></a>目標

在此步驟中，您將會瞭解下列各項：

-   如何在 Microsoft Visual Basic 中撰寫交易元件
-   COM + 服務的預設設定是什麼
-   如何設定 COM + 服務

## <a name="description"></a>描述

UpdateAuthorAddress 元件是在此區段中建立的元件，會更新 Pubs 資料庫中現有作者的位址。 Pubs 資料庫是 Microsoft SQL Server 隨附的範例資料庫。 它包含作者姓名、位址和書籍標題等發行資訊。

> [!Note]  
> Pubs 是此入門中所使用的資料存放區。

 

因為 UpdateAuthorAddress 會更新資料存放區，建議您在交易中包含工作，如下圖所示，如此一來，當用戶端呼叫元件時，COM + 會自動啟動交易，並在該交易 (resource manager) 登錄資料庫。  (如需有關 COM + 中交易的詳細資訊，請參閱 [Com + 交易](com--transactions.md)。 ) 

![此圖顯示具有 UpdateAuthorAddress 的 COM + 交易。](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

若要使 UpdateAuthorAddress 成為交易元件，必須執行下列步驟：

1.  必須寫入元件。 為了額外保護，會新增副程式，確認 COM + 已在交易中建立物件。 此外，元件中包含基本的錯誤處理，以簡化錯誤復原。 交易驗證和錯誤處理會增強元件的可靠性。  (如需完整的 UpdateAuthorAddress 元件清單，請參閱步驟1的範例程式碼。 ) 
2.  將元件加入至 COM + 應用程式並安裝應用程式之後，交易屬性必須設定為 [ **必要**]，以確保 com + 在交易中建立每個 UpdateAuthorAddress 物件。 如需有關如何設定元件之交易屬性的指示，請參閱 [設定交易屬性](setting-the-transaction-attribute.md)。
    > [!Note]  
    > 在元件上設定交易屬性，會定義 COM + 如何建立每個與交易有關的物件。 交易屬性值會被 **忽略**、 **不支援**、 **支援**、 **必要**，且 **需要新** 的。 **必要** 值不是元件的預設屬性值之一。

     

COM + 會將交易服務系結至即時 (JIT) 啟用和平行存取。 當您將元件宣告為交易式時，COM + 也會強制執行 JIT 啟用和並行保護 (同步處理) 。

## <a name="sample-code"></a>範例程式碼

UpdateAuthorAddress 元件會開啟與 Pubs 資料庫的連接，讓使用者可以修改作者的名稱、位址或合約狀態。 它也會呼叫第二個元件，這會在 [步驟2：跨多個元件延伸交易](step-2--extending-a-transaction-across-multiple-components.md)時討論。

若要在 microsoft Visual Basic 專案中使用下列程式碼，請開啟新的 ActiveX.dll 專案，並將參考新增至 microsoft ActiveX Data Objects 程式庫和 com + 服務型別程式庫。

> [!Note]  
> 本入門中的範例程式碼是為了說明的目的，對於實際的預備和生產來說可能不是最有效率的。

 


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



## <a name="summary"></a>摘要

-   COM + 會指派預設屬性值。 您可以重新設定大部分的服務屬性。
-   將元件的交易屬性設定為 [ **必要** ] 可保證 com + 必須在交易中建立該元件的每個實例，但不一定會啟動新的交易。
-   確認交易是否存在，會確認元件的交易屬性值不會不慎重設為非交易值，例如「 **略** 過」或「 **不支援**」。
-   處理錯誤可讓您的元件更可靠且更容易進行疑難排解。
-   COM + 會針對交易元件強制執行 [JIT 啟用](com--just-in-time-activation.md) 和 [並行保護](com--synchronization.md) 服務。
-   當您完成資料庫連接時，請將其關閉，以允許相同交易中的另一個元件重複使用連接集區中的連接。  (連接共用不應與 [物件](com--object-pooling.md)共用混淆。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[步驟2：跨多個元件擴充交易](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[步驟3：重複使用元件](step-3--reusing-components.md)
</dt> <dt>

[COM + 即時啟用](com--just-in-time-activation.md)
</dt> <dt>

[COM + 同步處理](com--synchronization.md)
</dt> <dt>

[設定交易](configuring-transactions.md)
</dt> <dt>

[建立 COM + 應用程式](creating-com--applications.md)
</dt> <dt>

[設定交易屬性](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



