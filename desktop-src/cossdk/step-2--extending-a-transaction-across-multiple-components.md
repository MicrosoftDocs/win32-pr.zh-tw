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
# <a name="step-2-extending-a-transaction-across-components"></a>步驟2：跨元件擴充交易

## <a name="objectives"></a>目標

在此步驟中，您將瞭解下列各項：

-   交易流程
-   多個物件在交易中的投票方式

## <a name="description"></a>Description

[步驟1：建立交易元件](step-1--creating-a-transactional-component.md) 示範如何撰寫簡單的交易元件，以更新 Microsoft SQL Server Pubs 資料庫中的作者資訊。 步驟2顯示在多個元件之間擴充交易時所發生的情況。

為了保持 COM + 程式設計模型，在 `UpdateAuthorAddress` 完成其工作的過程中，會呼叫另一個元件。 第二個元件會 `ValidateAuthorAddress` 驗證作者的位址，並將結果傳回給它的呼叫者 `UpdateAuthorAddress` 。

與其呼叫端不同 `ValidateAuthorAddress` 的是，不需要交易，但仍可參與其呼叫端的交易。 在這個步驟中，其交易屬性值會設定為 [ **支援**]，如下圖所示，這會將現有的交易擴充至新的物件。

![顯示將現有交易擴充至新物件的圖表。](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

只有當呼叫端為交易式時， **支援** 的屬性值才會) 現有交易中擴充 (或流程。 當 `UpdateAuthorAddress` 呼叫時 `ValidateAuthorAddress` ，com + 會先查看呼叫端的內容，以查看它是否為交易式。 然後 COM + 會查看在上設定的服務屬性 `ValidateAuthorAddress` ，並將指派給呼叫端物件的相同交易識別碼指派給新的物件。 若要進一步瞭解此程式，請參閱 [內容啟用](context-activation.md)。

因為它們共用相同的交易識別碼，所以這兩個物件都必須順利完成其工作，否則 COM + 會中止交易， (復原對 Pubs 資料庫) 所做的任何變更。

參與交易的所有物件都會投票至認可或中止交易。 當您在程式碼中包含投票指令時，會明確地進行投票，如下列步驟1範例程式碼中所示的解壓縮程式代碼，該程式碼會建立 `UpdateAuthorAddress` 元件：


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



投票也會隱含地發生，如同在元件中所做的一樣 `ValidateAuthorAddress` 。 除非物件另行宣告，否則 COM + 會假設物件已順利完成其工作，但尚未準備好停用。 COM + 會進行下列假設：


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



當 `ValidateAuthorAddress` 回到其呼叫端時，COM + 會以認可的形式讀取其投票。 除非在停用根物件（在此案例中為交易中的第一個物件，即在此案例中為物件），否則 COM + 不會計入投票 `UpdateAuthorAddress` 。

## <a name="sample-code"></a>範例程式碼

`ValidateAuthorAddress`元件會簡單檢查作者的位址。 因為不 `UpdateAuthorAddress` 會明確投票，COM + 會使用預設投票設定。


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



## <a name="summary"></a>總結

-   將元件的交易屬性設定為 [ **支援** ] 可能會導致在呼叫物件的交易中建立新的物件。 COM + 會查看呼叫端的內容，以判斷新物件的交易狀態。 如果呼叫端是交易式的，COM + 會將交易流動至新的物件。
-   參與相同交易的所有物件都會共用一般交易識別碼，而 COM + 會從物件的內容讀取此識別碼。
-   交易中的每個物件都會與其他物件分開投票。 當根物件停用時，COM + 會計算投票。
-   您可以在認可和中止之間切換物件的交易，直到 COM + 停用物件為止，或直到 COM + 停用根物件並結束交易為止。 只有最後一個投票設定計數。 [**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)和 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)介面會提供方法，並產生如下表所示的類似投票結果。 您可以使用其中一個介面，在交易中明確地投票。 

    | [**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) 組合方法                                                                                                                                                      | [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 對等方法       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   除非元件有明確的投票，否則 COM + 會將物件的投票設定為對等的 [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) 。
-   明確投票可以減少交易的整體持續時間，以及釋出昂貴的資源鎖定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[步驟1：建立交易式元件](step-1--creating-a-transactional-component.md)
</dt> <dt>

[步驟3：重複使用元件](step-3--reusing-components.md)
</dt> <dt>

[內容啟用](context-activation.md)
</dt> <dt>

[管理 COM + 中的自動交易](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




