---
description: 在交易中使用非交易式元件
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: 在交易中使用非交易式元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689172"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>在交易中使用非交易式元件

將非交易式元件放置在交易中，以利用交易的 [ACID 屬性](acid-properties.md) 通常很有用。 例如，如果您使用非交易式舊版元件來更新網路上的密碼，您可以將這些元件放在交易中，以確保網路上的密碼更新是一致的。

*交易內容物件* 是泛型物件，可讓非交易式用戶端將多個 COM 物件的工作結合成單一交易，而不需要您特別針對該目的開發新元件。 相對於自動交易，交易內容物件需要其用戶端明確地認可或中止交易。

依預設，交易內容物件的交易屬性值會設定為 [必要]。 如果用戶端在沒有明確發出認可或中止呼叫的情況下釋放交易內容物件，COM + 就會中止交易。

下列 Visual Basic 範例顯示非交易式用戶端如何將一個以上的物件所完成的工作組成單一交易：


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a>交易內容物件的限制

以下是交易內容物件的一些重要限制：

-   使用交易內容物件時，將多個物件的工作結合成單一交易的應用程式邏輯會系結至特定的非交易式用戶端執行，而且會遺失使用 COM 元件的一些優點。 這些遺失的優點包括下列各項：
    -   在更大的交易中重複使用應用程式邏輯的能力
    -   宣告式安全性的拼版
    -   從用戶端遠端執行邏輯的彈性
-   交易內容物件會與非交易式用戶端一起執行，這表示 COM + 必須可在非交易式用戶端電腦上使用。 這可能不是問題，例如，從使用中的伺服器頁（在與 COM + 相同伺服器上執行的 (ASP) 頁面）使用交易內容物件時。
-   當您建立交易內容物件時，不會取得非交易式用戶端的內容。 交易式工作只能透過使用交易內容物件所建立的 COM 物件來間接完成。 尤其是，非交易式用戶端無法使用 COM + 資源機 (例如 ODBC) ，並將工作包含在交易中。 例如，開發人員可能會熟悉下列在關係資料庫系統上執行交易式工作的語法：

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    以類似的方式使用交易內容物件不會產生所需的結果：

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    在此範例中，呼叫 DoWork 不會在交易中登記。 相反地，您必須建立會呼叫 DoWork 的 COM 元件、使用交易內容物件來建立該元件的物件實例，然後從非交易式用戶端呼叫該物件，讓工作成為用戶端控制交易的一部分。

 

 



